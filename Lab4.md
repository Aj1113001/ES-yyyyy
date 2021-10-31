## 嵌入式系統 - 實作4: 七段顯示器, LCD 顯示器 + 超音波感測器 (W7, W9) 
## Lab 4-1 用七段顯示器來顯示數字"8."
![image](https://user-images.githubusercontent.com/89329295/137610094-b9ce2126-4979-473f-bad3-eb1918755ad5.png)
````c
void setup()
{
for(int x = 1; x < 9; x++) {
pinMode(x,OUTPUT);
}
}

void seg71(int a, int b, int c, int d, int e, int f, int g, int h)
{
digitalWrite(1, a);
digitalWrite(2, b);
digitalWrite(3, c);
digitalWrite(4, d);
digitalWrite(5, e);
digitalWrite(6, f);
digitalWrite(7, g);
digitalWrite(8, h);
delay(500);
}

void loop()
{
//    a, b, c, d, e, f, g, h
seg71(0, 0, 0, 0, 0, 0, 0, 0); // OFF
seg71(1, 1, 1, 1, 1, 1, 1, 1); // 8
}
````
## Lab 4-2 如下圖的Demo, 用七段顯示器, 顯示 . →1→ ... → 9 → 0 → 全滅, 狀態改變的間隔時間為0.5秒
![image](https://user-images.githubusercontent.com/89329295/137610346-12307a14-4334-41f7-85ad-73276ba02edd.png)
````c
void setup()
{
  for(int x = 1; x < 10; x++) {
      pinMode(x,OUTPUT);
  }
}

void SSD(int a, int b, int c, int d, int e, int f, int g, int h, int time = 500)
{
  digitalWrite(9, a);
  digitalWrite(2, b);
  digitalWrite(3, c);
  digitalWrite(4, d);
  digitalWrite(5, e);
  digitalWrite(6, f);
  digitalWrite(7, g);
  digitalWrite(8, h);
  delay(time);
}

void Display(int num) 
{
  switch (num) {
  	case 0:
    	SSD(0, 0, 0, 0, 0, 0, 0, 0, 0);
    	SSD(1, 1, 1, 1, 1, 1, 0, 0);
    	break;
    case 1:
    	SSD(0, 0, 0, 0, 0, 0, 0, 0, 0);
    	SSD(0, 1, 1, 0, 0, 0, 0, 0);
    	break;
    case 2:
    	SSD(0, 0, 0, 0, 0, 0, 0, 0, 0);
    	SSD(1, 1, 0, 1, 1, 0, 1, 0);
    	break;
    case 3:
    	SSD(0, 0, 0, 0, 0, 0, 0, 0, 0);
    	SSD(1, 1, 1, 1, 0, 0, 1, 0);
    	break;
    case 4:
    	SSD(0, 0, 0, 0, 0, 0, 0, 0, 0);
    	SSD(0, 1, 1, 0, 0, 1, 1, 0);
    	break;
    case 5:
    	SSD(0, 0, 0, 0, 0, 0, 0, 0, 0);
    	SSD(1, 0, 1, 1, 0, 1, 1, 0);
    	break;
    case 6:
    	SSD(0, 0, 0, 0, 0, 0, 0, 0, 0);
    	SSD(1, 0, 1, 1, 1, 1, 1, 0);
    	break;
    case 7:
    	SSD(0, 0, 0, 0, 0, 0, 0, 0, 0);
    	SSD(1, 1, 1, 0, 0, 1, 0, 0);
    	break;
    case 8:
    	SSD(0, 0, 0, 0, 0, 0, 0, 0, 0);
    	SSD(1, 1, 1, 1, 1, 1, 1, 0);
    	break;
    case 9:
    	SSD(0, 0, 0, 0, 0, 0, 0, 0, 0);
    	SSD(1, 1, 1, 1, 0, 1, 1, 0);
    	break;
    case 99: // dp
    	SSD(0, 0, 0, 0, 0, 0, 0, 0, 0);
    	SSD(0, 0, 0, 0, 0, 0, 0, 1);
    	break;
    default: // off
    	SSD(0, 0, 0, 0, 0, 0, 0, 0, 0);
    	SSD(0, 0, 0, 0, 0, 0, 0, 0);
    	break;
  }
}

void loop()
{
  	Display(100);
  	Display(99);
  	Display(1);
  	Display(2);
  	Display(3);
  	Display(4);
  	Display(5);
  	Display(6);
  	Display(7);
  	Display(8);
  	Display(9);
  	Display(0);
}
````
## Lab 4-3 LCD顯示"Hello" + 你的英文名字 (e.g., "Hello Horace")
![image](https://user-images.githubusercontent.com/89329295/139565260-b914ec67-3e46-4668-9079-f6fa989a8f7b.png)
````c
// include the library code:
#include <LiquidCrystal.h>

// initialize the library with the numbers of the interface pins
LiquidCrystal lcd(12, 11, 5, 4, 3, 2);

void setup() {
  // set up the LCD's number of columns and rows:
  lcd.begin(16, 2);
  // Print a message to the LCD.
  lcd.print("hello, Iris!");
}

void loop() {
  // set the cursor to column 0, line 1
  // (note: line 1 is the second row, since counting begins with 0):
  lcd.setCursor(0, 1);
  // print the number of seconds since reset:
  lcd.print(millis() / 1000);
}
````
## Lab 4-4 整合超音波感測器 + LCD: 參考之前的實作, 完成以下任務:
## 1.將超音波感測器傳回的距離, 在LCD上面顯示,
## 2.同時也和之前的實作一樣, 在序列輸出.
## 3.另外, 當物體的距離小於150cm時, 則亮紅色LED, 否則亮綠色LED
![image](https://user-images.githubusercontent.com/89329295/139565728-263a7d30-3f1c-4017-96b8-f534a4bb638e.png)
````c
#include <LiquidCrystal.h>

#define echo 7
#define trig 7
  
float  duration; // time taken by the pulse to return back
float  dd; // oneway distance travelled by the pulse
int RLED = 9;
int GLED = 8;

LiquidCrystal lcd(12, 11, 5, 4, 3, 2);

void setup() {
  digitalWrite(RLED, OUTPUT);
  digitalWrite(GLED, OUTPUT);
  lcd.begin(16, 2);
}

void loop() {
  time_Measurement();
  dd = duration * 0.01723;   
  lcd.setCursor(0, 0);
  lcd.print("Distance, cm: ");
  lcd.setCursor(0, 1);
  lcd.print(dd);
  
    if (dd < 150) {
    digitalWrite(RLED, HIGH);
    digitalWrite(GLED, LOW);
  } else {
    digitalWrite(RLED, LOW);
    digitalWrite(GLED, HIGH);
  }
}
  
void time_Measurement()
{ //function to measure the time taken by the pulse to return back
    pinMode(trig, OUTPUT);
    digitalWrite(trig, LOW);
    delayMicroseconds(2);  
    digitalWrite(trig, HIGH);
    delayMicroseconds(10);
    digitalWrite(trig, LOW);
    pinMode(echo, INPUT);  
    duration = pulseIn(echo, HIGH);
}
````

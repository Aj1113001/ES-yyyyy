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

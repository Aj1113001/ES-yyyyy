## 嵌入式系統 - 實作3: 使用超音波感測器 + LED控制, 常用的C語言程式介紹
## Lab 3-1: Ultrasonic Sensor (3-pin) + 測距 (以公分顯示即可) + RS232 Output
![image](https://user-images.githubusercontent.com/89329295/134792689-f87d567d-7f07-490c-b097-c70bb14a35fb.png)
![image](https://user-images.githubusercontent.com/89329295/134792715-0e3f9eb4-f914-47c9-9c6b-cbfe4fd49008.png)
````c
int inches = 0;

int cm = 0;

long readUltrasonicDistance(int triggerPin, int echoPin)
{
  pinMode(triggerPin, OUTPUT);  // Clear the trigger
  digitalWrite(triggerPin, LOW);
  delayMicroseconds(2);
  // Sets the trigger pin to HIGH state for 10 microseconds
  digitalWrite(triggerPin, HIGH);
  delayMicroseconds(10);
  digitalWrite(triggerPin, LOW);
  pinMode(echoPin, INPUT);
  // Reads the echo pin, and returns the sound wave travel time in microseconds
  return pulseIn(echoPin, HIGH);
}

void setup()
{
  Serial.begin(9600);

}

void loop()
{
  // measure the ping time in cm
  cm = 0.01723 * readUltrasonicDistance(7, 7);
  // convert to inches by dividing by 2.54
  inches = (cm / 2.54);
  Serial.print(inches);
  Serial.print("in, ");
  Serial.print(cm);
  Serial.println("cm");
  delay(100); // Wait for 100 millisecond(s)
}
````
## Lab 3-2: 超音波感測器 + LED (紅色LED:亮<70cm, 緑色LED: 亮>270cm, 藍色LED:亮, 介於70cm ~ 270cm之間) + RS232 Output
## 紅
![image](https://user-images.githubusercontent.com/89329295/134793626-b9cbf106-1735-42e7-8eb0-ef35f5f667b1.png)
## 綠
![image](https://user-images.githubusercontent.com/89329295/134793634-d83faa27-f6af-4bd3-aafa-d6183b8f61b3.png)
## 藍
![image](https://user-images.githubusercontent.com/89329295/134793644-4688e40a-3746-416f-b974-fd311636c03e.png)
````c
int inches = 0;
int GLED = 8;
int RLED = 12;
int BLED = 10;
int cm = 0;


void LED(int RH, int GH,int BH)
{  
  digitalWrite(RLED, RH);
  digitalWrite(GLED, GH);
  digitalWrite(BLED, BH);
}

long readUltrasonicDistance(int triggerPin, int echoPin)
{
  pinMode(triggerPin, OUTPUT); //clear the trigger
  digitalWrite(triggerPin, LOW);
  delayMicroseconds(2);
  // Sets the trigger pin to HIGH state for 10 microseconds
  digitalWrite(triggerPin, HIGH);
  delayMicroseconds(10);
  digitalWrite(triggerPin, LOW);
  pinMode(echoPin, INPUT);
  return pulseIn(echoPin, HIGH);
 }

void setup()
{
  Serial.begin(9600);
  digitalWrite(GLED, OUTPUT);
  digitalWrite(RLED, OUTPUT);
  digitalWrite(BLED, OUTPUT);
}

void loop()
{
  // measure the ping time in cm
  cm = 0.01723 * readUltrasonicDistance(7, 7);
  // convert to inches by sividing by 2.54
  inches = (cm / 2.54);
  Serial.print(inches);
  Serial.print("in, ");
  Serial.print(cm);
  
  if(cm<70){
    LED(1, 0, 0); // int RH, int GH, int BH
  }
  else if(cm>270){
    LED(0, 0, 1); // int RH, int GH, int BH
  }
  else{
    LED(0, 1, 0);  // int RH, int GH, int BH
  }
  
  Serial.println("cm");
  delay(100); 
}
````
## Lab 3-3: Arudino常用的C語言程式介紹與實作
![image](https://user-images.githubusercontent.com/89329295/137609283-1342c387-e94a-4fc4-a1ad-5114a5215a3c.png)
````c
int RLED = 13;
int GLED = 11;


int result, result2, result3;
String d0 = "****** 9X9 Table ******";
String d1, d2, d3;
void setup()
{
  pinMode(RLED, OUTPUT);   // Configure PIN13
  pinMode(GLED, OUTPUT);   // Configure PIN11
  
  Serial.begin(9600);

}

void loop()
{
  int aa = 0;

  Serial.println(d0); 
  
  digitalWrite(RLED, HIGH);
  analogWrite(GLED, aa); 
  
  for (int i=1;i<=9; i=i+3){
    for (int j=1;j<=9; j++){
      
      result = i*j;
      result2 = (i+1)*j;
      result3 = (i+2)*j;
      
      d1 = String(String(i) + "X" + String(j) + "=" + String(result));
      d2 = String(String(i+1) + "X" + String(j) + "=" + String(result2));
      d3 = String(String(i+2) + "X" + String(j) + "=" + String(result3));
      
      Serial.println(d1 + ", " + d2 + ", " + d3);


       
      aa+=1;
      
      delay(100);
    } // loop j
    analogWrite(GLED, aa*3); 
    Serial.println("");
  } // loop i

  digitalWrite(RLED, LOW);
  analogWrite(GLED, 255); 
  delay(2000);	
  analogWrite(GLED, 0);
}
````c


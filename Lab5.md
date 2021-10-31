## Lab 5-1 請使用兩個伺服馬達同步從 0 度逐步掃描到 180 度之後再逐步掃描回0度, 每步的間隔時間為50ms (0.05秒)
![image](https://user-images.githubusercontent.com/89329295/139565841-88a60cdc-0609-4035-aef6-8fd0ad8c803a.png)
````c
#include <Servo.h>

int pos = 0;

Servo servo_9;
Servo servo_8;
void setup()
{
  servo_9.attach(9, 500, 2500);
  servo_8.attach(8, 500, 2500);  
}

void loop()
{
// 從 0 到 180 度逐步掃描伺服, 1度/步
  for (pos = 0; pos <= 180; pos += 1) {

    servo_9.write(pos);
    servo_8.write(pos);       

    delay(50); // 等50ms (0.05秒)
  }
  
  for (pos = 180; pos >= 0; pos -= 1) {
// 從 180 到 0 度逐步掃描伺服, 1度/步
    servo_9.write(pos);
    servo_8.write(pos);        

    delay(50); // 等50ms (0.05秒)
  }
}
````
## Lab 5-2 LCD顯示溫度感應器的溫度;若溫度<38 綠LED亮; 若大於38度, 紅色LED亮
接線圖(<38 綠燈亮)
![image](https://user-images.githubusercontent.com/89329295/139565933-41e2d734-88bb-44a5-a2d7-b27dbf7bf656.png)
接線圖(>=38 紅燈亮)
![image](https://user-images.githubusercontent.com/89329295/139565974-5b929977-40cf-4fc4-9686-712b3c99cf66.png)
````c
#include <LiquidCrystal.h>

LiquidCrystal lcd(12, 11, 5, 4, 3, 2);
float tempC, reading,voltage;
int RLED = 9;
int GLED = 8;
void setup() {
  lcd.begin(16, 2);
  pinMode(A1, INPUT); // Read analog voltage level (2^10)
  pinMode(RLED, OUTPUT);
  pinMode(GLED, OUTPUT);
  Serial.begin(9600);	

}

void loop() {
  reading = analogRead(A1);  // read analog level level (2^10)
  voltage = (reading/1024.0) * 5.0;
  tempC = (voltage - 0.5) * 100.0;

  lcd.setCursor(0,0);  
  lcd.print("TMP Sensor Demo");
  //實作
  if(tempC<38)
  {
    digitalWrite(RLED, LOW);
    digitalWrite(GLED, HIGH); 
  }
  else
  {
    digitalWrite(RLED, HIGH);
    digitalWrite(GLED, LOW);
  }

  lcd.setCursor(0,1);
  lcd.print("Tmp:");
  lcd.print(tempC);
  lcd.print(" C");
  delay(500);
  lcd.clear();
  Serial.println(reading);
  Serial.println(voltage);  
}
````

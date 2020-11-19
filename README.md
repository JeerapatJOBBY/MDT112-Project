# MDT112 : 1. อุปกรณ์ถอกรหัส



## สมาชิก



| ชื่อ      | ชื่อเล่น          | รหัส  |Github Profile Link|
| ------------- |:-------------:| -----:|----|
|นายจีรัฒน์ บรรจง     | จ๊อบ  | 62120501057 |https://github.com/JeerapatJOBBY|
|||||
|||||

# รายละเอียดโปรเจค


# โค้ดใหม่
#include <Adafruit_GFX.h>
#include <Adafruit_SSD1306.h>
#include <SPI.h>
#include <Wire.h>

Adafruit_SSD1306 oled = Adafruit_SSD1306(128, 32, &Wire);    //ประกาศสร้าง oject ที่ใช้ลองรับชื่อของอุปกรณ์

String var1[] = {"A","B","C","D","E","F","G","H","I","J","K","L","M","N","O","P","Q","R","S","T","U","V","W","X","Y","Z"};   //ประกาศอาเรย์ตัวหนังสืออยู่ตรงนี้

void setup() 
{
  pinMode(2, INPUT_PULLUP); 
  oled.begin(0x3C); // Address 0x3C for 128x32
  Serial.begin(9600);
}
int i = 0;
void loop() 
{
  oled.clearDisplay();      //ล้างหน้าจอแสดงผล
  oled.setCursor(0, 0);        //กำหนดตำตำแหน่ง curcor (แกน x, แกน y)
  oled.setTextColor(SSD1306_WHITE);         //กำหนดสีของตัวหนังสือ  (มีแค่สีขาว)
  oled.setTextSize(1);                          //กำหนดขนาดของตัวหนังสือ(มีตั้งแต่1-3)
  oled.println("Guu kuy yai mark");        //แสดงคำบนหน้าจอ
  oled.display();           //แสดงการทำงานทั้งหมด
  delay(10);            //หน่วงเวลา
}

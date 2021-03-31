# การทดลองที่ 7 เรื่อง การประยุกต์ใช้โปรเเกรม

## วัตถุประสงค์
* เพื่อเข้าใจการประยุกต์ใช้โปรเเกรมที่ซับซ้อนขึ้น
* เข้าใจในหลักการทำงานของ microcontroller
* เพื่อนำโปรเเกรมไปประยุกใช้ในชีวิตประจำวัน

## อุปกรณ์ที่ใช้
* ไมโครคอนโทรลเลอร์ ESP-01
* สายUSB
* ESP-01 board adapter/Serial port
* adapter ของ port0 เเละ port1
* LED สองสี
* ออด

## ศึกษาข้อมูลเบื้องต้น
* ได้เเก่
  * https://www.youtube.com/watch?v=CCnN1WJsXQY
  * https://github.com/choompol-boonmee/lab63b/tree/master/examples

## วิธีการทดลอง
1. ต่อ serial port กับ adapter
2. ต่อเข้ากับ adapter เเละ port1 ส่วน port0 ต่อขนานกับออด
3. ต่อทุกอย่างเข้ากับ ESP-01
4. นำโปรเเกรมใน folder Example ชื่อ 03_Output-port มาเขียนบน microcontroller โดยพิมพ์ vi src/main.ccp เพื่อเช็ค

'''javascript
#include <Arduino.h>
#include <ESP8266WiFi.h>

int cnt = 0;

void setup()
{
	Serial.begin(115200);
	pinMode(0, OUTPUT);
	Serial.println("\n\n\n");
}

void loop()
{
	cnt++;
	if(cnt % 2) {
		Serial.println("========== ON ===========");
		digitalWrite(0, HIGH);
	} else {
		Serial.println("========== OFF ===========");
		digitalWrite(0, LOW);
	}
	delay(500);
}
'''

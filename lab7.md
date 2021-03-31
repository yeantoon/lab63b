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
* รีเลย์

## ศึกษาข้อมูลเบื้องต้น
* ได้เเก่
  * https://www.youtube.com/watch?v=CCnN1WJsXQY
  * https://github.com/choompol-boonmee/lab63b/tree/master/examples

## วิธีการทดลอง
1. ต่อ serial port กับ adapter
2. ต่อเข้ากับ adapter port1 port0 เเละออด
3. ต่อทุกอย่างเข้ากับ ESP-01
4. นำโปรเเกรมใน folder Example ชื่อ 03_Output-port มาเขียนบน microcontroller โดยพิมพ์ vi src/main.ccp เพื่อเช็ค
```javascript
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
```
5. ทำการเเก้ไข
```javascript
#include <Arduino.h>
#include <ESP8266WiFi.h>
int cnt = 0;

void setup()
{
	Serial.begin(115200);
	pinMode(0, OUTPUT);
	pinMode(1, OUTPUT);
	Serial.println("\n\n\n");
}

void loop()
{
	cnt++;
	if(cnt % 2) {
		Serial.println("========== red ON ===========");
		digitalWrite(0, HIGH);
		Serial.println("========== blue OFF ===========");
		digitalWrite(1, LOW);
	} else {
		Serial.println("========== red OFF ===========");
		digitalWrite(0, LOW);
		Serial.println("========== blue ON ===========");
		digitalWrite(1, HIGH);
	}
	delay(1000);
}
```

6. upload ลงบน microcontroller โดยใช้คำสั่ง pio run -t upload พร้อมกับกดปุ่ม upload เเละ reset เพื่อให้ ESP-01 รับโปรเเกรม
7. ใช้คำสั่ง pio device monitor เพื่อดูผลลัพท์

## การบันทึกผลการทดลอง
* เมื่อทำการกดปุ่มเปิดเเล้วมีเสียงออดดังตลอด เเละหลอดไฟทั้งสองหลอดสับกันกระพริบทุกๆ 1 วินาที
* ไฟสีเเดงจะเปิดเมือ port0 เเสดงผลเป็น on เเละจะปิดเมือเเสดงผลเป็น off ไฟสีน้ำเงินจะเปิดเมื่อ port1เเสดงผลเป็น on เเละจะปิดเมือเเสดงผลเป็น off

## อภิปรายผลการทดลอง
* การนำโปรเเกรมใน folder Example ชื่อ 03_Output-port มาปรับเปลี่ยนเเละเขียนลงบน microcontroller เพื่อทดสอบเมือกด device monitor run ผลลัพท์จะเเสดงสลับ red on/blue off สลับ on/off ทุกๆ 1 วินาที ทำให้ทุกครั้งที่เเสดง on หลอดไฟที่ port0 จะติด ส่วน port1 จะดับสลับกันไป เมื่อนำไปต่อกับ reley มันก็จะทำหน้าที่เป็นสวิซท์เปิดปิด

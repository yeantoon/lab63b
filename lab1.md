# การทดลองที่ 1 เรื่อง การเขียนโปรแกรมเพื่อรันบนไมโครคอนโทรเลอร์

## วัตถุประสงค์
* เขียนโปรเเกรมเพื่อรันบนไมโครคอนโทรเลอร์

## อุปกรณ์ที่ใช้
* ไมโครคอนโทรลเลอร์ ESP-01
* สายUSB
* ESP-01 board adapter/Serial port

## ศึกษาข้อมูลเบื้องต้น
* ได้เเก่
  * https://www.youtube.com/watch?v=NLIUsWLEpmg
  * https://platformio.org/
  * https://github.com/choompol-boonmee/lab63b/tree/master/examples

## วิธีการทดลอง
1. ต่อ Microcontroller เข้า serial
![image](C:\Users\ธีรภัทร สิงห์ตะนะ\Desktop\lab\lab1)
2. นำโปรเเกรมใน folder Example ชื่อ 01_serial_monitor มาเขียนบน microcontroller เพื่อทดสอบ

3. ใช้ platformio.ini เพื่อรัน

4. upload ลงบน microcontroller โดยใช้คำสั่ง pio run -t upload

5. กดปุ่มใน microcontroller ให้ reset เพื่อรับโปรเเกรมใหม่

6. ใช้คำสั่ง pio device monitor เพื่อดูผลลัพท์


## การบันทึกผลการทดลอง
เมื่อพิมพ์คำสั่ง pio device monitor ตัวเเปร count จะเริ่มนับโดยเพิ่มทีละ 1 ทุกๆ 1 วินาที เมื่อกด reset ที่ esp-01 ก็จะเริ่มต้นนับที่ 0 เเล้วเพิ่มทีละ 1 ทุกๆ 1 วินาทีใหม่

## อภิปรายผลการทดลอง
* การทดลองเขียนโปรเเกรมลงบน Microcontroller โดยเลือกเป็นโปรเเกรม Serial monitor จะเป็นโปรเเกรมเเสดงผล count ซึ่งเพิ่มขึ้นที่ละ 1 ทุกๆ 1 วินาที

## คำถามหลังการทดลอง
* ผลของการ count มีที่สิ้นสุดหรือไม่
   * ไม่

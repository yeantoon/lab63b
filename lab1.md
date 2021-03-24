# การทดลองที่ 1 เรื่อง การเขียนโปรแกรมเพื่อรันบนไมโครคอนโทรเลอร์

## วัตถุประสงค์
* เขียนโปรเเกรมเพื่อรันบนไมโครคอนโทรเลอร์

## อุปกรณ์ที่ใช้
1. ไมโครคอนโทรลเลอร์ ESP-01
2. สายUSB
3. ESP-01 board adapter/Serial port

## ศึกษาข้อมูลเบื้องต้น
* ได้เเก่
  * https://www.youtube.com/watch?v=NLIUsWLEpmg
  * https://platformio.org/
  * https://github.com/choompol-boonmee/lab63b/tree/master/examples

## วิธีการทดลอง
1. ต่อ Microcontroller เข้า serial
2. นำโปรเเกรมใน folder Example ชื่อ 01_serial_monitor มาเขียนบน microcontroller เพื่อทดสอบ
3. ใช้ platformio.ini เพื่อรัน
4. upload ลงบน microcontroller โดยใช้คำสั่ง pio run -t upload
5. กดปุ่มใน microcontroller ให้ reset เพื่อรับโปรเเกรมใหม่
6. ใช้คำสั่ง pio device monitor เพื่อดูผลลัพท์

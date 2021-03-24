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
![1](https://user-images.githubusercontent.com/80879503/112341378-f2993300-8cf3-11eb-8408-f290059c1b29.jpg)

2. นำโปรเเกรมใน folder Example ชื่อ 01_serial_monitor มาเขียนบน microcontroller เพื่อทดสอบ
![6](https://user-images.githubusercontent.com/80879503/112342160-94b91b00-8cf4-11eb-921b-5465bce10f3c.jpg)

3. ใช้ platformio.ini เพื่อรัน
![2](https://user-images.githubusercontent.com/80879503/112342221-a00c4680-8cf4-11eb-9ca8-46e6e7d2deea.jpg)

4. upload ลงบน microcontroller โดยใช้คำสั่ง pio run -t upload
![3](https://user-images.githubusercontent.com/80879503/112342240-a3073700-8cf4-11eb-970f-f34cf9bd6767.jpg)

5. กดปุ่มใน microcontroller ให้ reset เพื่อรับโปรเเกรมใหม่
![4](https://user-images.githubusercontent.com/80879503/112342262-a8fd1800-8cf4-11eb-960f-f7730034c7fa.jpg)

6. ใช้คำสั่ง pio device monitor เพื่อดูผลลัพท์
![5](https://user-images.githubusercontent.com/80879503/112342285-ad293580-8cf4-11eb-90a6-41f2db4a853b.jpg)

## การบันทึกผลการทดลอง
เมื่อพิมพ์คำสั่ง pio device monitor ตัวเเปร count จะเริ่มนับโดยเพิ่มทีละ 1 ทุกๆ 1 วินาที เมื่อกด reset ที่ esp-01 ก็จะเริ่มต้นนับที่ 0 เเล้วเพิ่มทีละ 1 ทุกๆ 1 วินาทีใหม่
![e1](https://user-images.githubusercontent.com/80879503/112342531-e06bc480-8cf4-11eb-8303-9e01c4891445.jpg)

## อภิปรายผลการทดลอง
* การทดลองเขียนโปรเเกรมลงบน Microcontroller โดยเลือกเป็นโปรเเกรม Serial monitor จะเป็นโปรเเกรมเเสดงผล count ซึ่งเพิ่มขึ้นที่ละ 1 ทุกๆ 1 วินาที
![e2](https://user-images.githubusercontent.com/80879503/112342544-e3ff4b80-8cf4-11eb-9ec8-a9fc7dbe6162.jpg)

## คำถามหลังการทดลอง
* ผลของการ count มีที่สิ้นสุดหรือไม่
   * ไม่

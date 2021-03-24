# การทดลองที่ 6 เรื่อง การเขียนโปรแกรมสร้างไวไฟแอคเซสพอยต์ (Wifi AP)

## วัตถุประสงค์
* เพื่อเขียนโปรแกรมสร้างไวไฟแอคเซสพอยต์

## อุปกรณ์ที่ใช้
* ไมโครคอนโทรลเลอร์ ESP-01
* สายUSB
* ESP-01 board adapter/Serial port

## ศึกษาข้อมูลเบื้องต้น
* ได้เเก่
  * https://www.youtube.com/watch?v=T26DVHePlTs
  * https://github.com/choompol-boonmee/lab63b/tree/master/examples

## วิธีการทดลอง
1. ต่อ serial port กับ adapter

![1](https://user-images.githubusercontent.com/80879503/112361613-2b420800-8d06-11eb-86b9-61fdee20effb.jpg)

2. นำโปรเเกรมใน folder Example ชื่อ 06_wifi-ap-web-server มาเขียนบน microcontroller เพื่อทดสอบ
![1](https://user-images.githubusercontent.com/80879503/112362034-94c21680-8d06-11eb-8019-4f2204cafdd2.jpg)
![2](https://user-images.githubusercontent.com/80879503/112362042-97bd0700-8d06-11eb-9d14-1994a5cc9723.jpg)

3. upload ลงบน microcontroller โดยใช้คำสั่ง pio run -t upload พร้อมกับกดปุ่ม upload เเละ reset เพื่อให้ ESP-01 รับโปรเเกรม
![3](https://user-images.githubusercontent.com/80879503/112362106-aacfd700-8d06-11eb-9246-4b952ea3d102.jpg)

4. ใช้คำสั่ง pio device monitor เพื่อดูผลลัพท์
![4](https://user-images.githubusercontent.com/80879503/112362505-187c0300-8d07-11eb-97d0-9aed7ddf8c7b.jpg)

5. ลองใช้โทรศัพท์หรือคอมพิวเตอร์หาไวไฟที่สร้าง
![5](https://user-images.githubusercontent.com/80879503/112362773-5ed16200-8d07-11eb-9fdf-d462e628a93e.jpg)

## การบันทึกผลการทดลอง
* หลังจากการ pio run microcontroller ก็สร้างไวไฟชื่อ HI_BMFWIFI_2.4G

## อภิปรายผลการทดลอง
* หลังจากการ run 06_wifi-ap-web-server ลงบน ESP-01 ก็สร้างไวไฟชื่อ HI_BMFWIFI_2.4G ขึ้นมาเเละสามารถ connect ได้

## คำถามหลังการทดลอง
* สามารถนำไปประยุกต์ใช้กับอะไรได้บ้าง
  *  นำมาสร้างเครือค่ายเองได้

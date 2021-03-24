# การทดลองที่ 2 เรื่องการเขียนโปรเเกรมหาไวไฟ

## วัตถุประสงค์
*เพื่อลงโปรเเกรมหาไวไฟในบอร์ด ESP-01

## อุปกรณ์ที่ใช้
* ไมโครคอนโทรลเลอร์ ESP-01
* สายUSB
* ESP-01 board adapter/Serial port

## ศึกษาข้อมูลเบื่องต้น
* ได้เเก่
  * https://www.youtube.com/watch?v=yBjab0UNuB8
  * https://github.com/choompol-boonmee/lab63b/tree/master/examples
 
## วิธีการทดลอง
1. ต่อ Microcontroller เข้า serial
![1](https://user-images.githubusercontent.com/80879503/112345669-d26b7300-8cf7-11eb-98b5-8ebfec4b1848.jpg)


2. นำโปรเเกรมใน folder Example ชื่อ 02_scan-wifi มาเขียนบน microcontroller เพื่อทดสอบ
![2](https://user-images.githubusercontent.com/80879503/112346414-84a33a80-8cf8-11eb-83f9-7c3f133f3b02.jpg)
![4](https://user-images.githubusercontent.com/80879503/112346967-0e530800-8cf9-11eb-8d5b-ca4eeb9884a8.jpg)

3. upload ลงบน microcontroller โดยใช้คำสั่ง pio run -t upload
![3](https://user-images.githubusercontent.com/80879503/112346948-098e5400-8cf9-11eb-9a8c-348286bab043.jpg)

4. กดปุ่มอัพโหลดและปุ่มรีเซ็ต บน Serial port เพื่อให้ Microcontroller รับโปรแกรมใหม่
![5](https://user-images.githubusercontent.com/80879503/112347289-4b1eff00-8cf9-11eb-96a8-04ed656af81b.jpg)


5. ใช้คำสั่ง pio divice monitor เพื่อเเสดงไวไฟที่ scan เจอ
![6](https://user-images.githubusercontent.com/80879503/112347553-8b7e7d00-8cf9-11eb-9ddd-4e42d973b107.jpg)

## การบันทึกผลการทดลอง
* หลังจากการ upload โปรเเกรมเสร็จเเล้วทำการเเสกนก็จะเจอไวไฟ ถ้าทำการกดปุ่ม reset program ก็จำทำงานใหม่
![7](https://user-images.githubusercontent.com/80879503/112347872-d39d9f80-8cf9-11eb-8c22-26a63fddd34d.jpg)

## อภิปรายผลการทดลอง
* การเขียนโปรเเกรมหาไวไฟโดยใช้ ESP-01 โดยใช้ Scan-wifi ทำให้ Microcontroller สามาหาไวไฟรอบๆได้
![7](https://user-images.githubusercontent.com/80879503/112348073-0e9fd300-8cfa-11eb-9edb-c91e406fb804.jpg)

## คำถามหลังการทดลอง
* จำนวนไวไฟที่ค้นได้ขึ้รอยู่กับอะไร
  * จำนวนไวไฟรอบๆ

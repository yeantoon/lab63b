# การทดลองที่ 4 เรื่อง การเขียนโปรแกรมอินพุทสัญญาณดิจิทัล

## วัตถุประสงค์ 
* นำสัญญาณ input จากภายนอกเข้า Microcontroller

## อุปกรณ์ที่ใช้
* ไมโครคอนโทรลเลอร์ ESP-01
* สายUSB
* ESP-01 board adapter/Serial port
* sensor เเสง ที่ต่อติดกับตัวต้านทาน
* adapter ของ port0 เเละ port1
* LED สองสี

## ศึกษาข้อมูลเบื้องต้น
* ได้เเก่
  * https://www.youtube.com/watch?v=nFqoZT26U5k
  * https://github.com/choompol-boonmee/lab63b/tree/master/examples

## วิธีการทดลอง
1. ต่อ serial port กับ adapter เเละ ESP-01

![2](https://user-images.githubusercontent.com/80879503/112354888-b966c000-8cff-11eb-8aa2-36e789bff509.jpg)

2. นำโปรเเกรมใน folder Example ชื่อ 04_input-port มาเขียนบน microcontroller เพื่อทดสอบ
![1](https://user-images.githubusercontent.com/80879503/112354971-cb486300-8cff-11eb-90b1-754050080017.jpg)

3. upload ลงบน microcontroller โดยใช้คำสั่ง pio run -t upload พร้อมกับกดปุ่ม upload เเละ reset เพื่อให้ ESP-01 รับโปรเเกรม
![3](https://user-images.githubusercontent.com/80879503/112355219-077bc380-8d00-11eb-9975-16111d79dc52.jpg)

4. ใช้คำสั่ง pio device monitor เพื่อดูผลลัพท์
![4](https://user-images.githubusercontent.com/80879503/112355367-28441900-8d00-11eb-812b-4a80628e289a.jpg)

5. นำสายไฟเส้นสีขาว(Port 0) ไปจิ้มเข้าช่องเดียวกันกับสายสีดำที่ให้สัญญาณ Input เป็น 0 จะแสดงผลoutputเป็น read 0 (ไฟติด) ถ้านำไปจิ้มเข้าช่องเดียวกันกับสายสีแดงที่ให้สัญญาณ Input เป็น 1 จะแสดงผลoutputเป็น read 1 (ไฟไม่ติด)
![5](https://user-images.githubusercontent.com/80879503/112355953-b9b38b00-8d00-11eb-8031-66d2a88696ae.jpg)
เมื่อกดปุ่มดำจะทำให้ port0 read0 ไฟติด เมื่อไม่กดจะ read1 ไฟไม่ติด
![51](https://user-images.githubusercontent.com/80879503/112357103-cc7a8f80-8d01-11eb-881a-9ccc87cfcca9.jpg)
![52](https://user-images.githubusercontent.com/80879503/112357127-cf758000-8d01-11eb-8c2d-3ebeac68f46b.jpg)

6. นำตัวต้านทานไปต่อกับสายไฟสีเเดงที่มีไฟเลี้ยง3v ขาตัวต้านทานที่พันกับsensorต่อกับ port0 ขาsensorต่อกับเส้นสีดำ นำเส้นสีขาวต่อกับ port0

![6](https://user-images.githubusercontent.com/80879503/112357974-78bc7600-8d02-11eb-9a7a-2594d63d9bc8.jpg)

7. เมื่อ sensor เจอกับไฟจะได้ค่า read0 ไฟจะติด ถ้าเอานิ้วบังจะอ่านค่า read1 ไฟจะดับ
![61](https://user-images.githubusercontent.com/80879503/112358415-e9639280-8d02-11eb-8b24-9950027816d7.jpg)
![62](https://user-images.githubusercontent.com/80879503/112358432-ee284680-8d02-11eb-8f13-9196a9b3e9de.jpg)

## การบันทึกผลการทดลอง
* หลังจากการลงโปรเเกรมเเล้วเมื่อนำสายไฟสีขาวไปฟจิ้มสีดำ input เป็น 0 outputออกมาเป็น read0 ไฟจะติด เมื่อสายสีขาวไปจิ้มกับสายสีเเดง input เป็น 1 outputออกมาเป็น read1 ไฟจะดับ
* เมื่อนำไปต่อกับ sensor ถ้าเจอเเสง output เป็น 0 ไฟจะติด ถ้าเอานิ้วไปปิดจะได้ค่า output เป็น1 ไฟจะดับ

## อภิปรายผลการทดลอง
*การนำโปรเเกรมใน folder Example ชื่อ 04_input-port มาเขียนบน microcontroller เพื่อทดสอบเมือกด device monitor runหลังจากการลงโปรเเกรมเเล้วเมื่อนำสายไฟสีขาวไปฟจิ้มสีดำ input เป็น 0 outputออกมาเป็น read0 ไฟจะติด เมื่อสายสีขาวไปจิ้มกับสายสีเเดง input เป็น 1 outputออกมาเป็น read1 ไฟจะดับ เมื่อนำไปต่อกับ sensor ถ้าเจอเเสง output เป็น 0 ไฟจะติด ถ้าเอานิ้วไปปิดจะได้ค่า output เป็น1 ไฟจะดับ

## คำถามหลังการทดลอง
* สามารถนำมาประยุกต์ใช้เป็นอะไรได้บ้่าง
  * สวิชท์ปิดเปิดไฟอัตโนมัติเมือมีเเสงหรือไม่มีเเสง


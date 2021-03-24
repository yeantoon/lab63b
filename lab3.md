# การทดลองที่ 3 เรื่อง การเขียนโปรแกรมเอ้าพุทสัญญาณดิจิทัล

## วัตถุประสงค์
* เพื่อเข้าใจการลงโปรเเกรมที่ส่ง outputสัญญาณดิจิตอลออกไปภายนอก

## อุปกรณ์ที่ใช้
* ไมโครคอนโทรลเลอร์ ESP-01
* สายUSB
* ESP-01 board adapter/Serial port
* รีเลย์
* adapter ของ port0 เเละ port1
* LED สองสี

## ศึกษาข้อมูลเบื้องต้น
* ได้เเก่
  * https://www.youtube.com/watch?v=CCnN1WJsXQY
  * https://github.com/choompol-boonmee/lab63b/tree/master/examples

## วิธีการทดลอง
1. ต่อ serial port กับ adapter

![1](https://user-images.githubusercontent.com/80879503/112349488-596e1a80-8cfb-11eb-8c74-5bd3aa986ac5.jpg)

2. ต่อ adapter port0 เเละ port1 เพื่อให้เห็น output ได้ง่ายขึ้น

![2](https://user-images.githubusercontent.com/80879503/112349891-b2d64980-8cfb-11eb-948e-e03cf7208eb4.jpg)

3. ต่อทุกอย่างเข้ากับ ESP-01

![3](https://user-images.githubusercontent.com/80879503/112351071-25472980-8cfc-11eb-9169-9864ab6dcc7a.jpg)

4. นำโปรเเกรมใน folder Example ชื่อ 03_Output-port มาเขียนบน microcontroller เพื่อทดสอบ
![4](https://user-images.githubusercontent.com/80879503/112351404-722b0000-8cfc-11eb-8a14-87a817473c36.jpg)

5. upload ลงบน microcontroller โดยใช้คำสั่ง pio run -t upload พร้อมกับกดปุ่ม upload เเละ reset เพื่อให้ ESP-01 รับโปรเเกรม
![5](https://user-images.githubusercontent.com/80879503/112351705-b28a7e00-8cfc-11eb-871d-0947de4f579d.jpg)

6. ใช้คำสั่ง pio device monitor เพื่อดูผลลัพท์
![6](https://user-images.githubusercontent.com/80879503/112351976-f4b3bf80-8cfc-11eb-91ef-414eec2ed6cf.jpg)

## การบันทึกผลการทดลอง
* หลอดไฟที่ต่อกับ port1 จะสว่างอยู่ตลอดเเละหลอดไฟที่ต่อกับport0 จะส่ว่างเมือค่าเเสดงผลเป็น on เเละจะเป็น off สลับ on ทุกๆ 0.5วินาที
* เมื่อต่อ reley เข้ากับวงจรก็จะกลายเป็นสวิชช์เปิดปิดไฟ(เสียงเปิดปิดเกิดจากreley)
![7](https://user-images.githubusercontent.com/80879503/112352831-b4087600-8cfd-11eb-8f78-cace4ca87435.jpg)

## อภิปรายผลการทดลอง
* การนำโปรเเกรมใน folder Example ชื่อ 03_Output-port มาเขียนบน microcontroller เพื่อทดสอบเมือกด device monitor run ผลลัพท์จะเเสดงสลับ on/off ทุกๆ 0.5 วินาที ทำให้ทุกครั้งที่เเสดง on หลอดไฟที่ port0 จะติด ส่วน port1 ติลตลอดเวลา เมื่อนำไปต่อกับ reley มันก็จะทำหน้าที่เป็นสวิซท์เปิดปิด

## คำถามหลังการทดลอง
* นอกจากต่อกับ LED เเล้วสามารถต่อกับอย่างอื่นเพื่อเเทนการเเสดงผลได้หรือไม่
  * ได้เช่น ออดไฟฟ้า

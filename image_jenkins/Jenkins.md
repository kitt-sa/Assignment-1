### How to install and config jenkins
#1.ติดตั้ง jenkines และ สามารถ Pull code จาก GitHub ได้
1.เมื่อเปิดตัวติดตั้งขึ้นมาให้กด Next
<img src="https://github.com/kitt-sa/Assignment-1/blob/main/image_jenkins/images/01.png" width="500"/>
2.เลือกโฟเดอร์ที่ต้องการติดตั้ง แล้วกด OK
<img src="images/02.png" width="500"/>
3.ใส่ user และ password ของเครื่อง แล้วกด Test Credentials
<img src="images/03.png" width="500"/>
<img src="images/04.png" width="500"/>
4.ไปที่ Local Security Policy ด้วยการ search "secpol"
<img src="images/05.png" width="500"/>
5.เลือก User Rights Assignment -> คลิ๊กขวาเลือก Properties ที่ Log on as a service
<img src="images/06.png" width="500"/>
6.เลือก Add User or Group... -> ในช่อง Enter the object names to select ให้ใส่ user ของเครื่อง -> เลือก Check Names -> เลือก OK
<img src="images/07.png" width="500"/>
7.กด OK
<img src="images/08.png" width="500"/>
8.กด Test Credentials หากถูกต้องจะขึ้นเครื่องหมายถูก แล้วกด Next
<img src="images/09.png" width="500"/>
9.กด Test Port แล้วกด Next
<img src="images/10.png" width="500"/>
10.เลือกโฟเดอร์ที่ติดตั้ง java jre ไว้ แล้วกด Next
<img src="images/11.png" width="500"/>
11.กด Next
<img src="images/12.png" width="500"/>
12.กด Install แล้ว รอจนกว่าจะติดตั้งเสร็จ
<img src="images/13.png" width="500"/>
<img src="images/14.png" width="500"/>
13.เมื่อกด Finish จะเปิด browser พร้อมแสดงหน้า Unlock Jenkins
<img src="images/15.png" width="500"/>
<img src="images/16.png" width="500"/>
14.ไปตาม path ที่แสดงไว้บนหน้าเว็บเพื่อคัดลอก password
<img src="images/17.png" width="500"/>
15.วาง password แล้วกด Continue
<img src="images/18.png" width="500"/>
16.เลือก install plugin แล้วรอจนเสร็จ
<img src="images/19.png" width="500"/>
17.สร้าง Admin User แล้วกด Save and Continue
<img src="images/20.png" width="500"/>
18.เมื่อเข้ามาจะมีหน้าตา
<img src="images/205.png" width="500"/>
19.ไปที่ Manage Jenkins -> Configure System
<img src="images/21.png" width="500"/>
20.เลื่อนหา Gitlab -> check Enable authentication for '/porject' end-point -> ตั้งชื่อ Connection -> ใส่ Gitlab URL -> ใน field Credentials เลือก Add "jenkins"
<img src="images/22.png" width="500"/>
21.ใน field Kind ให้เปลี่ยนเป็น Gitlab API token -> Scope เปลี่ยนเป็น Global -> วาง token ที่ได้มาจาก Gitlab
<img src="images/23.png" width="500"/>
22.เลือก Credentials ที่สร้างขึ้นมา แล้วกด Save
<img src="images/24.png" width="500"/>
23.ไปที่ New Item -> ตั้งชื่อ Project แล้วเลือก Freestyle project
<img src="images/25.png" width="500"/>
<img src="images/26.png" width="500"/>
24.check Github project -> ในช่อง Project url ใส่ url ของ repository จาก gitlab -> ช่อง Display name ใส่ชื่อของ repository -> ช่อง gitlab connection เลือกชื่อ connection ที่สร้างไว้
<img src="images/27.png" width="500"/>
25. ใน field Source Code Management เลือก Git ใส่ Repository URL -> เปลี่ยนชื่อ Branch
<img src="images/28.png" width="500"/>
26.ใน field Build Triggers ให้ check "Build when a change is pushed to GitLab." -> check "Accepted Merge Request Events" -> check "Closed Merge Request Events"
<img src="images/29.png" width="500"/>
27.ใน field Post-build Actions ให้เลือก Public build status to Gitlab แล้วกด Save
<img src="images/30.png" width="500"/>
28.เลือก Build Now
<img src="images/31.png" width="500"/>
29.เมื่อเข้ามาใน Workspace จะพบกับไฟล์ที่อยู่ใน Repository เดียวกันกับใน Github
<img src="images/32.png" width="500"/>
#2.สามารถ Compile code ที่เขียนด้วยภาษาต่างๆ เช่น ภาษา Python
1.ติดตั้ง Plugin Python Plugin
<img src="images/325.png" width="500"/>
2.ตั้ง directory
<img src="images/33.png" width="500"/>
3.พิมคำสั่งเพื่อรัน ไฟล์ py
<img src="images/34.png" width="500"/>
4.กด build now จะได้ผลลัพท์
<img src="images/35.png" width="500"/>
#3.สามารถทำงานร่วมกับ Robotframework เพื่อทำการทดสอบระดับ UAT บน Web application ได้
1.ติดตั้ง Plugin Robotframework
<img src="images/36.png" width="500"/>
2.ตั้ง directory ที่จะเก็บไฟล์ผลลัพท์ และ ตั้ง Thresholds -> กด Save
<img src="images/37.png" width="500"/>
3.กด build now จะได้ผลลัพท์
<img src="images/35.png" width="500"/>
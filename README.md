

AWS Cloudformation Template Creat VPC
======
1. สำหรับ Network วง /24 เท่านั้น CIDR Block คือ 10.0.0.1/24 - 10.0.0.10/24 สามารถแก้ไขได้ในไฟล์
2. จะสร้าง subnet รองรับแค่ 2 AZ เท่านั้น
3. สร้างทั้งหมด 6 Subnet  

|  Subnet Name       |  IPv4 CIDR          | Available IPs  |  GW  | Routing Table  |
| ------------- |:-------------:| -----:|-----:| -----:|  
| Public ZA  | 10.0.0.0/27 | 27 |  IG | Public-RT
| Public ZB  | 10.0.0.32/27 | 27 | IG | Public-RT
| Private ZA | 10.0.0.64/27 | 27 | NAT-GW | Private-RT
| Private ZB | 10.0.0.96/27 | 27 | NAT-GW | Private-RT
| DB ZA      | 10.0.0.128/27 | 27 | NAT-GW | Private-RT
| DB ZB      | 10.0.0.160/27 | 27 | NAT-GW | Private-RT

4. สามารถกำหนด Prefix ของ Subnet ได้เอง
5. สามารถกำหนด ชื่อของ VPC ได้


## Network Diagram

![alt text](https://image.ibb.co/bUnfGa/Cloudformation_Basic_VPC.png "Logo Title Text 1")


## ScreenShot

![alt text](https://image.ibb.co/kxLWpv/cloudformation.png "Logo Title Text 1")


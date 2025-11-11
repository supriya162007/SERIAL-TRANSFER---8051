# SERIAL-TRANSFER-OF-SINGLE-BYTE-CHARACTER-USING-8051-KEIL.-EMBEDDED-C-PROGRAM-

**AIM:** 

To write and execute Embedded C Program for Serial Transfer of Single Byte / Character using 8051 KEIL

**APPARATUS REQUIRED:**

Personal computer with Keil software

**PROGRAM:**

**(i)	Serial port transfer a character A**
```
#include<reg51.h> void main(void)
{
TMOD=0X20;//TIMER 1,MODE 2 TH1=0XFA;
SCON=0X50; TR1=1;
while(1)
{ SBUF='A';
while(TI==0); TI=0;
}
}
```
**(ii)	Serial port to Transfer a Message**
```
#include<reg51.h> void main(void)
{
unsigned char msg[]="SUPRIYA"; unsigned char i;
TMOD=0X20;//TIMER 1,MODE 2 TH1=0XFA;
SCON=0X50; TR1=1;
for (i=0; i<17;i++)
{
SBUF= msg[i]; while(TI==0); TI=0;
}
while(1);
}
```
**OUTPUT:**
![WhatsApp Image 2025-11-11 at 21 29 35_c8b43915](https://github.com/user-attachments/assets/a1cc4a9f-c618-4e97-8f12-06bd96f977f8)

**Result:**

Thus the Serial transfer of Single Byte / Character using 8051 KEIL was done and shown the output.

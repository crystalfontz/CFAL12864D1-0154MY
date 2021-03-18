# CFAL12864D1-0154MY Demo Code

Example Seeeduino (Arduino clone) code for the Crystalfontz CFAL12864D1-0154MY display. This is a yellow OLED with a 1.54" diagonal that can be interfaced with by SPI, I2C, and 8-bit Parallel.

The display and dev kit can be found here:

[CFAL12864D1-0154MY](https://www.crystalfontz.com/product/cfal12864d10154my) - OLED display\
[CFAL12864D1-0154MY-E1-2](https://www.crystalfontz.com/product/cfal12864d10154mye12) - OLED display + carrier board + Seeeduino pre-programmed with demo code
  
There are two carrier boards that can be purchased seperately if desired, the CFA10105 and the CFA10102. The CFA10105 is plug and play with this display and is the preferrable option. The CFA10102 is a generic board that will require the passive components to be soldered to it.

[CFA10105](https://www.crystalfontz.com/product/cfa10105) - plug and play adapter board\
[CFA10102](https://www.crystalfontz.com/product/cfa10102) - generic OLED adapter board





# Connection Details
## **To CFA10098 Adapter Board (See kits above)**
### **SPI Configuration**
Please note, the BS1 and BS2 jumpers should be unsoldered
| OLED/CFA10102       | Seeeduino Pin | Connection Description            
|---------------------|---------------|-----------------------------------
| 1  VDD              | 3v3           | Power Supply for Logic Circuit
| 2  D0               | D13           | LCD_D10 (DB0) (SCK)
| 3  GND              | GND           | Supporting pin to reduce stresses from ESD
| 4  D1               | D11           | LCD_D11 (DB1) (SDIN)
| 5  CS               | D8            | Chip Select
| 6  D2               | DNC           | LCD_D12 (DB2) 
| 7  D/C              | A0            | Data/Command Control
| 8  D3               | DNC           | LCD_D13 (DB3)
| 9  RES              | D9            | Power Reset for Controller and Driver
| 10 D4               | DNC           | LCD_D14 (DB4)
| 11 VEN              | DNC           | VOLED Enable Pin
| 12 D5               | DNC           | LCD_D15 (DB5)
| 13 E/RD             | A2            | Write Enable or Read
| 14 D6               | DNC           | LCD_D16 (DB6)
| 15 R/W              | A1            | Read/Write Select or Write
| 16 D7               | DNC           | LCD_D17 (DB7)

### **Parallel Configuration**
Please note, the BS1 and BS2 jumpers should be soldered according to the interface selected
| OLED/CFA10102       | Seeeduino Pin | Connection Description            
|---------------------|---------------|-----------------------------------
| 1  VDD              | 3v3           | Power Supply for Logic Circuit
| 2  D0               | D0            | LCD_D10 (DB0) 
| 3  GND              | GND           | Supporting pin to reduce stresses from ESD
| 4  D1               | D1            | LCD_D11 (DB1) 
| 5  CS               | D8            | Chip Select
| 6  D2               | D2            | LCD_D12 (DB2) 
| 7  D/C              | A0            | Data/Command Control
| 8  D3               | D3            | LCD_D13 (DB3)
| 9  RES              | D9            | Power Reset for Controller and Driver
| 10 D4               | D4            | LCD_D14 (DB4)
| 11 VEN              | DNC           | VOLED Enable Pin
| 12 D5               | D5            | LCD_D15 (DB5)
| 13 E/RD             | A2            | Write Enable or Read
| 14 D6               | D6            | LCD_D16 (DB6)
| 15 R/W              | A1            | Read/Write Select or Write
| 16 D7               | D7            | LCD_D17 (DB7)


## **To the display ZIF tail**
### **SPI Configuration**
| OLED/CFA10102       | Seeeduino Pin | Connection Description            
|---------------------|---------------|-----------------------------------
| 1  GND              | GND           | Supporting pin to reduce stresses from ESD
| 2  VLSS             | GND           | Ground of Analog Circuit
| 3  VSS              | GND           | Ground of Logic Circuit
| 4  NC               | DNC           | Reserved Pin
| 5  VDD              | 3v3           | Power Supply for Logic Circuit
| 6  BS1              | GND           | Interface select bit 1
| 7  BS2              | GND           | Interface select bit 2
| 8  CS               | D8            | Chip Select
| 9  RES              | D9            | Power Reset for Controller and Driver
| 10 D/C              | A0            | Data/Command Control
| 11 R/W              | A1            | Read/Write Select or Write
| 12 E/RD             | A2            | Write Enable or Read
| 13 D0               | D13           | LCD_D10 (DB0) (SCK)
| 14 D1               | D11           | LCD_D11 (DB1) (SDIN)
| 15 D2               | DNC           | LCD_D12 (DB2) 
| 16 D3               | 3v3           | LCD_D13 (DB3)
| 17 D4               | 3v3           | LCD_D14 (DB4)
| 18 D5               | 3v3           | LCD_D15 (DB5)
| 19 D6               | 3v3           | LCD_D16 (DB6)
| 20 D7               | 3v3           | LCD_D17 (DB7)
| 21 IREF             | DNC           | Current Reference for Brightness Adjustment
| 22 VCOMH            | GND           | Voltage Output Hight Level for COM Signal
| 23 VCC              | GND           | Power Supply for OEL Panel
| 24 GND              | GND           | Supporting pin to reduce stresses from ESD

#### **Parallel Configuration**
| OLED/CFA10102       | Seeeduino Pin | Connection Description            
|---------------------|---------------|-----------------------------------
| 1  GND              | GND           | Supporting pin to reduce stresses from ESD
| 2  VLSS             | GND           | Ground of Analog Circuit
| 3  VSS              | GND           | Ground of Logic Circuit
| 4  NC               | DNC           | Reserved Pin
| 5  VDD              | 3v3           | Power Supply for Logic Circuit
| 6  BS1              | GND           | Interface select bit 1
| 7  BS2              | GND           | Interface select bit 2
| 8  CS               | D8            | Chip Select
| 9  RES              | D9            | Power Reset for Controller and Driver
| 10 D/C              | A0            | Data/Command Control
| 11 R/W              | A1            | Read/Write Select or Write
| 12 E/RD             | A2            | Write Enable or Read
| 13 D0               | D0            | LCD_D10 (DB0)
| 14 D1               | D1            | LCD_D11 (DB1)
| 15 D2               | D2            | LCD_D12 (DB2)
| 16 D3               | D3            | LCD_D13 (DB3)
| 17 D4               | D4            | LCD_D14 (DB4)
| 18 D5               | D5            | LCD_D15 (DB5)
| 19 D6               | D6            | LCD_D16 (DB6)
| 20 D7               | D7            | LCD_D17 (DB7)
| 21 IREF             | DNC           | Current Reference for Brightness Adjustment
| 22 VCOMH            | GND           | Voltage Output Hight Level for COM Signal
| 23 VCC              | GND           | Power Supply for OEL Panel
| 24 GND              | GND           | Supporting pin to reduce stresses from ESD

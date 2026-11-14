<div dir="rtl" align="right">

# میکروکنترلر CH585 | هسته RISC-V، ارتباط BLE 5.4، USB 2.0 و NFC

<p align="center">
  <img src="Images/GitHub-Assets/MES-Hero-Banner.svg" width="100%" alt="MEMAR ELECTRONIC SANAT — MES">
</p>

## معرفی

میکروکنترلر **CH585** محصول شرکت **WCH**، مبتنی بر هسته پردازنده ۳۲ بیتی **RISC-V** از خانواده QingKe است. این تراشه مجموعه‌ای از قابلیت‌های پردازشی، ارتباطی و کنترلی را در یک قطعه ارائه می‌دهد و برای طراحی تجهیزات هوشمند، ابزارهای بی‌سیم، رابط‌های کاربری، تجهیزات USB و محصولات مبتنی بر BLE و NFC مناسب است.

CH585 از ارتباط بی‌سیم **Bluetooth Low Energy 5.4** و ارتباط اختصاصی 2.4GHz، رابط **USB 2.0 High-Speed (480Mbps)** و Full-Speed، رابط **NFC**، واحد تشخیص کلید لمسی، ADC، PWM و رابط‌های متداول ارتباطی پشتیبانی می‌کند.

این مخزن مجموعه‌ای از مستندات، فایل‌های طراحی سخت‌افزار، نمونه‌کدها و منابع توسعه CH585 را گردآوری می‌کند. محتوای مخزن شامل دیتاشیت و مستندات فنی، بسته توسعه EVT شرکت WCH، پروژه نمونه صفحه‌کلید لمسی خازنی و تصاویر راهنما است.

## ویژگی‌ها و مشخصات اصلی

- هسته پردازنده **RISC-V3C** از خانواده QingKe
- پشتیبانی از مجموعه دستورالعمل‌های **RV32IMBC** و دستورالعمل‌های توسعه‌یافته اختصاصی
- حافظه داخلی **128KB SRAM** و **512KB Flash**
- پشتیبانی از روش‌های برنامه‌ریزی و به‌روزرسانی **ICP، ISP و IAP** و به‌روزرسانی بی‌سیم **OTA**
- فرستنده/گیرنده رادیویی 2.4GHz به همراه بخش Baseband و کنترل پیوند ارتباطی
- پشتیبانی از **Bluetooth Low Energy 5.4** با نرخ‌های انتقال داده 1Mbps و 2Mbps
- حساسیت گیرندگی تا **‎-95dBm** و توان ارسال قابل برنامه‌ریزی تا **‎+4.5dBm**
- پشتیبانی از نرخ Polling تا **8kHz** در حالت ارتباطی 2.4GHz
- کنترل‌کننده و فرستنده/گیرنده داخلی **USB 2.0** با سرعت High-Speed برابر 480Mbps و Full-Speed؛ پشتیبانی از حالت Host و Device
- رابط ارتباط بی‌سیم **NFC**
- کنترل‌کننده LCD سگمنتی با پشتیبانی از نمایشگرهایی تا 112 نقطه (28×4)
- رابط نمایشگر ماتریسی LED با پشتیبانی از 1، 2، 4 یا 8 خط داده
- چهار رابط **UART**، دوازده کانال **PWM**، دو رابط **SPI** و یک رابط **I²C**
- چهارده کانال تشخیص کلید لمسی (**TouchKey**) و چهارده کانال مبدل **ADC دوازده‌بیتی**
- دارای **40 پایه GPIO** که دو پایه از آن‌ها قابلیت دریافت سیگنال ورودی 5V را دارند
- حداقل ولتاژ تغذیه **1.7V**
- حسگر دمای داخلی و واحد ساعت بلادرنگ **RTC**
- سخت‌افزار رمزنگاری و رمزگشایی **AES-128** و شناسه منحصربه‌فرد تراشه (Chip ID)
- گزینه‌های پکیج: **QFN48T، QFN32، QFN26C3 و QFN20**

## نمودار بلوکی و راهنمای انتخاب محصول

<p align="center">
  <img src="./image/CH585.jpg" width="90%" alt="CH585 Block Diagram">
</p>

<p align="center">
  <img src="./image/SelectionGuide.jpg" width="90%" alt="CH585 and CH584 Product Selection Guide">
</p>

تراشه **CH584** نسخه ساده‌شده‌ای از CH585 است. در این مدل، یک مجموعه USBHS و رابط SPI1 حذف شده و ظرفیت حافظه RAM به **96KB** کاهش یافته است. برای انتخاب قطعه و بررسی تفاوت‌های دقیق، به دیتاشیت رسمی مراجعه کنید.

---

## ساختار مخزن و منابع

### ۱. پروژه کاربردی | Application

پوشه [Application](./Application/) شامل پروژه‌های کاربردی مبتنی بر CH585 است.

#### صفحه‌کلید لمسی خازنی | Capacitive Touch Keyboard

<p align="center">
  <a href="./Application/CapacitiveTouchKeyboard/">
    <img src="./Application/CapacitiveTouchKeyboard/image/Layout_v2.0.jpg" width="85%" alt="Capacitive Touch Keyboard v2.0 PCB Layout">
  </a>
</p>

پروژه **Capacitive Touch Keyboard** یک نمونه عملی از به‌کارگیری قابلیت TouchKey در CH585M است که عملکرد صفحه‌کلید لمسی خازنی را همراه با ارتباط BLE و قابلیت NFC پیاده‌سازی می‌کند. نسخه سخت‌افزاری 2.0 و Firmware نسخه 2.2 در این مجموعه ارائه شده‌اند.

- [راهنمای کامل پروژه و توضیحات فنی (README)](./Application/CapacitiveTouchKeyboard/README.md)
- [فایل‌های طراحی سخت‌افزار و PCB](./Application/CapacitiveTouchKeyboard/hardware/)
  - **CapTouchKeyboard_v1.1**: نسخه اولیه طراحی
  - **CapTouchKeyboard_v2.0**: نسخه بازنگری‌شده مبتنی بر CH585M؛ شامل فایل‌های شماتیک و PCB آلتیوم و خروجی PDF
- [پروژه‌های نرم‌افزاری](./Application/CapacitiveTouchKeyboard/software/)
  - **CapTouchKeyboard_V1.0**
  - **CapTouchKeyboard_v2.2**: نمونه نرم‌افزاری با پشتیبانی از صفحه‌کلید BLE HID و NFC
- [تصاویر، شماتیک و دیاگرام‌های پروژه](./Application/CapacitiveTouchKeyboard/image/)

در طراحی این صفحه‌کلید از ساختار ماتریسی برای تشخیص کلیدها استفاده شده است. راهنمای پروژه شامل اصول عملکرد تشخیص خازنی، نکات طراحی PCB، ساختار نرم‌افزار و مراحل پروگرام‌کردن CH585 با ابزار WCHISPTool است.

### ۲. بسته توسعه و مثال‌ها | EVT

پوشه [EVT](./EVT/) شامل بسته توسعه و مثال‌های نرم‌افزاری ارائه‌شده توسط WCH برای میکروکنترلر CH585 است.

| مسیر | محتوا |
|---|---|
| [EVT/EXAM](./EVT/EXAM/) | مثال‌های نرم‌افزاری و پروژه‌های نمونه |
| [EVT/EXAM/ADC](./EVT/EXAM/ADC/) | نمونه‌های ADC، اندازه‌گیری و کاربردهای مرتبط با TouchKey |
| [EVT/EXAM/BLE](./EVT/EXAM/BLE/) | مثال‌های Bluetooth Low Energy و ارتباط 2.4GHz |
| [EVT/EXAM/FLASH](./EVT/EXAM/FLASH/) | خواندن، نوشتن و پاک‌کردن حافظه Flash |
| [EVT/EXAM/FreeRTOS](./EVT/EXAM/FreeRTOS/) | نمونه راه‌اندازی FreeRTOS |
| [EVT/EXAM/HarmonyOS](./EVT/EXAM/HarmonyOS/) | نمونه‌های مرتبط با HarmonyOS |
| [EVT/EXAM/I2C](./EVT/EXAM/I2C/) | ارتباط I²C در حالت Master و Slave |
| [EVT/EXAM/IAP](./EVT/EXAM/IAP/) | به‌روزرسانی برنامه از طریق USB، USBHS و UART |
| [EVT/EXAM/LCD](./EVT/EXAM/LCD/) و [LED](./EVT/EXAM/LED/) | راه‌اندازی نمایشگرهای LCD و LED |
| [EVT/EXAM/NFCA](./EVT/EXAM/NFCA/) | مثال‌ها و کتابخانه‌های NFC-A |
| [EVT/EXAM/PM](./EVT/EXAM/PM/) | حالت‌های کم‌مصرف و روش‌های بیدارشدن |
| [EVT/EXAM/PWMX](./EVT/EXAM/PWMX/) | خروجی PWM |
| [EVT/EXAM/RT-Thread](./EVT/EXAM/RT-Thread/) | نمونه راه‌اندازی RT-Thread |
| [EVT/EXAM/SPI](./EVT/EXAM/SPI/) | ارتباط SPI در حالت Master و Slave |
| [EVT/EXAM/TMR](./EVT/EXAM/TMR/) | مثال‌های Timer |
| [EVT/EXAM/TOUCH](./EVT/EXAM/TOUCH/) | مثال‌های تشخیص لمسی، TouchKey و کتابخانه مربوطه |
| [EVT/EXAM/UART1](./EVT/EXAM/UART1/) | ارسال و دریافت داده از طریق UART |
| [EVT/EXAM/USB](./EVT/EXAM/USB/) | مثال‌های USB در حالت Host و Device و USB High-Speed |

پوشه [EVT/SRC](./EVT/EXAM/SRC/) شامل فایل‌های پایه نرم‌افزار، فایل‌های راه‌اندازی، Linker و درایورهای تجهیزات جانبی است که در پروژه‌های نمونه استفاده می‌شوند.

#### مستندات و فایل‌های سخت‌افزاری برد ارزیابی

پوشه [EVT/PUB](./EVT/PUB/) شامل منابع منتشرشده مربوط به برد ارزیابی CH585 است:

- [شماتیک برد ارزیابی CH585 (PDF)](./EVT/PUB/CH585SCH.pdf)
- [راهنمای برد ارزیابی CH585 (نسخه چینی، PDF)](./EVT/PUB/CH585评估板说明书.pdf)
- [نکات مهم طراحی مدار و PCB تراشه‌های Bluetooth (نسخه چینی، PDF)](./EVT/PUB/蓝牙芯片的电路及PCB设计的重要注意事项.pdf)
- [فایل‌های شماتیک و PCB برد CH585D-DG-R0](./EVT/PUB/SCHPCB/CH585D-DG-R0/)
- [فایل‌های شماتیک و PCB برد CH585M-R1](./EVT/PUB/SCHPCB/CH585M-R1/)

فایل‌های طراحی سخت‌افزار با فرمت‌های **SchDoc** و **PcbDoc** ارائه شده‌اند و برای مشاهده و ویرایش آن‌ها می‌توان از **Altium Designer** استفاده کرد.

### ۳. دیتاشیت و مستندات فنی | Datasheet

پوشه [Datasheet](./Datasheet/) شامل دیتاشیت و مستندات فنی CH585 است.

| سند | توضیحات |
|---|---|
| [CH585DS1_EN.PDF](./Datasheet/CH585DS1_EN.PDF) | دیتاشیت CH585 به زبان انگلیسی |
| [CH585DS1_zh.PDF](./Datasheet/CH585DS1_zh.PDF) | دیتاشیت CH585 به زبان چینی |
| [WCH BLE Software Development Reference Manual.pdf](./Datasheet/WCH%20BLE%20Software%20Development%20Reference%20Manual.pdf) | راهنمای مرجع توسعه نرم‌افزار BLE شرکت WCH |

برای طراحی سخت‌افزار، انتخاب پایه‌ها، بررسی مشخصات الکتریکی و محدودیت‌های عملکردی، دیتاشیت رسمی را مرجع اصلی قرار دهید. برای توسعه نرم‌افزار BLE نیز از راهنمای مرجع و مثال‌های مرتبط در EVT استفاده کنید.

### ۴. تصاویر و دیاگرام‌ها | image

پوشه [image](./image/) شامل تصاویر عمومی مورد استفاده در README است:

- [CH585.jpg](./image/CH585.jpg): نمودار بلوکی میکروکنترلر CH585
- [SelectionGuide.jpg](./image/SelectionGuide.jpg): راهنمای انتخاب و مقایسه محصولات CH585 و CH584

تصاویر اختصاصی پروژه صفحه‌کلید لمسی خازنی در مسیر [Application/CapacitiveTouchKeyboard/image](./Application/CapacitiveTouchKeyboard/image/) قرار دارند.

## شروع کار

برای شروع توسعه با CH585، مسیر پیشنهادی زیر را دنبال کنید:

1. دیتاشیت CH585 را از پوشه [Datasheet](./Datasheet/) دریافت و مشخصات قطعه و پکیج موردنظر را بررسی کنید.
2. بسته توسعه و مثال متناسب با واحد جانبی موردنظر را از پوشه [EVT/EXAM](./EVT/EXAM/) انتخاب کنید.
3. پروژه را در محیط توسعه سازگار با ابزارهای WCH، مانند **MounRiver Studio**، باز کنید.
4. برای پروگرام و عیب‌یابی، از ابزارها و روش‌های معرفی‌شده در مستندات WCH و مثال‌های EVT استفاده کنید.
5. برای آشنایی با کاربرد عملی TouchKey، ارتباط BLE و NFC، پروژه [Capacitive Touch Keyboard](./Application/CapacitiveTouchKeyboard/README.md) را مطالعه کنید.

> **نکته:** پیش از استفاده از هر مثال، تنظیمات کلاک، پایه‌ها، پکیج تراشه و وابستگی‌های نرم‌افزاری آن را با سخت‌افزار واقعی خود تطبیق دهید. همه پایه‌ها و قابلیت‌ها لزوماً در تمام پکیج‌های خانواده در دسترس نیستند.

---

## تصاویر و دیاگرام‌های راهنما

<p align="center">
  <img src="Images/GitHub-Assets/MES-Section-Header.svg" width="100%" alt="MES Technical Resources">
</p>

برای مشاهده سایر تصاویر، دیاگرام‌ها و عناصر گرافیکی مورد استفاده در مستندات، به [پوشه GitHub-Assets](./Images/GitHub-Assets/) مراجعه کنید.

<p align="center">
  <img src="Images/GitHub-Assets/MES-Divider.svg" width="100%" alt="MES Divider">
</p>

## تهیه و تدوین

**معمار الکترونیک صنعت**  
**MEMAR ELECTRONIC SANAT (MES)**

همراه شما در مسیر طراحی و ساخت مدارهای مطمئن

- کانال تلگرام: [https://t.me/Memar_Electronic](https://t.me/Memar_Electronic)
- پیج اینستاگرام: [https://www.instagram.com/Memar.Electronic](https://www.instagram.com/Memar.Electronic)

[مشاهده سایر آموزش‌ها](https://github.com/MEMAR-ELECTRONIC-SANAT)

<p align="center">
  <img src="Images/GitHub-Assets/MES-Thank-You-Footer.svg" width="100%" alt="Thank you for visiting MES">
</p>

</div>

---

# CH585 Microcontroller | RISC-V Core, BLE 5.4, USB 2.0 and NFC

<p align="center">
  <img src="Images/GitHub-Assets/MES-Hero-Banner.svg" width="100%" alt="MEMAR ELECTRONIC SANAT — MES">
</p>

## Overview

The **CH585**, manufactured by **WCH**, is a 32-bit RISC-V microcontroller based on the QingKe processor family. It integrates processing, wireless connectivity and peripheral-control capabilities for embedded products, smart devices, wireless interfaces, USB applications and BLE/NFC-enabled designs.

The CH585 supports **Bluetooth Low Energy 5.4**, proprietary 2.4GHz communication, **USB 2.0 High-Speed (480Mbps)** and Full-Speed, **NFC**, capacitive touch-key detection, ADC, PWM and common serial interfaces.

This repository collects technical documentation, hardware design resources, software examples and development materials for the CH585. It includes datasheets, WCH's EVT package, a capacitive touch keyboard reference project and supporting images.

## Main Features and Specifications

- **RISC-V3C** QingKe 32-bit processor core
- **RV32IMBC** instruction set and proprietary extended instructions
- **128KB SRAM** and **512KB Flash**
- **ICP, ISP and IAP** programming/update methods, plus wireless **OTA** updates
- Integrated 2.4GHz RF transceiver, baseband and link-layer controller
- **Bluetooth Low Energy 5.4**, supporting 1Mbps and 2Mbps data rates
- Receiver sensitivity down to **-95dBm** and programmable transmit power up to **+4.5dBm**
- Polling rates up to **8kHz** in 2.4GHz communication mode
- Integrated **USB 2.0** controller and transceiver, with 480Mbps High-Speed and Full-Speed; Host and Device modes
- **NFC** wireless interface
- Segment LCD controller supporting up to 112 points (28×4)
- LED matrix display interface with 1, 2, 4 or 8 data lines
- Four **UART** interfaces, twelve **PWM** channels, two **SPI** interfaces and one **I²C** interface
- Fourteen capacitive **TouchKey** channels and fourteen 12-bit **ADC** channels
- **40 GPIO pins**, including two pins capable of accepting 5V input signals
- Minimum operating supply voltage of **1.7V**
- Internal temperature sensor and **RTC**
- **AES-128** hardware encryption/decryption and unique Chip ID
- Package options: **QFN48T, QFN32, QFN26C3 and QFN20**

## Block Diagram and Product Selection Guide

<p align="center">
  <img src="./image/CH585.jpg" width="90%" alt="CH585 Block Diagram">
</p>

<p align="center">
  <img src="./image/SelectionGuide.jpg" width="90%" alt="CH585 and CH584 Product Selection Guide">
</p>

The **CH584** is a simplified version of the CH585. It omits one USBHS block and the SPI1 interface, and its RAM capacity is reduced to **96KB**. Refer to the official datasheets for detailed device selection and specifications.

---

## Repository Structure and Resources

### 1. Application

The [Application](./Application/) directory contains application-level projects based on the CH585.

#### Capacitive Touch Keyboard

<p align="center">
  <a href="./Application/CapacitiveTouchKeyboard/">
    <img src="./Application/CapacitiveTouchKeyboard/image/Layout_v2.0.jpg" width="85%" alt="Capacitive Touch Keyboard v2.0 PCB Layout">
  </a>
</p>

The **Capacitive Touch Keyboard** is a practical example of the CH585M TouchKey peripheral. It implements a capacitive keyboard with BLE connectivity and NFC functionality. The repository provides hardware revision 2.0 and Firmware version 2.2.

- [Complete project guide and technical documentation (README)](./Application/CapacitiveTouchKeyboard/README.md)
- [Hardware design files and PCB layouts](./Application/CapacitiveTouchKeyboard/hardware/)
  - **CapTouchKeyboard_v1.1**: Initial hardware revision
  - **CapTouchKeyboard_v2.0**: Revised CH585M-based design, including Altium schematic, PCB and PDF files
- [Software projects](./Application/CapacitiveTouchKeyboard/software/)
  - **CapTouchKeyboard_V1.0**
  - **CapTouchKeyboard_v2.2**: BLE HID keyboard and NFC-enabled software example
- [Project images, schematics and diagrams](./Application/CapacitiveTouchKeyboard/image/)

The keyboard uses a matrix-based approach for touch-key detection. Its project guide explains capacitive sensing principles, PCB layout recommendations, software organization and CH585 programming through WCHISPTool.

### 2. EVT Package and Examples

The [EVT](./EVT/) directory contains WCH's development package and software examples for the CH585.

| Path | Contents |
|---|---|
| [EVT/EXAM](./EVT/EXAM/) | Software examples and reference projects |
| [EVT/EXAM/ADC](./EVT/EXAM/ADC/) | ADC sampling, measurement and TouchKey-related examples |
| [EVT/EXAM/BLE](./EVT/EXAM/BLE/) | Bluetooth Low Energy and 2.4GHz examples |
| [EVT/EXAM/FLASH](./EVT/EXAM/FLASH/) | On-chip Flash read, write and erase examples |
| [EVT/EXAM/FreeRTOS](./EVT/EXAM/FreeRTOS/) | FreeRTOS porting example |
| [EVT/EXAM/HarmonyOS](./EVT/EXAM/HarmonyOS/) | HarmonyOS-related example |
| [EVT/EXAM/I2C](./EVT/EXAM/I2C/) | I²C Master and Slave communication |
| [EVT/EXAM/IAP](./EVT/EXAM/IAP/) | Firmware update over USB, USBHS and UART |
| [EVT/EXAM/LCD](./EVT/EXAM/LCD/) and [LED](./EVT/EXAM/LED/) | LCD and LED display examples |
| [EVT/EXAM/NFCA](./EVT/EXAM/NFCA/) | NFC-A examples and libraries |
| [EVT/EXAM/PM](./EVT/EXAM/PM/) | Low-power modes and wake-up examples |
| [EVT/EXAM/PWMX](./EVT/EXAM/PWMX/) | PWM output examples |
| [EVT/EXAM/RT-Thread](./EVT/EXAM/RT-Thread/) | RT-Thread porting example |
| [EVT/EXAM/SPI](./EVT/EXAM/SPI/) | SPI Master and Slave communication |
| [EVT/EXAM/TMR](./EVT/EXAM/TMR/) | Timer examples |
| [EVT/EXAM/TOUCH](./EVT/EXAM/TOUCH/) | Touch sensing, TouchKey examples and related library |
| [EVT/EXAM/UART1](./EVT/EXAM/UART1/) | UART data transmission and reception |
| [EVT/EXAM/USB](./EVT/EXAM/USB/) | USB Host, Device and USB High-Speed examples |

The [EVT/EXAM/SRC](./EVT/EXAM/SRC/) directory contains common software files, startup code, linker files and peripheral driver sources used by the example projects.

#### Evaluation Board Documentation and Hardware Design Files

The [EVT/PUB](./EVT/PUB/) directory contains published resources for the CH585 evaluation board:

- [CH585 Evaluation Board Schematic (PDF)](./EVT/PUB/CH585SCH.pdf)
- [CH585 Evaluation Board User Manual (Chinese, PDF)](./EVT/PUB/CH585评估板说明书.pdf)
- [Important PCB and Circuit Design Notes for Bluetooth Chips (Chinese, PDF)](./EVT/PUB/蓝牙芯片的电路及PCB设计的重要注意事项.pdf)
- [CH585D-DG-R0 schematic and PCB files](./EVT/PUB/SCHPCB/CH585D-DG-R0/)
- [CH585M-R1 schematic and PCB files](./EVT/PUB/SCHPCB/CH585M-R1/)

The hardware design files are provided in **SchDoc** and **PcbDoc** formats and can be viewed or edited using **Altium Designer**.

### 3. Datasheets and Technical Documentation

The [Datasheet](./Datasheet/) directory contains the CH585 datasheets and technical reference documentation.

| Document | Description |
|---|---|
| [CH585DS1_EN.PDF](./Datasheet/CH585DS1_EN.PDF) | CH585 datasheet in English |
| [CH585DS1_zh.PDF](./Datasheet/CH585DS1_zh.PDF) | CH585 datasheet in Chinese |
| [WCH BLE Software Development Reference Manual.pdf](./Datasheet/WCH%20BLE%20Software%20Development%20Reference%20Manual.pdf) | WCH BLE software development reference manual |

Use the official datasheet as the primary reference for hardware design, pin selection, electrical characteristics and device limitations. For BLE software development, refer to the software reference manual and the corresponding EVT examples.

### 4. Images and Diagrams

The [image](./image/) directory contains the general images used in this README:

- [CH585.jpg](./image/CH585.jpg): CH585 microcontroller block diagram
- [SelectionGuide.jpg](./image/SelectionGuide.jpg): CH585 and CH584 product selection guide

Images specific to the capacitive touch keyboard project are available in [Application/CapacitiveTouchKeyboard/image](./Application/CapacitiveTouchKeyboard/image/).

## Getting Started

A recommended workflow for starting CH585 development:

1. Download the CH585 datasheet from [Datasheet](./Datasheet/) and review the specifications and target package.
2. Select the relevant peripheral example from [EVT/EXAM](./EVT/EXAM/).
3. Open the project in a development environment compatible with WCH tools, such as **MounRiver Studio**.
4. Follow WCH documentation and the EVT examples for programming and debugging.
5. To explore a practical implementation of TouchKey, BLE and NFC, review the [Capacitive Touch Keyboard project](./Application/CapacitiveTouchKeyboard/README.md).

> **Note:** Before using an example, verify its clock configuration, pin assignments, device package and software dependencies against your target hardware. Not all pins and peripherals are available in every package.

---

## Images and Reference Diagrams

<p align="center">
  <img src="Images/GitHub-Assets/MES-Section-Header.svg" width="100%" alt="MES Technical Resources">
</p>

For additional images, diagrams and graphical assets used in the documentation, visit the [GitHub-Assets directory](./Images/GitHub-Assets/).

<p align="center">
  <img src="Images/GitHub-Assets/MES-Divider.svg" width="100%" alt="MES Divider">
</p>

## Credits and Documentation

**MEMAR ELECTRONIC SANAT (MES)**

*Your partner in designing and building reliable circuits.*

- Telegram: [https://t.me/Memar_Electronic](https://t.me/Memar_Electronic)
- Instagram: [https://www.instagram.com/Memar.Electronic](https://www.instagram.com/Memar.Electronic)

[Explore more tutorials](https://github.com/MEMAR-ELECTRONIC-SANAT)

<p align="center">
  <img src="Images/GitHub-Assets/MES-Thank-You-Footer.svg" width="100%" alt="Thank you for visiting MES">
</p>

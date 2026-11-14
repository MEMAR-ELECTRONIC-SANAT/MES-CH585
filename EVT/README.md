<div dir="rtl" align="right">

# بسته توسعه و مثال‌های نرم‌افزاری CH585 | WCH EVT

## معرفی

این پوشه شامل بسته توسعه **EVT (Evaluation and Verification Toolkit)** و مجموعه مثال‌های نرم‌افزاری شرکت **WCH** برای میکروکنترلر **CH585** است. منابع موجود، نمونه‌هایی برای آشنایی با واحدهای جانبی، قابلیت‌های ارتباطی، مدیریت توان، حافظه، رابط‌های USB و BLE و همچنین فایل‌های پایه موردنیاز برای توسعه نرم‌افزار را در اختیار توسعه‌دهنده قرار می‌دهند.

محتوای این پوشه بر اساس ساختار بسته اصلی WCH نگهداری شده است. برای مشاهده فهرست تفصیلی و توضیحات ارائه‌شده توسط سازنده، از فایل‌های زیر استفاده کنید:

- [فهرست بسته EVT – نسخه انگلیسی](./CH585_List_EN.txt)
- [فهرست بسته EVT – نسخه چینی](./CH585_List.txt)

> **توجه:** توضیحات این README راهنمای مسیریابی در فایل‌های مخزن است. برای جزئیات پیاده‌سازی، تنظیمات، محدودیت‌ها و روش استفاده از هر مثال، فایل‌های راهنما و توضیحات همراه همان مثال را بررسی کنید.

## ساختار پوشه‌ها

| مسیر | شرح |
|---|---|
| [EXAM](./EXAM/) | مثال‌های نرم‌افزاری و پروژه‌های مرجع CH585 |
| [PUB](./PUB/) | مستندات عمومی، شماتیک و فایل‌های طراحی برد ارزیابی |

---

## ۱. مثال‌های نرم‌افزاری | EXAM

پوشه [EXAM](./EXAM/) مجموعه مثال‌های کاربردی CH585 را در بر می‌گیرد. هر زیرپوشه معمولاً شامل یک یا چند پروژه نمونه، فایل‌های سورس و تنظیمات مربوط به همان قابلیت است.

| زیرپوشه | موضوع و کاربرد |
|---|---|
| [ADC](./EXAM/ADC/) | نمونه‌های نمونه‌برداری ADC، اندازه‌گیری دما، ورودی تک‌کاناله و تفاضلی، نمونه‌برداری وقفه‌ای و کاربردهای مرتبط با TouchKey |
| [BLE](./EXAM/BLE/) | مثال‌های Bluetooth Low Energy و ارتباط رادیویی 2.4GHz؛ شامل نقش‌های Central و Peripheral، BLE HID، سنسورها، ارتباط چندگانه، Mesh، OTA و نمونه‌های RF |
| [FLASH](./EXAM/FLASH/) | عملیات پاک‌کردن، خواندن و نوشتن حافظه Flash داخلی، شامل ناحیه کد و DataFlash |
| [FreeRTOS](./EXAM/FreeRTOS/) | نمونه راه‌اندازی و استفاده از سیستم‌عامل بلادرنگ FreeRTOS |
| [HarmonyOS](./EXAM/HarmonyOS/) | نمونه و منابع پورت‌کردن یا کار با HarmonyOS |
| [I2C](./EXAM/I2C/) | ارتباط I²C در حالت‌های Master و Slave |
| [IAP](./EXAM/IAP/) | به‌روزرسانی برنامه از طریق USB، USB High-Speed و UART؛ به همراه ابزار و برنامه‌های مرتبط |
| [LCD](./EXAM/LCD/) | نمونه‌های راه‌اندازی و کنترل LCD، از جمله نمایش و حالت خواب |
| [LED](./EXAM/LED/) | نمونه رابط کنترل نمایشگرهای LED |
| [NFCA](./EXAM/NFCA/) | مثال‌های NFC-A شامل حالت کارت‌خوان (PCD)، شبیه‌سازی نرم‌افزاری کارت‌خوان و حالت کارت (PICC)؛ همراه با کتابخانه‌ها و نمونه‌های Mifare Classic و Type 2 Tag |
| [PM](./EXAM/PM/) | حالت‌های کم‌مصرف، خواب سیستم و روش‌های بیدارشدن |
| [PWMX](./EXAM/PWMX/) | مثال‌های تولید خروجی PWM |
| [RT-Thread](./EXAM/RT-Thread/) | نمونه راه‌اندازی و استفاده از RT-Thread |
| [SPI](./EXAM/SPI/) | ارتباط SPI در حالت‌های Master و Slave |
| [SRC](./EXAM/SRC/) | فایل‌های پایه و مشترک مورد استفاده پروژه‌ها؛ شامل فایل‌های Linker، هدرهای هسته، Startup و درایورهای استاندارد جانبی |
| [TMR](./EXAM/TMR/) | مثال‌های مربوط به Timer و زمان‌سنجی |
| [TOUCH](./EXAM/TOUCH/) | کتابخانه تشخیص لمسی و مثال‌های TouchKey؛ شامل کلید لمسی، اسلایدر، حلقه لمسی و تشخیص مجاورت، با و بدون ارتباط BLE |
| [UART1](./EXAM/UART1/) | مثال‌های ارسال و دریافت داده از طریق UART1 |
| [USB](./EXAM/USB/) | مثال‌های USB در حالت Device و Host و همچنین USB High-Speed؛ شامل CDC، HID، دستگاه ترکیبی، USB Storage و کاربردهای میزبان |

### ساختار منابع پایه | EXAM/SRC

پوشه [EXAM/SRC](./EXAM/SRC/) شامل اجزای پایه‌ای است که پروژه‌های نمونه از آن‌ها استفاده می‌کنند:

| مسیر | کاربرد |
|---|---|
| [Ld](./EXAM/SRC/Ld/) | فایل‌های Linker و تعریف نواحی حافظه |
| [RVMSIS](./EXAM/SRC/RVMSIS/) | فایل‌های هدر و منابع مرتبط با هسته RISC-V و CMSIS |
| [Startup](./EXAM/SRC/Startup/) | فایل‌های راه‌اندازی اولیه میکروکنترلر |
| [StdPeriphDriver](./EXAM/SRC/StdPeriphDriver/) | فایل‌های سورس و هدر درایورهای پایه واحدهای جانبی |

### راهنمای انتخاب مثال

- برای شروع کار با GPIO و واحدهای جانبی، مثال‌های مرتبط با ADC، PWMX، TMR، UART1، I2C و SPI را بررسی کنید.
- برای توسعه محصولات بی‌سیم، ابتدا مثال‌های BLE را با توجه به نقش موردنیاز (Central، Peripheral یا هر دو) مطالعه کنید.
- برای طراحی رابط کاربری لمسی، پوشه TOUCH و سپس پروژه کاربردی [Capacitive Touch Keyboard](../Application/CapacitiveTouchKeyboard/) را ببینید.
- برای توسعه تجهیزات USB، مثال‌های USB Device، USB Host و USBHS را متناسب با نقش و سرعت موردنیاز بررسی کنید.
- برای پیاده‌سازی به‌روزرسانی Firmware، مثال‌های IAP و BLE OTA را مطالعه کنید.
- برای کاهش مصرف انرژی، از مثال‌های PM و نمونه‌های کم‌مصرف BLE شروع کنید.

---

## ۲. مستندات و فایل‌های سخت‌افزاری | PUB

پوشه [PUB](./PUB/) شامل مستندات و منابع سخت‌افزاری منتشرشده برای CH585 و بردهای ارزیابی آن است.

### مستندات PDF

| فایل | توضیحات |
|---|---|
| [CH585SCH.pdf](./PUB/CH585SCH.pdf) | شماتیک برد ارزیابی CH585 |
| [CH585评估板说明书.pdf](./PUB/CH585评估板说明书.pdf) | راهنمای برد ارزیابی CH585 به زبان چینی |
| [蓝牙芯片的电路及PCB设计的重要注意事项.pdf](./PUB/蓝牙芯片的电路及PCB设计的重要注意事项.pdf) | نکات مهم طراحی مدار و PCB برای تراشه‌های Bluetooth به زبان چینی |

### فایل‌های شماتیک و PCB

فایل‌های طراحی بردهای ارزیابی در مسیر [PUB/SCHPCB](./PUB/SCHPCB/) قرار دارند:

| پوشه | فایل‌ها و توضیحات |
|---|---|
| [CH585D-DG-R0](./PUB/SCHPCB/CH585D-DG-R0/) | شماتیک `CH585D-DG-R0.SchDoc` و PCB `CH585D-DG-R0-1v0.PcbDoc` |
| [CH585M-R1](./PUB/SCHPCB/CH585M-R1/) | شماتیک `CH585M-R1.SchDoc` و PCB `CH585M-R1-1v1.PcbDoc` |

فایل‌های `SchDoc` و `PcbDoc` با نرم‌افزار **Altium Designer** قابل مشاهده و ویرایش هستند.

---

## ۳. روش استفاده از مثال‌ها

برای استفاده از پروژه‌های EVT، مراحل زیر را دنبال کنید:

1. دیتاشیت CH585 را مطالعه کنید و از سازگاری قابلیت موردنظر با مدل و پکیج تراشه اطمینان حاصل کنید.
2. مثال مرتبط را از پوشه [EXAM](./EXAM/) انتخاب کنید.
3. فایل‌های پروژه و راهنمای موجود در همان زیرپوشه را بررسی کنید.
4. پروژه را با محیط توسعه و ابزارهای سازگار با بسته WCH، مانند **MounRiver Studio**، باز کنید. نوع پروژه و فایل‌های تنظیمات آن را در نظر بگیرید.
5. پیش از کامپایل و پروگرام، کلاک، پایه‌های GPIO، تنظیمات حافظه، فایل Linker و وابستگی‌های کتابخانه‌ای را با سخت‌افزار خود تطبیق دهید.
6. ابتدا مثال را بدون تغییر روی برد ارزیابی یا سخت‌افزار مرجع اجرا کنید؛ سپس تغییرات موردنیاز محصول خود را مرحله‌به‌مرحله اعمال کنید.

### نکات مهم

- مثال‌های EVT برای آشنایی و ارزیابی قابلیت‌های تراشه ارائه شده‌اند و لزوماً بدون تغییر برای هر طراحی سخت‌افزاری آماده استفاده در محصول نهایی نیستند.
- تخصیص پایه‌ها، کلاک، تغذیه، اتصالات RF و تنظیمات USB باید با شماتیک و دیتاشیت قطعه مورد استفاده مطابقت داشته باشند.
- برخی مثال‌ها به برد ارزیابی، تجهیزات جانبی، ابزار میزبان یا مثال مکمل نیاز دارند؛ توضیحات داخل پروژه را بررسی کنید.
- در پروژه‌های BLE و RF، تنظیمات آنتن، تطبیق امپدانس و طراحی PCB بر عملکرد ارتباط بی‌سیم اثر مستقیم دارند.
- پیش از استفاده از فایل‌های کتابخانه‌ای و کدهای آماده در محصول تجاری، شرایط مجوز و محدودیت‌های اعلام‌شده توسط WCH را بررسی کنید.

## منابع مرتبط در همین مخزن

- [README اصلی پروژه CH585](../README.md)
- [دیتاشیت و مستندات فنی CH585](../Datasheet/)
- [پروژه صفحه‌کلید لمسی خازنی](../Application/CapacitiveTouchKeyboard/)
- [فهرست EVT به زبان انگلیسی](./CH585_List_EN.txt)
- [فهرست EVT به زبان چینی](./CH585_List.txt)

---

## تصاویر و دیاگرام‌های راهنما

<p align="center">
  <img src="../Images/GitHub-Assets/MES-Section-Header.svg" width="100%" alt="MES Technical Resources">
</p>

برای مشاهده سایر عناصر گرافیکی و منابع تصویری مورد استفاده در مستندات MES، به [پوشه GitHub-Assets](../Images/GitHub-Assets/) مراجعه کنید.

<p align="center">
  <img src="../Images/GitHub-Assets/MES-Divider.svg" width="100%" alt="MES Divider">
</p>

## تهیه و تدوین

**معمار الکترونیک صنعت**  
**MEMAR ELECTRONIC SANAT (MES)**

همراه شما در مسیر طراحی و ساخت مدارهای مطمئن

- تلگرام: [https://t.me/Memar_Electronic](https://t.me/Memar_Electronic)
- اینستاگرام: [https://www.instagram.com/Memar.Electronic](https://www.instagram.com/Memar.Electronic)

[مشاهده سایر آموزش‌ها](https://github.com/MEMAR-ELECTRONIC-SANAT)

<p align="center">
  <img src="../Images/GitHub-Assets/MES-Thank-You-Footer.svg" width="100%" alt="Thank you for visiting MES">
</p>

</div>

---

# CH585 EVT Development Package and Software Examples

## Overview

This directory contains the **EVT (Evaluation and Verification Toolkit)** and software examples provided by **WCH** for the **CH585** microcontroller. The package includes reference projects covering peripheral interfaces, wireless connectivity, power management, memory operations, USB, BLE and the common software resources required for application development.

The original WCH package directory structure is preserved. For the vendor's detailed directory descriptions, refer to:

- [EVT package directory list – English](./CH585_List_EN.txt)
- [EVT package directory list – Chinese](./CH585_List.txt)

> **Note:** This README is a navigation guide to the repository contents. For implementation details, configuration requirements, limitations and usage instructions, check the documentation included with each example.

## Directory Structure

| Path | Description |
|---|---|
| [EXAM](./EXAM/) | CH585 software examples and reference projects |
| [PUB](./PUB/) | Public documentation, evaluation-board schematics and hardware design files |

---

## 1. Software Examples | EXAM

The [EXAM](./EXAM/) directory contains application examples for the CH585. Each subdirectory generally includes one or more reference projects, source files and configuration files for the corresponding feature.

| Directory | Topics and Applications |
|---|---|
| [ADC](./EXAM/ADC/) | ADC sampling, temperature measurement, single-ended and differential channels, interrupt-based sampling and TouchKey-related examples |
| [BLE](./EXAM/BLE/) | Bluetooth Low Energy and 2.4GHz examples, including Central and Peripheral roles, BLE HID, sensors, multi-connection, Mesh, OTA and RF examples |
| [FLASH](./EXAM/FLASH/) | On-chip Flash erase, read and write operations, including Code and DataFlash areas |
| [FreeRTOS](./EXAM/FreeRTOS/) | FreeRTOS porting and usage example |
| [HarmonyOS](./EXAM/HarmonyOS/) | HarmonyOS-related porting and example resources |
| [I2C](./EXAM/I2C/) | I²C communication in Master and Slave modes |
| [IAP](./EXAM/IAP/) | Firmware update over USB, USB High-Speed and UART, with related utilities and applications |
| [LCD](./EXAM/LCD/) | LCD initialization and control, including display and sleep examples |
| [LED](./EXAM/LED/) | LED display-controller interface example |
| [NFCA](./EXAM/NFCA/) | NFC-A examples for reader (PCD), software-decoded reader and card (PICC) modes, including Mifare Classic and Type 2 Tag examples |
| [PM](./EXAM/PM/) | Low-power modes, system sleep and wake-up examples |
| [PWMX](./EXAM/PWMX/) | PWM output examples |
| [RT-Thread](./EXAM/RT-Thread/) | RT-Thread porting and usage example |
| [SPI](./EXAM/SPI/) | SPI communication in Master and Slave modes |
| [SRC](./EXAM/SRC/) | Common project resources: linker files, core headers, startup files and standard peripheral drivers |
| [TMR](./EXAM/TMR/) | Timer and timing examples |
| [TOUCH](./EXAM/TOUCH/) | Touch sensing library and TouchKey examples, including touch buttons, sliders, wheels and proximity sensing, with and without BLE |
| [UART1](./EXAM/UART1/) | UART1 data transmission and reception |
| [USB](./EXAM/USB/) | USB Device, Host and USB High-Speed examples, including CDC, HID, composite devices, USB storage and host applications |

### Common Source Resources | EXAM/SRC

The [EXAM/SRC](./EXAM/SRC/) directory provides common components used by the example projects:

| Path | Description |
|---|---|
| [Ld](./EXAM/SRC/Ld/) | Linker files and memory-region definitions |
| [RVMSIS](./EXAM/SRC/RVMSIS/) | RISC-V core and CMSIS-related headers and resources |
| [Startup](./EXAM/SRC/Startup/) | MCU startup files |
| [StdPeriphDriver](./EXAM/SRC/StdPeriphDriver/) | Standard peripheral driver source and header files |

### Choosing an Example

- For peripheral development, start with ADC, PWMX, TMR, UART1, I2C and SPI examples.
- For wireless products, select BLE examples according to the required role: Central, Peripheral or combined operation.
- For touch-based user interfaces, review TOUCH and then the practical [Capacitive Touch Keyboard](../Application/CapacitiveTouchKeyboard/) project.
- For USB products, choose USB Device, USB Host or USBHS examples according to the required role and speed.
- For firmware updates, review IAP and BLE OTA examples.
- For low-power applications, start with PM and the low-power BLE examples.

---

## 2. Documentation and Hardware Design Files | PUB

The [PUB](./PUB/) directory contains published documentation and hardware resources for the CH585 and its evaluation boards.

### PDF Documentation

| File | Description |
|---|---|
| [CH585SCH.pdf](./PUB/CH585SCH.pdf) | CH585 evaluation board schematic |
| [CH585评估板说明书.pdf](./PUB/CH585评估板说明书.pdf) | CH585 evaluation board user manual (Chinese) |
| [蓝牙芯片的电路及PCB设计的重要注意事项.pdf](./PUB/蓝牙芯片的电路及PCB设计的重要注意事项.pdf) | Important circuit and PCB design considerations for Bluetooth chips (Chinese) |

### Schematic and PCB Design Files

Evaluation-board design files are available under [PUB/SCHPCB](./PUB/SCHPCB/):

| Directory | Files and Description |
|---|---|
| [CH585D-DG-R0](./PUB/SCHPCB/CH585D-DG-R0/) | Schematic: `CH585D-DG-R0.SchDoc`; PCB: `CH585D-DG-R0-1v0.PcbDoc` |
| [CH585M-R1](./PUB/SCHPCB/CH585M-R1/) | Schematic: `CH585M-R1.SchDoc`; PCB: `CH585M-R1-1v1.PcbDoc` |

The `SchDoc` and `PcbDoc` files can be viewed and edited using **Altium Designer**.

---

## 3. How to Use the Examples

A recommended workflow for working with the EVT projects:

1. Read the CH585 datasheet and confirm that the required feature is supported by your target device and package.
2. Select the relevant example from [EXAM](./EXAM/).
3. Review the project files and any documentation included in that example directory.
4. Open the project using a development environment compatible with the WCH package, such as **MounRiver Studio**. Check the project type and its configuration files.
5. Before building and programming, verify the clock settings, GPIO assignments, memory configuration, linker file and library dependencies against your hardware.
6. Run the unmodified example on an evaluation board or reference hardware first; then apply product-specific changes incrementally.

### Important Notes

- EVT examples are provided for device evaluation and learning. They may require modifications before being used in a custom production design.
- Pin assignments, clock configuration, power supply, RF connections and USB settings must match the datasheet and the actual hardware design.
- Some examples require an evaluation board, external peripherals, host-side utilities or a companion example. Check the project documentation.
- In BLE and RF designs, antenna layout, impedance matching and PCB design directly affect wireless performance.
- Before using bundled libraries or source code in a commercial product, review the license terms and restrictions specified by WCH.

## Related Resources in This Repository

- [Main CH585 project README](../README.md)
- [CH585 datasheets and technical documentation](../Datasheet/)
- [Capacitive Touch Keyboard project](../Application/CapacitiveTouchKeyboard/)
- [EVT directory list – English](./CH585_List_EN.txt)
- [EVT directory list – Chinese](./CH585_List.txt)

---

## Images and Reference Diagrams

<p align="center">
  <img src="../Images/GitHub-Assets/MES-Section-Header.svg" width="100%" alt="MES Technical Resources">
</p>

For additional graphical assets and images used in MES documentation, visit the [GitHub-Assets directory](../Images/GitHub-Assets/).

<p align="center">
  <img src="../Images/GitHub-Assets/MES-Divider.svg" width="100%" alt="MES Divider">
</p>

## Credits and Documentation

**MEMAR ELECTRONIC SANAT (MES)**

*Your partner in designing and building reliable circuits.*

- Telegram: [https://t.me/Memar_Electronic](https://t.me/Memar_Electronic)
- Instagram: [https://www.instagram.com/Memar.Electronic](https://www.instagram.com/Memar.Electronic)

[Explore more tutorials](https://github.com/MEMAR-ELECTRONIC-SANAT)

<p align="center">
  <img src="../Images/GitHub-Assets/MES-Thank-You-Footer.svg" width="100%" alt="Thank you for visiting MES">
</p>

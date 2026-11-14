<div dir="rtl" align="right">

<img src="../../Images/GitHub-Assets/MES-Section-Header.svg" alt="MES - معمار الکترونیک صنعت" width="100%">

# منابع سخت‌افزاری و مستندات طراحی CH585 | PUB

پوشه **PUB** بخشی از مجموعه منابع رسمی و فنی همراه با بسته توسعه **EVT** میکروکنترلر **WCH CH585** است. در این پوشه، مستندات مربوط به بردهای ارزیابی، شماتیک‌ها، نکات طراحی مدار و PCB و فایل‌های طراحی سخت‌افزار با نرم‌افزار **Altium Designer** نگهداری می‌شوند.

هدف این بخش، فراهم‌کردن منابع لازم برای بررسی سخت‌افزار نمونه، مطالعه مدارهای مرجع و استفاده از طراحی‌های موجود به‌عنوان نقطه شروع برای توسعه بردهای مبتنی بر CH585 است.

> **نکته:** فایل‌های این پوشه منابع مرجع هستند. پیش از استفاده در محصول نهایی، نسخه قطعه، پکیج، محدودیت‌های الکتریکی، الزامات RF و توصیه‌های دیتاشیت و مستندات به‌روز WCH را بررسی کنید.

---

## ۱. ساختار پوشه

| مسیر | شرح |
|---|---|
| `CH585SCH.pdf` | سند شماتیک مربوط به سخت‌افزار CH585 |
| `CH585评估板说明书.pdf` | راهنمای برد ارزیابی CH585 (به زبان چینی) |
| `蓝牙芯片的电路及PCB设计的重要注意事项.pdf` | نکات مهم طراحی مدار و PCB برای تراشه‌های Bluetooth (به زبان چینی) |
| `SCHPCB/` | فایل‌های شماتیک و PCB طراحی‌شده با Altium Designer |

## ۲. مستندات PDF

### ۲.۱. شماتیک CH585

[**دانلود CH585SCH.pdf**](./CH585SCH.pdf)

این فایل برای مشاهده و بررسی شماتیک سخت‌افزار مرجع CH585 در نظر گرفته شده است. هنگام مطالعه شماتیک، موارد زیر را با دیتاشیت و راهنمای طراحی سخت‌افزار تطبیق دهید:

- اتصالات تغذیه و خازن‌های بای‌پس و دیکاپلینگ
- اتصالات پایه‌های Reset و پروگرام/دیباگ
- مدار و اتصالات کریستال، در صورت استفاده
- اتصالات رابط‌های ارتباطی و پایه‌های چندمنظوره
- بخش‌های مرتبط با آنتن و مسیر RF، در صورت وجود در طراحی

### ۲.۲. راهنمای برد ارزیابی CH585

[**دانلود CH585评估板说明书.pdf**](./CH585评估板说明书.pdf)

این سند، راهنمای برد ارزیابی CH585 است و فایل آن به زبان چینی منتشر شده است. برای آشنایی با برد، امکانات سخت‌افزاری، اتصالات و نحوه استفاده از بخش‌های مختلف آن به این مستند مراجعه کنید.

### ۲.۳. نکات طراحی مدار و PCB تراشه‌های Bluetooth

[**دانلود 蓝牙芯片的电路及PCB设计的重要注意事项.pdf**](./蓝牙芯片的电路及PCB设计的重要注意事项.pdf)

این مستند به نکات مهم طراحی مدار و PCB برای تراشه‌های Bluetooth می‌پردازد و به‌ویژه هنگام طراحی بخش RF و پیاده‌سازی بردهای دارای ارتباط بی‌سیم می‌تواند مفید باشد.

در طراحی نهایی، به موارد زیر توجه ویژه داشته باشید:

- رعایت اصول طراحی مسیر RF و تطبیق امپدانس مطابق مرجع سازنده
- جانمایی صحیح آنتن و رعایت ناحیه ممنوعه مس و قطعات اطراف آنتن (Antenna Keepout)
- کوتاه و کنترل‌شده نگه‌داشتن مسیرهای RF و جلوگیری از ایجاد انشعاب‌های غیرضروری
- پیوستگی صفحه زمین (GND) و رعایت مسیر بازگشت جریان
- جانمایی مناسب خازن‌های تغذیه و قطعات تطبیق در نزدیکی پایه‌های مربوط
- توجه به اثر محفظه، کابل‌ها، باتری و قطعات مکانیکی بر عملکرد آنتن

این موارد راهنمای عمومی هستند؛ مقادیر و الزامات اجرایی باید از مستندات RF و طراحی مرجع همان قطعه استخراج شوند.

## ۳. فایل‌های شماتیک و PCB در Altium Designer

پوشه [**SCHPCB**](./SCHPCB/) شامل فایل‌های طراحی سخت‌افزار با پسوندهای بومی Altium Designer است:

- `.SchDoc` — فایل شماتیک (Schematic Document)
- `.PcbDoc` — فایل طراحی برد مدار چاپی (PCB Document)

### ۳.۱. طراحی CH585D-DG-R0

[**مشاهده پوشه CH585D-DG-R0**](./SCHPCB/CH585D-DG-R0/)

| فایل | نوع | توضیح |
|---|---|---|
| [CH585D-DG-R0.SchDoc](./SCHPCB/CH585D-DG-R0/CH585D-DG-R0.SchDoc) | SchDoc | شماتیک طراحی CH585D-DG-R0 |
| [CH585D-DG-R0-1v0.PcbDoc](./SCHPCB/CH585D-DG-R0/CH585D-DG-R0-1v0.PcbDoc) | PcbDoc | فایل PCB نسخه 1v0 |

### ۳.۲. طراحی CH585M-R1

[**مشاهده پوشه CH585M-R1**](./SCHPCB/CH585M-R1/)

| فایل | نوع | توضیح |
|---|---|---|
| [CH585M-R1.SchDoc](./SCHPCB/CH585M-R1/CH585M-R1.SchDoc) | SchDoc | شماتیک طراحی CH585M-R1 |
| [CH585M-R1-1v1.PcbDoc](./SCHPCB/CH585M-R1/CH585M-R1-1v1.PcbDoc) | PcbDoc | فایل PCB نسخه 1v1 |

**توجه:** نام‌گذاری D و M در شناسه طراحی‌ها حفظ شده است؛ از روی نام پوشه به‌تنهایی درباره تفاوت الکتریکی، پکیج یا کاربرد دو برد نتیجه‌گیری نکنید. برای تشخیص دقیق، شماتیک و مشخصات قطعه را در Altium و مستندات WCH بررسی کنید.

## ۴. روش استفاده از فایل‌های Altium

۱. فایل‌های `.SchDoc` و `.PcbDoc` موردنظر را از پوشه مربوط دانلود کنید.

۲. فایل‌ها را با نسخه سازگار **Altium Designer** باز کنید. در صورت نیاز، ابتدا هر دو فایل یک طراحی را در یک پروژه واحد قرار دهید.

۳. در صورت مشاهده قطعات یا کتابخانه‌های مفقود، مسیر کتابخانه‌ها و مدل‌های وابسته را بررسی کنید. فایل‌های موجود در این مخزن لزوماً شامل تمام کتابخانه‌های جانبی یا فایل پروژه یکپارچه نیستند.

۴. پیش از ویرایش یا ساخت PCB، تطابق شماتیک و برد، قوانین طراحی (Design Rules)، شبکه‌ها (Nets)، ابعاد، لایه‌ها و Footprint قطعات را کنترل کنید.

۵. خروجی ساخت را بدون بازبینی و تأیید مهندسی مستقیماً برای تولید ارسال نکنید. فایل‌های مرجع ممکن است با نیازهای محصول، قطعات در دسترس یا نسخه فعلی دیتاشیت متفاوت باشند.

## ۵. ملاحظات مهم در طراحی سخت‌افزار CH585

- **تغذیه:** محدوده ولتاژ مجاز و الزامات هر پایه تغذیه را از دیتاشیت CH585 استخراج کنید. خازن‌های بای‌پس را مطابق توصیه سازنده و تا حد امکان نزدیک پایه‌های تغذیه قرار دهید.
- **پروگرام و دیباگ:** اتصالات لازم برای پروگرام، دیباگ و بازیابی Firmware را در طراحی خود پیش‌بینی کنید و پایه‌های مربوط را با عملکردهای دیگر تداخل ندهید.
- **کلاک:** در صورت استفاده از کریستال یا منبع کلاک خارجی، نوع قطعه، ظرفیت بار، جانمایی و مسیرهای اتصال را با مرجع طراحی تطبیق دهید.
- **RF و آنتن:** طراحی بخش 2.4GHz به جانمایی، امپدانس مسیر، زمین، آنتن و شرایط مکانیکی وابسته است. از کپی‌کردن ابعاد یا شبکه تطبیق بدون بررسی فرکانس، آنتن و مشخصات برد خودداری کنید.
- **PCB:** پیوستگی GND، مسیر بازگشت جریان، جداسازی نواحی پرنویز و جانمایی قطعات حساس را در بازبینی Layout کنترل کنید.
- **اعتبارسنجی:** پس از ساخت برد، ابتدا تغذیه و جریان مصرفی، سپس پروگرام و دیباگ، کلاک، رابط‌ها و در نهایت عملکرد RF را مرحله‌به‌مرحله آزمایش کنید.

## ۶. ارتباط با سایر بخش‌های مخزن

- [صفحه اصلی پروژه MES-CH585](../../README.md)
- [مستندات و منابع EVT](../README.md)
- [مثال‌های نرم‌افزاری EVT/EXAM](../EXAM/README.md)
- [منابع دیتاشیت CH585](../../Datasheet/)
- [تصاویر و فایل‌های گرافیکی پروژه](../../Images/)

## ۷. منابع و مسئولیت استفاده

فایل‌های PDF و طراحی‌های سخت‌افزاری این پوشه با هدف مطالعه، آموزش، ارزیابی و توسعه در اختیار کاربران قرار گرفته‌اند. نام فایل‌ها و محتوای اصلی منابع حفظ شده است تا ردیابی نسخه‌ها و مراجعه به اسناد سازنده آسان باشد.

پیش از استفاده تجاری یا تولید انبوه، مجوز و شرایط استفاده از منابع اصلی، صحت طراحی، وضعیت قطعات و انطباق با آخرین مستندات رسمی WCH را بررسی کنید.

## ۸. تصاویر و دیاگرام‌های راهنما

<img src="../../Images/GitHub-Assets/MES-Divider.svg" alt="MES Divider" width="100%">

برای مشاهده سایر تصاویر و عناصر گرافیکی مورد استفاده در مستندات پروژه، به پوشه [Images/GitHub-Assets](../../Images/GitHub-Assets/) مراجعه کنید.

---

## تهیه و تدوین

**معمار الکترونیک صنعت | MEMAR ELECTRONIC SANAT (MES)**

*همراه شما در مسیر طراحی و ساخت مدارهای مطمئن*

- **GitHub:** [MEMAR-ELECTRONIC-SANAT](https://github.com/MEMAR-ELECTRONIC-SANAT)
- **Telegram:** [@Memar_Electronic](https://t.me/Memar_Electronic)
- **Instagram:** [@Memar.Electronic](https://www.instagram.com/Memar.Electronic)

[مشاهده سایر آموزش‌ها و پروژه‌ها](https://github.com/MEMAR-ELECTRONIC-SANAT)

<img src="../../Images/GitHub-Assets/MES-Thank-You-Footer.svg" alt="Thank you - MES" width="100%">

</div>

---

# CH585 Hardware Resources and Design Documents | PUB

The **PUB** directory is part of the hardware and technical resources provided with the **WCH CH585 EVT** package. It contains reference documentation for the CH585 evaluation hardware, circuit and PCB design notes, and hardware design files created with **Altium Designer**.

These resources are intended to help developers study reference hardware, review schematics, and use the available designs as a starting point for their own CH585-based boards.

> **Important:** These files are reference materials. Before using them in a final product, verify the device variant, package, electrical limits, RF requirements, and the latest WCH datasheet and hardware design recommendations.

## 1. Directory Structure

| Path | Description |
|---|---|
| `CH585SCH.pdf` | CH585 hardware schematic document |
| `CH585评估板说明书.pdf` | CH585 evaluation board user guide (Chinese) |
| `蓝牙芯片的电路及PCB设计的重要注意事项.pdf` | Important circuit and PCB design considerations for Bluetooth chips (Chinese) |
| `SCHPCB/` | Altium Designer schematic and PCB files |

## 2. PDF Documentation

### 2.1. CH585 Schematic

[**Download CH585SCH.pdf**](./CH585SCH.pdf)

This document is provided for reviewing the CH585 reference hardware schematic. Cross-check the power connections, bypass capacitors, reset and programming/debug interfaces, clock circuitry, peripheral connections, and RF-related circuitry (where applicable) against the device datasheet and hardware design documentation.

### 2.2. CH585 Evaluation Board User Guide

[**Download CH585评估板说明书.pdf**](./CH585评估板说明书.pdf)

This is the CH585 evaluation board guide. The document is in Chinese and can be used to review the board hardware, available features, connections, and usage instructions.

### 2.3. Bluetooth Circuit and PCB Design Considerations

[**Download 蓝牙芯片的电路及PCB设计的重要注意事项.pdf**](./蓝牙芯片的电路及PCB设计的重要注意事项.pdf)

This Chinese document covers important considerations for Bluetooth chip circuit and PCB design. It is particularly relevant when implementing the RF section of a wireless board.

Pay special attention to RF routing and impedance matching, antenna placement and keepout, a continuous ground plane and return paths, supply decoupling, and the influence of the enclosure and nearby components on antenna performance. These are general considerations; implementation details must follow the reference design and RF documentation for the exact device and antenna.

## 3. Altium Designer Schematic and PCB Files

The [**SCHPCB**](./SCHPCB/) directory contains native Altium Designer documents:

- `.SchDoc` — Schematic Document
- `.PcbDoc` — PCB Document

### 3.1. CH585D-DG-R0 Design

[**Browse CH585D-DG-R0**](./SCHPCB/CH585D-DG-R0/)

| File | Type | Description |
|---|---|---|
| [CH585D-DG-R0.SchDoc](./SCHPCB/CH585D-DG-R0/CH585D-DG-R0.SchDoc) | SchDoc | CH585D-DG-R0 schematic |
| [CH585D-DG-R0-1v0.PcbDoc](./SCHPCB/CH585D-DG-R0/CH585D-DG-R0-1v0.PcbDoc) | PcbDoc | PCB document, version 1v0 |

### 3.2. CH585M-R1 Design

[**Browse CH585M-R1**](./SCHPCB/CH585M-R1/)

| File | Type | Description |
|---|---|---|
| [CH585M-R1.SchDoc](./SCHPCB/CH585M-R1/CH585M-R1.SchDoc) | SchDoc | CH585M-R1 schematic |
| [CH585M-R1-1v1.PcbDoc](./SCHPCB/CH585M-R1/CH585M-R1-1v1.PcbDoc) | PcbDoc | PCB document, version 1v1 |

**Note:** The D and M identifiers are retained as used in the original design names. Do not infer package, electrical, or functional differences from the folder names alone. Inspect the schematics and the relevant WCH documentation to identify the exact hardware variants.

## 4. Working with the Altium Files

1. Download the required `.SchDoc` and `.PcbDoc` files.
2. Open them with a compatible version of **Altium Designer**. If required, add both documents to a single Altium project.
3. If components or libraries are missing, check the library paths and external model dependencies. The repository files are not necessarily accompanied by every library or an integrated project file.
4. Before modifying or manufacturing the PCB, verify schematic-to-PCB consistency, design rules, nets, board dimensions, layer stackup, and component footprints.
5. Do not send manufacturing outputs directly to production without an engineering review. Reference files may differ from your product requirements, available components, or the latest datasheet revision.

## 5. CH585 Hardware Design Considerations

- **Power supply:** Check the permitted voltage range and requirements of each supply pin in the CH585 datasheet. Place bypass capacitors close to the relevant power pins as recommended by WCH.
- **Programming and debugging:** Provide the required programming, debugging, and firmware-recovery connections. Avoid conflicts between these pins and other functions.
- **Clock:** For an external crystal or clock source, verify the component specification, load capacitance, placement, and routing against the reference design.
- **RF and antenna:** 2.4 GHz performance depends on placement, trace impedance, grounding, antenna design, and mechanical conditions. Do not copy antenna dimensions or matching networks without validating them for the selected antenna and PCB.
- **PCB layout:** Review ground continuity, return-current paths, noisy circuit areas, and the placement of sensitive components.
- **Validation:** After assembly, test the power rails and current consumption first, followed by programming/debugging, clock operation, interfaces, and RF performance.

## 6. Related Repository Sections

- [MES-CH585 project home](../../README.md)
- [EVT documentation and resources](../README.md)
- [EVT/EXAM software examples](../EXAM/README.md)
- [CH585 datasheet resources](../../Datasheet/)
- [Project images and graphics](../../Images/)

## 7. Resource and Usage Notice

The PDFs and hardware design files in this directory are provided for study, education, evaluation, and development. Original filenames have been retained to make version tracking and reference to the source documents easier.

Before commercial use or mass production, review the original resource licensing and usage terms, validate the design, confirm component availability, and check the latest official WCH documentation.

## 8. Reference Images and Diagrams

<img src="../../Images/GitHub-Assets/MES-Divider.svg" alt="MES Divider" width="100%">

For other visual assets used in this project documentation, visit [Images/GitHub-Assets](../../Images/GitHub-Assets/).

---

## Prepared by

**MEMAR ELECTRONIC SANAT (MES)**

*Your partner in designing and building reliable circuits.*

- **GitHub:** [MEMAR-ELECTRONIC-SANAT](https://github.com/MEMAR-ELECTRONIC-SANAT)
- **Telegram:** [@Memar_Electronic](https://t.me/Memar_Electronic)
- **Instagram:** [@Memar.Electronic](https://www.instagram.com/Memar.Electronic)

[Explore more tutorials and projects](https://github.com/MEMAR-ELECTRONIC-SANAT)

<img src="../../Images/GitHub-Assets/MES-Thank-You-Footer.svg" alt="Thank you - MES" width="100%">

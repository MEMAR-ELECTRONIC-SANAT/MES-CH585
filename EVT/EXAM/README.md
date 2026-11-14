<div dir="rtl" align="right">

# مجموعه مثال‌های نرم‌افزاری میکروکنترلر CH585 | CH585 EVT Examples

## معرفی

پوشه **EXAM** بخش اصلی مثال‌های نرم‌افزاری در بسته توسعه **EVT (Evaluation and Verification Toolkit)** شرکت **WCH** برای میکروکنترلر **CH585** است. این مجموعه برای آشنایی با واحدهای جانبی، رابط‌های ارتباطی، قابلیت‌های بی‌سیم، مدیریت حافظه و توان، سیستم‌عامل‌های بلادرنگ و امکانات USB ارائه شده است.

ساختار مثال‌ها به‌گونه‌ای است که هر قابلیت یا کاربرد، در یک پوشه مستقل قرار گرفته و معمولاً فایل‌های پروژه، کدهای منبع، تنظیمات کامپایل و در برخی موارد فایل خروجی قابل پروگرام را در بر می‌گیرد. هدف این README معرفی ساختار پوشه‌ها، کمک به انتخاب مثال مناسب و ارائه مسیر شروع کار است؛ توضیحات اختصاصی هر پروژه و محدودیت‌های آن را باید در فایل‌های همراه همان پروژه و مستندات رسمی WCH بررسی کنید.

- [بازگشت به راهنمای بسته EVT](../README.md)
- [مشاهده مخزن MES-CH585](../../)
- [دیتاشیت و مستندات CH585](../../Datasheet/)

## ساختار کلی

| پوشه | موضوع |
|---|---|
| [ADC](./ADC/) | مبدل آنالوگ به دیجیتال و نمونه‌برداری |
| [BLE](./BLE/) | Bluetooth Low Energy و ارتباط بی‌سیم 2.4GHz |
| [FLASH](./FLASH/) | خواندن، نوشتن و پاک‌کردن حافظه Flash |
| [FreeRTOS](./FreeRTOS/) | نمونه استفاده از سیستم‌عامل FreeRTOS |
| [HarmonyOS](./HarmonyOS/) | نمونه و منابع مرتبط با LiteOS-M / HarmonyOS |
| [I2C](./I2C/) | ارتباط سریال I²C |
| [IAP](./IAP/) | به‌روزرسانی و پروگرام درون‌مداری برنامه |
| [LCD](./LCD/) | کنترل نمایشگر LCD |
| [LED](./LED/) | کنترل نمایشگر و رابط LED |
| [NFCA](./NFCA/) | قابلیت‌های NFC-A، کارت‌خوان و شبیه‌سازی کارت |
| [PM](./PM/) | مدیریت توان و حالت‌های کم‌مصرف |
| [PWMX](./PWMX/) | تولید سیگنال PWM |
| [RT-Thread](./RT-Thread/) | نمونه استفاده از RT-Thread |
| [SPI](./SPI/) | ارتباط سریال SPI |
| [SRC](./SRC/) | فایل‌های پایه و مشترک پروژه‌ها |
| [TMR](./TMR/) | تایمرها و زمان‌سنجی |
| [TOUCH](./TOUCH/) | تشخیص لمسی خازنی و TouchKey |
| [UART1](./UART1/) | ارتباط UART1 |
| [USB](./USB/) | USB Device، USB Host و USB High-Speed |

---

## معرفی گروه‌های مثال

### ۱. واحدهای جانبی و رابط‌های ارتباطی

| پوشه | شرح و موارد استفاده |
|---|---|
| [ADC](./ADC/) | نمونه کدهای مربوط به مبدل **ADC** و خواندن ورودی‌های آنالوگ. برای بررسی روش نمونه‌برداری و پردازش مقدار ورودی، نقطه شروع مناسبی است. |
| [I2C](./I2C/) | مثال ارتباط **I²C** و فایل راهنمای رابط I²C با نام [I2C接口使用指南.PDF](./I2C/I2C接口使用指南.PDF). |
| [SPI](./SPI/) | مثال راه‌اندازی رابط **SPI** و تبادل داده با تجهیزات جانبی. |
| [UART1](./UART1/) | نمونه ارسال و دریافت داده از طریق **UART1**؛ مناسب برای آشنایی با تنظیمات سریال و ارتباط با تجهیزات خارجی. |
| [TMR](./TMR/) | مثال‌های مبتنی بر **Timer** برای ایجاد وقفه، زمان‌بندی و اندازه‌گیری بازه‌های زمانی. |
| [PWMX](./PWMX/) | نمونه تولید خروجی **PWM**؛ کاربردهایی مانند کنترل توان، LED و تولید سیگنال کنترلی را می‌توان بر پایه این مثال‌ها توسعه داد. |
| [FLASH](./FLASH/) | نمونه عملیات حافظه Flash داخلی، شامل خواندن، نوشتن و پاک‌کردن داده. هنگام استفاده، به آدرس‌بندی حافظه و محدوده‌های رزروشده برای Firmware توجه کنید. |
| [LCD](./LCD/) | مثال‌های راه‌اندازی و کنترل رابط نمایشگر LCD. |
| [LED](./LED/) | نمونه‌های مربوط به رابط و کنترل نمایشگرهای LED. |

### ۲. ارتباط بی‌سیم | BLE

پوشه [BLE](./BLE/) مجموعه گسترده‌ای از پروژه‌های **Bluetooth Low Energy** و ارتباط رادیویی 2.4GHz را در بر می‌گیرد. نمونه‌های موجود، کاربردهای متنوعی از ارتباط ساده بین دو دستگاه تا پروفایل‌های استاندارد BLE و به‌روزرسانی بی‌سیم Firmware را پوشش می‌دهند.

برخی از پروژه‌ها و گروه‌های قابل توجه:

| پروژه / پوشه | کاربرد کلی |
|---|---|
| [Peripheral](./BLE/Peripheral/) | نمونه دستگاه BLE در نقش Peripheral |
| [Central](./BLE/Central/) | نمونه دستگاه BLE در نقش Central |
| [CentPeri](./BLE/CentPeri/) | ترکیب عملکرد Central و Peripheral |
| [MultiCentral](./BLE/MultiCentral/) و [MultiCentPeri](./BLE/MultiCentPeri/) | نمونه‌های ارتباط چندگانه و مدیریت چند اتصال |
| [Observer](./BLE/Observer/) و [Broadcaster](./BLE/Broadcaster/) | دریافت و ارسال بسته‌های تبلیغاتی BLE |
| [BLE_UART](./BLE/BLE_UART/) | ایجاد ارتباط سریال بی‌سیم با استفاده از BLE |
| [BLE_USB](./BLE/BLE_USB/) | نمونه ترکیب قابلیت BLE و USB |
| [HID_Keyboard](./BLE/HID_Keyboard/)، [HID_Mouse](./BLE/HID_Mouse/) و [HID_Consumer](./BLE/HID_Consumer/) | پیاده‌سازی کاربردهای HID مانند صفحه‌کلید، ماوس و کنترلر Consumer |
| [HeartRate](./BLE/HeartRate/) و [CyclingSensor](./BLE/CyclingSensor/) | نمونه‌هایی مبتنی بر پروفایل‌های سنسور ضربان قلب و دوچرخه |
| [BackupUpgrade_OTA](./BLE/BackupUpgrade_OTA/) | نمونه سازوکار به‌روزرسانی Firmware از طریق BLE OTA |
| [Direct_Test_Mode](./BLE/Direct_Test_Mode/) و [RF_PHY](./BLE/RF_PHY/) | مثال‌ها و ابزارهای مرتبط با آزمون RF و لایه فیزیکی |
| [MESH](./BLE/MESH/) | منابع و مثال‌های ارتباط شبکه‌ای BLE Mesh |
| [PAwR_ADV](./BLE/PAwR_ADV/) و [PAwR_RSP](./BLE/PAwR_RSP/) | مثال‌های ارسال‌کننده و پاسخ‌دهنده در قابلیت PAwR |

همچنین در این پوشه فایل‌های مرجع توسعه BLE و مستندات مربوط به **BLE OTA** قرار دارند. برای جزئیات پروتکل‌ها، ساختار Profile و Service، پارامترهای RF و روند OTA، فایل‌های راهنمای داخل پوشه و مرجع توسعه BLE شرکت WCH را مطالعه کنید.

> **نکته:** نام و وجود یک مثال به معنی پشتیبانی یکسان تمام قابلیت‌ها در همه پکیج‌های CH585/CH584 نیست. قبل از انتخاب پایه‌ها یا قابلیت‌های رادیویی، دیتاشیت دقیق قطعه و مستندات همان نسخه SDK را بررسی کنید.

### ۳. به‌روزرسانی Firmware | IAP

پوشه [IAP](./IAP/) نمونه‌ها و منابع مربوط به **In-Application Programming (IAP)** را در اختیار قرار می‌دهد. ساختار فعلی این پوشه شامل زیرشاخه‌های زیر است:

- [APP](./IAP/APP/)
- [UART_IAP](./IAP/UART_IAP/)
- [USB_IAP](./IAP/USB_IAP/)
- [USBHS_IAP](./IAP/USBHS_IAP/)
- [ابزار WCH MCU IAP برای Windows](./IAP/WCHMcuIAP_WinAPP.zip)

این مثال‌ها برای بررسی معماری Bootloader و انتقال Firmware از مسیرهای ارتباطی مختلف مفید هستند. پیش از استفاده عملی، نقشه حافظه، آدرس شروع Bootloader و Application، اندازه Firmware، روش اعتبارسنجی فایل و سازگاری نسخه پروگرامر را با پروژه خود تطبیق دهید.

### ۴. ارتباط و کاربردهای NFC-A

پوشه [NFCA](./NFCA/) منابع مربوط به **NFC-A** را شامل می‌شود:

| زیرپوشه / فایل | شرح |
|---|---|
| [PCD](./NFCA/PCD/) | نمونه عملکرد در نقش Proximity Coupling Device یا Reader |
| [PCD_SOFT](./NFCA/PCD_SOFT/) | نمونه پیاده‌سازی نرم‌افزاری عملکرد PCD |
| [PICC](./NFCA/PICC/) | نمونه عملکرد در نقش Proximity Integrated Circuit Card یا Card |
| [NFCA_LIB](./NFCA/NFCA_LIB/) | کتابخانه‌ها و فایل‌های پشتیبان NFC-A |
| [راهنمای کاربرد NFC در CH585](./NFCA/CH585%20NFC读卡器应用指南.pdf) | سند راهنمای کاربرد NFC Reader |

برای توسعه کاربردهای NFC، ابتدا نقش موردنیاز سیستم (Reader یا Card) را مشخص کنید و سپس مثال متناظر را بررسی کنید. نوع تگ، پروتکل و کتابخانه مورد استفاده باید با سخت‌افزار و هدف پروژه سازگار باشد.

### ۵. تشخیص لمسی خازنی | TOUCH

پوشه [TOUCH](./TOUCH/) مثال‌ها و کتابخانه‌های تشخیص لمسی خازنی **TouchKey** را شامل می‌شود.

| مسیر | کاربرد |
|---|---|
| [TKYLIB](./TOUCH/TKYLIB/) | کتابخانه تشخیص لمسی WCH |
| [Touch_EX001](./TOUCH/Touch_EX001/) | پروژه نمونه TouchKey |
| [Touch_EX001_ble](./TOUCH/Touch_EX001_ble/) | نمونه TouchKey همراه با ارتباط BLE |
| [Touch_EX002](./TOUCH/Touch_EX002/) | پروژه نمونه دوم TouchKey |
| [Touch_EX002_ble](./TOUCH/Touch_EX002_ble/) | نمونه دوم TouchKey همراه با BLE |
| [راهنمای کتابخانه لمسی WCH](./TOUCH/WCH触摸库使用说明.pdf) | مستندات استفاده از کتابخانه TouchKey |

این مثال‌ها برای بررسی پیاده‌سازی کلید لمسی و ترکیب ورودی لمسی با ارتباط BLE مناسب هستند. پارامترهای حساسیت، کالیبراسیون، طراحی الکترود و شرایط PCB بر عملکرد تشخیص لمسی اثر مستقیم دارند؛ بنابراین تنظیمات نرم‌افزاری را همراه با طراحی واقعی برد ارزیابی کنید.

### ۶. مدیریت توان | PM

پوشه [PM](./PM/) مثال‌های مربوط به **Power Management** را در بر می‌گیرد. این منابع برای بررسی حالت‌های کم‌مصرف، ورود و خروج از حالت خواب و روش‌های بیدارشدن از طریق منابع مختلف مفید هستند.

در طراحی کم‌مصرف، جریان مصرفی هر حالت، وضعیت GPIOها، منبع کلاک، تایمرها، BLE و منابع بیدارباش را در کنار یکدیگر بررسی کنید. مقادیر نهایی مصرف توان باید با اندازه‌گیری روی سخت‌افزار هدف تأیید شوند.

### ۷. سیستم‌عامل‌های بلادرنگ و منابع نرم‌افزاری

| پوشه | شرح |
|---|---|
| [FreeRTOS](./FreeRTOS/) | پروژه نمونه و منابع مرتبط با استفاده از FreeRTOS روی CH585؛ فایل [readme.txt](./FreeRTOS/readme.txt) را نیز بررسی کنید. |
| [RT-Thread](./RT-Thread/) | نمونه مبتنی بر RT-Thread Nano و منابع آن؛ فایل [readme.txt](./RT-Thread/readme.txt) راهنمای همراه پروژه است. |
| [HarmonyOS](./HarmonyOS/) | منابع پروژه LiteOS-M و فایل راهنمای [readme.txt](./HarmonyOS/readme.txt). |

این پروژه‌ها برای آشنایی با ساختار Task، زمان‌بندی، مدیریت وقفه و استفاده از امکانات سیستم‌عامل مناسب‌اند. پیش از انتقال آن‌ها به محصول نهایی، میزان مصرف RAM و Flash، اولویت Taskها، پشته (Stack)، زمان‌بندی وقفه‌ها و سازگاری درایورها را ارزیابی کنید.

### ۸. فایل‌های پایه و مشترک | SRC

پوشه [SRC](./SRC/) اجزای زیرساختی مشترک مورد استفاده پروژه‌های EVT را نگهداری می‌کند:

| زیرپوشه | نقش |
|---|---|
| [Ld](./SRC/Ld/) | فایل‌های Linker و تعریف نواحی حافظه |
| [RVMSIS](./SRC/RVMSIS/) | فایل‌های هدر و منابع مرتبط با RISC-V CMSIS / هسته |
| [Startup](./SRC/Startup/) | کدهای راه‌اندازی اولیه پردازنده و برد |
| [StdPeriphDriver](./SRC/StdPeriphDriver/) | درایورهای استاندارد واحدهای جانبی |

این فایل‌ها بخشی از ساختار ساخت و اجرای Firmware هستند. هنگام ایجاد پروژه جدید یا انتقال مثال به محیط توسعه دیگر، وابستگی مسیرها، فایل Linker، فایل Startup، تعریف تراشه و نسخه درایورها را حفظ و کنترل کنید.

### ۹. رابط USB

پوشه [USB](./USB/) مثال‌های USB را در سه گروه اصلی دسته‌بندی کرده است:

| مسیر | شرح |
|---|---|
| [Device](./USB/Device/) | نمونه‌های CH585 در نقش USB Device |
| [Host](./USB/Host/) | نمونه‌های CH585 در نقش USB Host |
| [USBHS](./USB/USBHS/) | مثال‌های مبتنی بر کنترلر USB High-Speed |

در گروه Device، پروژه‌هایی مانند **COM، CompoundDev، HID_CompliantDev** و **VendorDefinedDev** دیده می‌شوند. این پروژه‌ها برای بررسی کلاس‌های USB و ساختار Descriptorها نقطه شروع مناسبی هستند.

در گروه Host، نمونه‌هایی مانند **HostEnum، HostAOA** و پروژه‌های **U_DISK** برای بررسی شناسایی دستگاه USB، ارتباط با تجهیزات جانبی و دسترسی به حافظه USB قرار دارند.

گروه USBHS نیز پروژه‌های Device و Host را شامل می‌شود؛ از جمله نمونه‌های **CDC، HID، Composite، MSC (Mass Storage)** و کاربردهای مرتبط با IAP. برای جزئیات هر پروژه، ساختار پوشه و فایل‌های سورس همان مثال را بررسی کنید.

---

## راهنمای شروع کار با مثال‌ها

۱. **انتخاب مثال:** ابتدا قابلیت موردنظر را مشخص کنید و پوشه مربوط به آن را از جدول ساختار کلی باز کنید.

۲. **مطالعه فایل‌های همراه:** فایل‌هایی مانند `readme.txt`، فایل‌های PDF و توضیحات متنی موجود در پوشه پروژه را پیش از کامپایل بخوانید.

۳. **بازکردن پروژه:** بسیاری از پروژه‌ها فایل‌های `.project`، `.cproject` و فایل اختصاصی `.wvproj` دارند. پروژه را با نسخه سازگار محیط توسعه WCH، مانند **MounRiver Studio**، باز کنید.

۴. **بررسی پیکربندی:** مدل دقیق تراشه، پکیج، فرکانس کلاک، تنظیمات حافظه، پایه‌های GPIO و وابستگی‌های پروژه را کنترل کنید. نام پروژه یا پوشه به‌تنهایی تضمین نمی‌کند که تنظیمات آن برای برد شما مناسب باشد.

۵. **کامپایل و پروگرام:** ابتدا پروژه را بدون تغییر کامپایل کنید؛ سپس با ابزار و روش پروگرام متناسب با برد، Firmware را روی تراشه اجرا کنید.

۶. **آزمون مرحله‌ای:** عملکرد مثال را ابتدا در شرایط مرجع و سپس با تغییرات محدود و کنترل‌شده بررسی کنید. برای قابلیت‌هایی مانند RF، BLE، NFC، USB و مصرف توان، آزمون سخت‌افزاری ضروری است.

## نکات مهم فنی

- **تطبیق مدل تراشه:** این مجموعه برای CH585 تهیه شده است. استفاده از مثال‌ها روی CH584 یا سایر اعضای خانواده را بدون بررسی تفاوت منابع سخت‌افزاری توصیه نمی‌کنیم.
- **محدودیت پکیج:** همه پایه‌ها و امکانات در تمام پکیج‌ها در دسترس نیستند. دیتاشیت پکیج دقیق را مرجع انتخاب پایه قرار دهید.
- **نسخه ابزار و SDK:** نسخه MounRiver Studio، کامپایلر، کتابخانه‌ها و ابزارهای پروگرام می‌توانند بر نتیجه ساخت اثر بگذارند.
- **فایل‌های خروجی:** وجود فایل‌های `.hex` در پوشه `obj` صرفاً نشان می‌دهد خروجی در مخزن قرار گرفته است؛ برای اطمینان از تناسب آن با سخت‌افزار، نسخه و تنظیمات ساخت، پروژه را مجدداً بررسی و در صورت نیاز کامپایل کنید.
- **حافظه و IAP:** در پروژه‌های Bootloader و OTA، پیش از هرگونه تغییر، نقشه حافظه و روش بازیابی Firmware را بررسی کنید.
- **ایمنی و صحت عملکرد:** مثال‌های EVT پروژه‌های مرجع آموزشی و توسعه هستند؛ استفاده در محصول نهایی به بازبینی کد، آزمون عملکرد، بررسی امنیت و اعتبارسنجی سخت‌افزار نیاز دارد.

## منابع و پیوندهای مرتبط

- [راهنمای کلی پوشه EVT](../README.md)
- [مخزن MES-CH585](../../)
- [دیتاشیت و مستندات فنی CH585](../../Datasheet/)
- [پروژه صفحه‌کلید لمسی خازنی CH585](../../Application/CapacitiveTouchKeyboard/)
- [فایل‌های سخت‌افزاری و مستندات برد ارزیابی](../PUB/)

---

## تصاویر و دیاگرام‌های راهنما

<p align="center">
  <img src="../../Images/GitHub-Assets/MES-Section-Header.svg" width="100%" alt="MES Technical Resources">
</p>

برای مشاهده سایر عناصر گرافیکی و تصاویر مورد استفاده در مستندات، به [پوشه GitHub-Assets](../../Images/GitHub-Assets/) مراجعه کنید.

<p align="center">
  <img src="../../Images/GitHub-Assets/MES-Divider.svg" width="100%" alt="MES Divider">
</p>

## تهیه و تدوین

**معمار الکترونیک صنعت**  
**MEMAR ELECTRONIC SANAT (MES)**

همراه شما در مسیر طراحی و ساخت مدارهای مطمئن

- کانال تلگرام: [https://t.me/Memar_Electronic](https://t.me/Memar_Electronic)
- پیج اینستاگرام: [https://www.instagram.com/Memar.Electronic](https://www.instagram.com/Memar.Electronic)

[مشاهده سایر آموزش‌ها](https://github.com/MEMAR-ELECTRONIC-SANAT)

<p align="center">
  <img src="../../Images/GitHub-Assets/MES-Thank-You-Footer.svg" width="100%" alt="Thank you for visiting MES">
</p>

</div>

---

# CH585 EVT Software Examples

## Overview

The **EXAM** directory is the main collection of software examples included in WCH's **Evaluation and Verification Toolkit (EVT)** for the **CH585** microcontroller. It provides reference projects for peripheral drivers, communication interfaces, wireless connectivity, memory management, low-power operation, real-time operating systems, NFC and USB.

Examples are organized into separate directories by function. A project folder may contain source code, project configuration, build settings and, in some cases, a prebuilt firmware image. This README provides a directory guide and a suggested workflow. Always consult the documentation shipped with each example and the official WCH references for implementation details and limitations.

- [Back to the EVT package guide](../README.md)
- [Open the MES-CH585 repository](../../)
- [CH585 datasheets and documentation](../../Datasheet/)

## Directory Overview

| Directory | Topic |
|---|---|
| [ADC](./ADC/) | Analog-to-digital conversion and sampling |
| [BLE](./BLE/) | Bluetooth Low Energy and 2.4GHz wireless communication |
| [FLASH](./FLASH/) | On-chip Flash read, write and erase operations |
| [FreeRTOS](./FreeRTOS/) | FreeRTOS example |
| [HarmonyOS](./HarmonyOS/) | LiteOS-M / HarmonyOS-related resources |
| [I2C](./I2C/) | I²C serial communication |
| [IAP](./IAP/) | In-application firmware programming and update |
| [LCD](./LCD/) | LCD interface examples |
| [LED](./LED/) | LED display interface examples |
| [NFCA](./NFCA/) | NFC-A, reader and card examples |
| [PM](./PM/) | Power management and low-power modes |
| [PWMX](./PWMX/) | PWM signal generation |
| [RT-Thread](./RT-Thread/) | RT-Thread example |
| [SPI](./SPI/) | SPI serial communication |
| [SRC](./SRC/) | Shared project and startup resources |
| [TMR](./TMR/) | Timers and timing |
| [TOUCH](./TOUCH/) | Capacitive touch sensing and TouchKey |
| [UART1](./UART1/) | UART1 communication |
| [USB](./USB/) | USB Device, USB Host and USB High-Speed |

## Example Groups

### 1. Peripherals and Serial Interfaces

| Directory | Description |
|---|---|
| [ADC](./ADC/) | ADC input sampling and analog measurement examples. |
| [I2C](./I2C/) | I²C communication examples and the [I2C interface guide](./I2C/I2C接口使用指南.PDF). |
| [SPI](./SPI/) | SPI interface initialization and data exchange with external peripherals. |
| [UART1](./UART1/) | UART1 transmission and reception examples. |
| [TMR](./TMR/) | Timer-based interrupts, timing and interval measurement. |
| [PWMX](./PWMX/) | PWM output generation for control and signal-generation applications. |
| [FLASH](./FLASH/) | On-chip Flash read, write and erase operations. Check memory regions reserved for firmware. |
| [LCD](./LCD/) | LCD interface and display-control examples. |
| [LED](./LED/) | LED display interface examples. |

### 2. Bluetooth Low Energy | BLE

The [BLE](./BLE/) directory contains a broad collection of **Bluetooth Low Energy** and 2.4GHz wireless examples, ranging from basic device roles to standard BLE profiles, RF testing and firmware updates.

Selected projects include:

| Project / Directory | General purpose |
|---|---|
| [Peripheral](./BLE/Peripheral/) | BLE Peripheral role |
| [Central](./BLE/Central/) | BLE Central role |
| [CentPeri](./BLE/CentPeri/) | Combined Central and Peripheral operation |
| [MultiCentral](./BLE/MultiCentral/) and [MultiCentPeri](./BLE/MultiCentPeri/) | Multiple connections and multi-role examples |
| [Observer](./BLE/Observer/) and [Broadcaster](./BLE/Broadcaster/) | BLE advertising reception and transmission |
| [BLE_UART](./BLE/BLE_UART/) | Wireless serial communication over BLE |
| [BLE_USB](./BLE/BLE_USB/) | BLE and USB combined example |
| [HID_Keyboard](./BLE/HID_Keyboard/), [HID_Mouse](./BLE/HID_Mouse/) and [HID_Consumer](./BLE/HID_Consumer/) | HID keyboard, mouse and consumer-control applications |
| [HeartRate](./BLE/HeartRate/) and [CyclingSensor](./BLE/CyclingSensor/) | Heart Rate and Cycling Sensor profile examples |
| [BackupUpgrade_OTA](./BLE/BackupUpgrade_OTA/) | BLE OTA firmware update example |
| [Direct_Test_Mode](./BLE/Direct_Test_Mode/) and [RF_PHY](./BLE/RF_PHY/) | RF and physical-layer test examples |
| [MESH](./BLE/MESH/) | BLE Mesh resources and examples |
| [PAwR_ADV](./BLE/PAwR_ADV/) and [PAwR_RSP](./BLE/PAwR_RSP/) | PAwR advertiser and responder examples |

The directory also contains BLE development reference material and BLE OTA documentation. Refer to the included documents for details about profiles, services, RF parameters and OTA procedures.

> **Note:** The presence of an example does not imply that every feature is available on every CH585/CH584 package. Check the exact device datasheet and SDK documentation before assigning pins or selecting a peripheral.

### 3. Firmware Update | IAP

The [IAP](./IAP/) directory contains resources for **In-Application Programming (IAP)**:

- [APP](./IAP/APP/)
- [UART_IAP](./IAP/UART_IAP/)
- [USB_IAP](./IAP/USB_IAP/)
- [USBHS_IAP](./IAP/USBHS_IAP/)
- [WCH MCU IAP Windows application](./IAP/WCHMcuIAP_WinAPP.zip)

These examples are useful for studying bootloader architecture and firmware transfer over different interfaces. Before deployment, verify the memory map, bootloader and application addresses, firmware size, image validation method and programmer compatibility.

### 4. NFC-A

The [NFCA](./NFCA/) directory contains **NFC-A** resources:

| Directory / File | Description |
|---|---|
| [PCD](./NFCA/PCD/) | Proximity Coupling Device / reader example |
| [PCD_SOFT](./NFCA/PCD_SOFT/) | Software-based PCD example |
| [PICC](./NFCA/PICC/) | Proximity Integrated Circuit Card example |
| [NFCA_LIB](./NFCA/NFCA_LIB/) | NFC-A libraries and supporting files |
| [CH585 NFC Reader Application Guide](./NFCA/CH585%20NFC读卡器应用指南.pdf) | NFC reader application documentation |

Select the required operating role (Reader or Card) before choosing an example. The tag type, protocol and library must match the target hardware and application.

### 5. Capacitive Touch Sensing | TOUCH

The [TOUCH](./TOUCH/) directory provides examples and libraries for the CH585 **TouchKey** capacitive sensing feature.

| Directory / File | Description |
|---|---|
| [TKYLIB](./TOUCH/TKYLIB/) | WCH touch-detection library |
| [Touch_EX001](./TOUCH/Touch_EX001/) | TouchKey example project |
| [Touch_EX001_ble](./TOUCH/Touch_EX001_ble/) | TouchKey example with BLE |
| [Touch_EX002](./TOUCH/Touch_EX002/) | Second TouchKey example |
| [Touch_EX002_ble](./TOUCH/Touch_EX002_ble/) | Second TouchKey example with BLE |
| [WCH Touch Library User Guide](./TOUCH/WCH触摸库使用说明.pdf) | TouchKey library documentation |

These projects are useful for studying capacitive key detection and combining touch input with BLE. Sensitivity, calibration, electrode geometry and PCB layout all affect touch performance; validate software settings on the actual board.

### 6. Power Management | PM

The [PM](./PM/) directory contains **Power Management** examples for low-power operation, sleep entry and wake-up sources. For a real design, evaluate current consumption, GPIO states, clock sources, timers, BLE activity and wake-up configuration together. Verify final power figures by measurement on the target hardware.

### 7. Real-Time Operating Systems and Software Resources

| Directory | Description |
|---|---|
| [FreeRTOS](./FreeRTOS/) | FreeRTOS example and related resources. See [readme.txt](./FreeRTOS/readme.txt). |
| [RT-Thread](./RT-Thread/) | RT-Thread Nano example and resources. See [readme.txt](./RT-Thread/readme.txt). |
| [HarmonyOS](./HarmonyOS/) | LiteOS-M resources and project notes. See [readme.txt](./HarmonyOS/readme.txt). |

These projects can help developers understand task scheduling, interrupt handling and RTOS integration. Before adapting them to a product, evaluate RAM and Flash usage, task priorities, stack sizes, interrupt timing and driver compatibility.

### 8. Shared Source Resources | SRC

The [SRC](./SRC/) directory contains shared components used by EVT projects:

| Directory | Purpose |
|---|---|
| [Ld](./SRC/Ld/) | Linker scripts and memory-region definitions |
| [RVMSIS](./SRC/RVMSIS/) | RISC-V core and CMSIS-related headers/resources |
| [Startup](./SRC/Startup/) | Processor startup code |
| [StdPeriphDriver](./SRC/StdPeriphDriver/) | Standard peripheral drivers |

When creating a new project or migrating an example to another development environment, verify include paths, linker scripts, startup files, device definitions and driver versions.

### 9. USB

The [USB](./USB/) directory is divided into three main groups:

| Directory | Description |
|---|---|
| [Device](./USB/Device/) | CH585 USB Device examples |
| [Host](./USB/Host/) | CH585 USB Host examples |
| [USBHS](./USB/USBHS/) | USB High-Speed controller examples |

The Device group includes projects such as **COM, CompoundDev, HID_CompliantDev** and **VendorDefinedDev**, which are useful for studying USB classes and descriptors.

The Host group includes examples such as **HostEnum, HostAOA** and **U_DISK** projects for USB enumeration, peripheral communication and USB storage access.

The USBHS group contains Device and Host projects, including **CDC, HID, Composite, MSC (Mass Storage)** and IAP-related applications. Consult each project's source and documentation for its exact implementation.

## Getting Started

1. **Choose an example:** Identify the required peripheral or feature and open the corresponding directory.
2. **Read the included documentation:** Review `readme.txt`, PDF files and project notes before building.
3. **Open the project:** Many examples include `.project`, `.cproject` and `.wvproj` files. Open them using a compatible WCH development environment such as **MounRiver Studio**.
4. **Check the configuration:** Verify the exact MCU, package, clock settings, memory configuration, GPIO assignments and project dependencies.
5. **Build and program:** Build the unmodified example first, then program the target board using a compatible tool and procedure.
6. **Test incrementally:** Verify the reference behavior before making controlled changes. Hardware validation is essential for RF, BLE, NFC, USB and low-power applications.

## Important Technical Notes

- **Device compatibility:** These examples are provided for CH585. Do not assume they can be used unchanged on CH584 or other family members.
- **Package limitations:** Not all pins and peripherals are available in every package. Use the exact package datasheet for pin selection.
- **Toolchain and SDK versions:** MounRiver Studio, compiler, libraries and programming tools can affect build results.
- **Prebuilt output files:** The presence of a `.hex` file in an `obj` directory only indicates that a firmware image is stored in the repository. Rebuild and verify it against your target hardware and project configuration when necessary.
- **Memory and IAP:** Before modifying bootloader or OTA projects, review the memory map and firmware recovery procedure.
- **Product readiness:** EVT examples are development references. Production use requires code review, functional testing, security assessment and hardware validation.

## Related Resources

- [EVT package guide](../README.md)
- [MES-CH585 repository](../../)
- [CH585 datasheets and technical documentation](../../Datasheet/)
- [CH585 Capacitive Touch Keyboard project](../../Application/CapacitiveTouchKeyboard/)
- [Evaluation board documentation and hardware files](../PUB/)

---

## Images and Reference Diagrams

<p align="center">
  <img src="../../Images/GitHub-Assets/MES-Section-Header.svg" width="100%" alt="MES Technical Resources">
</p>

For additional graphical assets and documentation images, visit the [GitHub-Assets directory](../../Images/GitHub-Assets/).

<p align="center">
  <img src="../../Images/GitHub-Assets/MES-Divider.svg" width="100%" alt="MES Divider">
</p>

## Credits and Documentation

**MEMAR ELECTRONIC SANAT (MES)**

*Your partner in designing and building reliable circuits.*

- Telegram: [https://t.me/Memar_Electronic](https://t.me/Memar_Electronic)
- Instagram: [https://www.instagram.com/Memar.Electronic](https://www.instagram.com/Memar.Electronic)

[Explore more tutorials](https://github.com/MEMAR-ELECTRONIC-SANAT)

<p align="center">
  <img src="../../Images/GitHub-Assets/MES-Thank-You-Footer.svg" width="100%" alt="Thank you for visiting MES">
</p>

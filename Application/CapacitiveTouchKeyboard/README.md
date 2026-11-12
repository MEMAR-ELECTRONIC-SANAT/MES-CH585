# Capacitive Touch Keyboard - v2.0

[[v1.1](./README_v1.1.md)]

### 1. Overview

This solution was first proposed by electronics enthusiast Ricardo. He wanted to design a capacitive touch keyboard PCB and print his business card on it. He chose to use CH582M for this solution and designed the PCB, but it has not been verified yet. So based on his solution, we upgraded the main control chip to CH585M and did actual verification. The PCB packages of CH585M and CH582M are the same, and they can be pin to pin compatible.

CH585M is a BLE chip that supports USB2.0 high/full/low speed, 14-channel TouchKey detection (supports up to 49 touch keys) and NFC. Compared with CH582M, CH585M upgrades the USB interface to high speed (480Mbps). TouchKey detection performance is stronger. The newly added NFC peripheral can simplify the BLE connection process. After the mobile phone scans NFC, it can directly connect to BLE, eliminating the tedious manual connection.

The latest version of the firmware v2.2 supports connecting to different terminals via BLE. This firmware simulates NFC as a card and saves BLE related information in it. Android phones can directly connect to the BLE keyboard by scanning the NFC card.

### 2. Schematic

<div style="text-align: center;">
  <img src="./image/Schematic_v2.0.png" width="1000" />
</div>

### 3. Layout

<div style="text-align: center;">
  <img src="./image/Layout_v2.0.jpg" width="1000" />
</div>

**Layout Notes:**

- **Signal Lines:**
1. The touch signal lines should be as short as possible.
2. It is recommended to use the minimum line width allowed by the PCB process. Generally, the minimum is 5mil and the maximum is no more than 10mil.
3. The spacing between adjacent signal lines should be kept at more than 3 times the line width. Otherwise, the interference between adjacent keys will increase, affecting the touch performance.
4. The routing should minimize corners. If it cannot be avoided, the corners should be 45&deg; or rounded.
5. The routing should avoid being close to high-frequency signal lines. If it cannot be avoided, the two should be routed vertically. If vertical routing is not possible, a ground wire needs to be added between the two.

- **Touch pad:**
1. Place the touch signal line on the back of the touch panel. Connect the touch signal line to the touch pad through a via. This can effectively reduce the probability of finger accidental touch. It is recommended that the vias be located at the edge of the touch pad to reduce the trace length.
2. If the touch signal line and the touch pad are not on the same layer, the signal line of other touch pads cannot be routed directly under the touch pad.
3. Do not lay copper directly below the touch pad (bottom layer). If copper needs to be laid on the touch pad layer (top layer), it is generally laid in a mesh pattern. The recommended distance between the touch pad or signal line and the ground is 1-2 mm.

### 4. Principle

<div style="text-align: center;">
  <img src="./image/Principle1.jpg" width="500" />
</div>

The touch pad on the PCB and the nearby GND form a parasitic capacitance ***C<sub>P</sub>***. Due to the existence of human body capacitance, when a finger touches the pad, a capacitance ***C<sub>F</sub>*** is introduced, which increases the total capacitance. The total capacitance ***C<sub>T</sub>*** can be expressed as: ***C<sub>T</sub> = C<sub>P</sub> + C<sub>F</sub>***.

The size of the capacitance change ***C<sub>F</sub>*** caused is approximately between 0.1pF and 5pF. The size of ***C<sub>F</sub>*** is related to factors such as the finger contact area, the distance between the finger and the pad, and the dielectric constant of the medium between the finger and the pad.

<div style="text-align: center;">
  <img src="./image/Principle2.jpg" width="500" />
</div>

As long as the same time is used to charge the pad capacitor, the ADC of the micro controller is used to collect the voltage value of the corresponding pad and compare it with the value when it is not touched. Then, the defined difference threshold can be used to identify whether the pad is touched.

<div style="text-align: center;">
  <img src="./image/Diagram1.jpg" width="500" />
</div>

This figure is a demonstration diagram of a 3*3 capacitive touch keyboard. Each pad consists of two parts, which are connected to two touch conversion channels respectively. Each touch conversion channel is connected to 3 pads. The connection directions are crossed to achieve a mesh pattern.

After the chip is powered on, it will obtain the touch conversion value of each pad when it is not touched as the reference value. Even if it is touched at this time, there is no problem, because this reference value will be updated after each scan, making it gradually approach the correct reference value.

<div style="text-align: center;">
  <img src="./image/Diagram2.jpg" width="500" />
</div>

At the beginning of each round of scanning, the software first sets the channel connected to the first column (COL1) to the touch conversion function. All other connected channels are set to push-pull output and output 0V. Then the touch conversion difference of the first column can be obtained. Then, in the same way, COL2, COL3, ROW1, ROW2, ROW3 are set to the touch conversion function, and the remaining channels are set to output 0V. The touch conversion difference of all channels can be obtained. When the touch conversion difference of a column channel and a row channel is greater than 0, it means that the intersection of this row and this column is touched.

### 5. Catalog Introduction

- **hardware**: This directory contains the schematics of capacitive touch keyboard
    - **CapTouchKeyboard_v2.0**: Schematic and PCB of CH585M including BLE, USB and NFC interfaces

- **software**: This directory contains software DEMO for capacitive touch keyboard
    - **CapTouchKeyboard_v2.2**: Software DEMO of capacitive touch keyboard supporting BLE and NFC
        - **APP**: Files related to BLE HID keyboard communication and touch key processing
        - **Enc**: Secure connection algorithm related files
        - **HAL**: Hardware related files
        - **LIB**: BLE protocol stack related files
        - **NFCA_LIB**: NFC-A protocol stack related files
        - **PICC_COMMON**: NFC-A PICC transceiver control related files
        - **Profile**: BLE HID keyboard service related files
        - **SRC**: 
            - **Ld**: link file, different projects use different link files
            - **RVMSIS**: Kernel system header files
            - **Startup**: Startup file, different projects use different startup files
            - **StdPeriphDriver**: Basic peripheral driver source files and header files
        - **T2T_COMMON**: NFC-A T2T configuration related files
        - **TKYLIB**: Touch key library related files

### 6. Instructions

#### 6.1 Software Development

The IDE used to develop this project is [MounRiver Studio](http://www.mounriver.com/). The projects in the directory **software** can be directly opened with **MounRiver**. The compiled hex file is downloaded to the board through [WCHISPTool](https://www.wch-ic.com/downloads/WCHISPTool_Setup_exe.html).

#### 6.2 CH585 Programming

1. Connect the keyboard to the PC via a USB cable. Do not power on the CH585 at this time.
2. Press the button (①) and turn on the switch (②) to power on the CH585. At this time, CH585 runs the Bootloader program, and the computer will recognize a USB device. After this the button can be released.
3. WCHISPTool will automatically recognize CH585 (③) and open the download interface.
4. Select the firmware in hex/bin format generated by the IDE (④). 
5. Click Download to program CH585 (⑤).

<img src=./image/Download1_v2.0.jpg width=51% /><img src=./image/Download2_v2.0.jpg width=49% />

---

# نسخه فارسی | صفحه‌کلید لمسی خازنی – نسخه 2.0

[مشاهده نسخه 1.1](./README_v1.1.md)

### ۱. معرفی

این راهکار ابتدا توسط علاقه‌مند حوزه الکترونیک، Ricardo، پیشنهاد شد. هدف او طراحی یک PCB برای صفحه‌کلید لمسی خازنی و چاپ کارت ویزیت خود روی آن بود. او برای این طرح از تراشه CH582M استفاده کرد و PCB را طراحی نمود؛ اما طرح اولیه هنوز مورد آزمایش و تأیید عملی قرار نگرفته بود. بر همین اساس، تراشه اصلی به CH585M ارتقا داده شد و عملکرد طرح به‌صورت عملی بررسی شد. پکیج‌های CH585M و CH582M یکسان هستند و از نظر پایه‌ها قابلیت جایگزینی مستقیم (Pin-to-Pin) دارند.

تراشه CH585M یک تراشه مجهز به BLE است که از USB 2.0 در حالت‌های High-Speed، Full-Speed و Low-Speed، تشخیص لمسی ۱۴ کاناله (TouchKey) با پشتیبانی از حداکثر ۴۹ کلید لمسی و همچنین NFC پشتیبانی می‌کند. در مقایسه با CH582M، رابط USB در CH585M به سرعت بالا (480Mbps) ارتقا یافته و عملکرد تشخیص لمسی نیز بهبود پیدا کرده است. اضافه‌شدن واحد NFC می‌تواند فرایند برقراری ارتباط BLE را ساده‌تر کند؛ به این صورت که تلفن همراه با اسکن NFC مستقیماً به BLE متصل می‌شود و نیازی به انجام مراحل دستی و زمان‌بر اتصال نخواهد بود.

در آخرین نسخه Firmware یعنی v2.2، امکان اتصال از طریق BLE به تجهیزات مختلف فراهم شده است. در این Firmware، قابلیت NFC به‌صورت شبیه‌سازی کارت پیاده‌سازی شده و اطلاعات مرتبط با BLE در آن ذخیره می‌شود. تلفن‌های همراه Android می‌توانند با اسکن کارت NFC، مستقیماً به صفحه‌کلید BLE متصل شوند.

### ۲. شماتیک

<div style="text-align: center;">
  <img src="./image/Schematic_v2.0.png" width="1000" />
</div>

### ۳. طراحی PCB و جانمایی قطعات

<div style="text-align: center;">
  <img src="./image/Layout_v2.0.jpg" width="1000" />
</div>

**نکات مهم در طراحی PCB:**

- **مسیرکشی سیگنال‌ها:**
  1. مسیرهای سیگنال لمسی باید تا حد امکان کوتاه باشند.
  2. توصیه می‌شود از کمترین عرض مسیر مجاز در فرایند ساخت PCB استفاده شود. به‌طور معمول عرض مسیر حداقل 5mil و حداکثر آن کمتر از 10mil در نظر گرفته می‌شود.
  3. فاصله بین مسیرهای سیگنال مجاور بهتر است بیش از سه برابر عرض مسیر باشد؛ در غیر این صورت تداخل بین کلیدهای مجاور افزایش یافته و عملکرد تشخیص لمسی تحت تأثیر قرار می‌گیرد.
  4. تعداد گوشه‌ها و تغییر جهت مسیرها را به حداقل برسانید. در صورت اجبار، از زوایای 45 درجه یا گوشه‌های قوس‌دار استفاده کنید.
  5. مسیرهای لمسی نباید در مجاورت مسیرهای فرکانس بالا قرار گیرند. اگر اجتناب از این موضوع ممکن نبود، مسیرها را عمود بر یکدیگر عبور دهید. در صورت امکان‌نداشتن مسیرکشی عمود، یک مسیر زمین بین آن‌ها قرار دهید.

- **پد لمسی (Touch Pad):**
  1. مسیر سیگنال لمسی را در لایه پشتی پنل لمسی قرار دهید و از طریق یک Via به پد لمسی متصل کنید. این روش احتمال تشخیص ناخواسته تماس انگشت با مسیر را کاهش می‌دهد. بهتر است Via در لبه پد قرار گیرد تا طول مسیر کاهش یابد.
  2. اگر مسیر سیگنال لمسی و پد در یک لایه نیستند، مسیر سیگنال مربوط به پدهای دیگر نباید مستقیماً از زیر پد لمسی عبور کند.
  3. در لایه زیرین پد لمسی از ایجاد سطح مسی خودداری کنید. اگر در لایه خود پد (لایه بالایی) نیاز به مس‌ریزی وجود دارد، معمولاً الگوی مشبک توصیه می‌شود. فاصله پیشنهادی بین پد یا مسیر سیگنال لمسی و زمین حدود 1 تا 2 میلی‌متر است.

### ۴. اصول عملکرد

<div style="text-align: center;">
  <img src="./image/Principle1.jpg" width="500" />
</div>

پد لمسی روی PCB به همراه سطح زمین (GND) مجاور آن، یک خازن انگلی با ظرفیت ***C<sub>P</sub>*** تشکیل می‌دهد. به دلیل وجود ظرفیت خازنی بدن انسان، هنگام تماس انگشت با پد، ظرفیت دیگری با مقدار ***C<sub>F</sub>*** به مدار اضافه می‌شود و ظرفیت کل افزایش می‌یابد. ظرفیت کل ***C<sub>T</sub>*** از رابطه زیر به دست می‌آید:

***C<sub>T</sub> = C<sub>P</sub> + C<sub>F</sub>***

مقدار تغییر ظرفیت ایجادشده یعنی ***C<sub>F</sub>*** تقریباً بین 0.1pF تا 5pF است. این مقدار به عواملی مانند سطح تماس انگشت، فاصله انگشت از پد و ثابت دی‌الکتریک ماده یا محیط بین انگشت و پد بستگی دارد.

<div style="text-align: center;">
  <img src="./image/Principle2.jpg" width="500" />
</div>

با اختصاص‌دادن زمان یکسان برای شارژ خازن پد، می‌توان ولتاژ متناظر با هر پد را از طریق ADC میکروکنترلر اندازه‌گیری و با مقدار ثبت‌شده در حالت بدون لمس مقایسه کرد. با تعریف یک آستانه برای اختلاف این مقادیر، می‌توان تشخیص داد که پد لمس شده است یا خیر.

<div style="text-align: center;">
  <img src="./image/Diagram1.jpg" width="500" />
</div>

این شکل، ساختار نمونه یک صفحه‌کلید لمسی خازنی 3×3 را نشان می‌دهد. هر پد از دو بخش تشکیل شده است که هر بخش به یکی از دو کانال تبدیل لمسی متصل می‌شود. هر کانال تبدیل لمسی به سه پد متصل است. جهت اتصال‌ها به‌صورت متقاطع طراحی شده تا یک ساختار شبکه‌ای ایجاد شود.

پس از روشن‌شدن تراشه، مقدار تبدیل لمسی هر پد در حالت بدون لمس به‌عنوان مقدار مرجع ثبت می‌شود. اگر در همین زمان پدی لمس شده باشد نیز مشکلی ایجاد نمی‌شود؛ زیرا مقدار مرجع پس از هر اسکن به‌روزرسانی می‌شود و به‌تدریج به مقدار مرجع صحیح نزدیک خواهد شد.

<div style="text-align: center;">
  <img src="./image/Diagram2.jpg" width="500" />
</div>

در ابتدای هر چرخه اسکن، نرم‌افزار ابتدا کانال متصل به ستون اول (COL1) را در حالت تبدیل لمسی قرار می‌دهد. تمام کانال‌های دیگر به‌صورت خروجی Push-Pull تنظیم شده و سطح صفر ولت (0V) را تولید می‌کنند. به این ترتیب اختلاف مقدار تبدیل لمسی ستون اول به دست می‌آید. همین فرایند برای ستون‌های COL2 و COL3 و سپس سطرهای ROW1، ROW2 و ROW3 تکرار می‌شود؛ در هر مرحله، کانال موردنظر در حالت تبدیل لمسی و سایر کانال‌ها در حالت خروجی 0V قرار می‌گیرند. در نهایت اختلاف مقدار تبدیل لمسی تمام کانال‌ها محاسبه می‌شود. هرگاه اختلاف مقدار یک کانال ستونی و یک کانال سطری بزرگ‌تر از صفر باشد، نقطه تقاطع آن سطر و ستون به‌عنوان محل لمس‌شده تشخیص داده می‌شود.

### ۵. معرفی ساختار پوشه‌ها

- **hardware**: شامل فایل‌های شماتیک و طراحی سخت‌افزار صفحه‌کلید لمسی خازنی است.
  - **CapTouchKeyboard_v2.0**: شماتیک و PCB مبتنی بر CH585M با رابط‌های BLE، USB و NFC.

- **software**: شامل نمونه نرم‌افزاری (Software DEMO) صفحه‌کلید لمسی خازنی است.
  - **CapTouchKeyboard_v2.2**: نمونه نرم‌افزاری با پشتیبانی از BLE و NFC.
    - **APP**: فایل‌های مربوط به ارتباط صفحه‌کلید BLE HID و پردازش کلیدهای لمسی.
    - **Enc**: فایل‌های مرتبط با الگوریتم اتصال امن.
    - **HAL**: فایل‌های مرتبط با سخت‌افزار.
    - **LIB**: فایل‌های مرتبط با پشته پروتکل BLE.
    - **NFCA_LIB**: فایل‌های مرتبط با پشته پروتکل NFC-A.
    - **PICC_COMMON**: فایل‌های کنترل فرستنده/گیرنده NFC-A در حالت PICC.
    - **Profile**: فایل‌های مرتبط با سرویس صفحه‌کلید BLE HID.
    - **SRC**: کدهای اصلی پروژه.
      - **Ld**: فایل‌های Linker؛ پروژه‌های مختلف از فایل‌های متفاوتی استفاده می‌کنند.
      - **RVMSIS**: فایل‌های سرآیند سیستم هسته.
      - **Startup**: فایل‌های راه‌اندازی؛ پروژه‌های مختلف ممکن است فایل راه‌اندازی متفاوتی داشته باشند.
      - **StdPeriphDriver**: فایل‌های منبع و سرآیند درایورهای پایه تجهیزات جانبی.
    - **T2T_COMMON**: فایل‌های پیکربندی NFC-A در حالت T2T.
    - **TKYLIB**: فایل‌های کتابخانه کلید لمسی.

### ۶. راهنمای استفاده

#### ۶.۱. توسعه نرم‌افزار

محیط توسعه مورد استفاده در این پروژه [MounRiver Studio](http://www.mounriver.com/) است. پروژه‌های موجود در پوشه **software** را می‌توان مستقیماً با **MounRiver Studio** باز کرد. فایل HEX تولیدشده پس از کامپایل، از طریق نرم‌افزار [WCHISPTool](https://www.wch-ic.com/downloads/WCHISPTool_Setup_exe.html) روی برد پروگرام می‌شود.

#### ۶.۲. پروگرام‌کردن CH585

1. صفحه‌کلید را از طریق کابل USB به رایانه متصل کنید. در این مرحله CH585 نباید روشن باشد.
2. دکمه شماره ① را نگه دارید و کلید برق شماره ② را روشن کنید تا تغذیه CH585 وصل شود. در این حالت CH585 برنامه Bootloader را اجرا می‌کند و رایانه یک دستگاه USB را شناسایی خواهد کرد. پس از شناسایی دستگاه می‌توانید دکمه را رها کنید.
3. نرم‌افزار WCHISPTool به‌صورت خودکار CH585 را شناسایی کرده (③) و رابط دانلود را باز می‌کند.
4. فایل Firmware با فرمت HEX یا BIN را که توسط محیط توسعه تولید شده است انتخاب کنید (④).
5. روی گزینه Download کلیک کنید تا برنامه روی CH585 نوشته شود (⑤).

<img src=./image/Download1_v2.0.jpg width=51% /><img src=./image/Download2_v2.0.jpg width=49% />

### ۷. تصاویر و دیاگرام‌های راهنما

تصاویر شماتیک، جانمایی PCB، اصول عملکرد و مراحل پروگرام در بخش‌های مرتبط همین راهنما قرار گرفته‌اند.

### ۸. تهیه و تدوین

**معمار الکترونیک صنعت / MEMAR ELECTRONIC SANAT (MES)**

*همراه شما در مسیر طراحی و ساخت مدارهای مطمئن*

- [GitHub](https://github.com/MEMAR-ELECTRONIC-SANAT)
- [Telegram](https://t.me/Memar_Electronic)
- [Instagram](https://www.instagram.com/Memar.Electronic)

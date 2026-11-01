# حریم خصوصی Dr.Net

[English below](#privacy--drnet)

خلاصه: Dr.Net هیچ اطلاعاتی از شما جمع نمی‌کند و جایی نمی‌فرستد. حساب کاربری ندارد، ابزار آمارگیری و تبلیغ ندارد، و نمی‌داند شما چه سایتی باز می‌کنید.

## چیزهایی که برنامه ندارد

- **هیچ ابزار آمار، ردیابی یا تبلیغ** (Firebase، Crashlytics، Google Analytics و مانند این‌ها) داخل برنامه نیست.
- **هیچ شناسه‌ای از گوشی خوانده نمی‌شود:** نه IMEI، نه شماره تلفن، نه ANDROID_ID، نه حساب‌های گوگل، نه مخاطبین.
- **موقعیت مکانی شما جمع نمی‌شود.** مجوز موقعیت فقط وقتی پرسیده می‌شود که خودتان بخواهید اسم وای‌فای را در صفحه‌ی اتصال ببینید (اندروید اسم وای‌فای را پشت این مجوز گذاشته). آن اسم فقط روی صفحه‌ی خودتان نشان داده می‌شود.
- **تاریخچه‌ی وب‌گردی، لایک، کامنت یا محتوای صفحه‌ها** نه دیده، نه ذخیره و نه فرستاده می‌شود.

## ترافیک و DNS شما

در هر روش اتصال، DNS هم از داخل تونل می‌رود و بیرون از آن نشت نمی‌کند:

| روش | DNS از کجا می‌رود |
|---|---|
| کانفیگ‌ها | با DNS-over-HTTPS از داخل تونل. فقط سایت‌های ایرانی (`.ir` و چند سایت ایرانی دیگر) مستقیم باز می‌شوند تا سریع بمانند؛ این را در تنظیمات DNS می‌توانید خاموش کنید. |
| ماسک، وایرگارد، وارپ در وارپ، آمنزیا | از داخل تونل وارپ. DNS اپراتور کنار گذاشته می‌شود. |
| سایفون | از داخل تونل سایفون. |
| تور | فقط از DNS خود تور. |
| لنترن | از داخل تونل لنترن؛ اسم سایت‌ها روی سرورهای لنترن به آدرس تبدیل می‌شود. |
| رله گوگل | هیچ اسمی روی گوشی به آدرس تبدیل نمی‌شود: به برنامه‌ها آدرس ساختگی داده می‌شود و اسم‌ها را اسکریپت گوگل خودتان آن طرف تبدیل می‌کند. |

اگر روشی IPv6 نداشته باشد، IPv6 بسته می‌شود یا به داخل تونل می‌رود تا از کنار تونل بیرون نرود.

**کانفیگ‌های رایگان:** فقط اگر خودتان از دکمه‌ی + در صفحه‌ی کانفیگ‌ها اضافه‌شان کنید. این‌ها سرورهای عمومی‌اند که دیگران راه انداخته‌اند، نه Dr.Net. اطلاعات شما مثل همیشه رمزشده می‌ماند، ولی صاحب هر سرور می‌تواند ببیند به چه سایت‌هایی وصل می‌شوید. با حذف دسته‌شان دیگر استفاده نمی‌شوند.

**دامین فرانتینگ:** برای اینکه گوگل، یوتیوب و اینستاگرام را بدون سرور باز کند، یک گواهی روی خود گوشی شما ساخته می‌شود. کلید آن هیچ‌وقت از گوشی بیرون نمی‌رود. ترافیک فقط از روی گوشی رد می‌شود و چیزی از آن ذخیره یا فرستاده نمی‌شود. با خاموش کردن این گزینه و حذف گواهی از تنظیمات اندروید همه چیز به حالت قبل برمی‌گردد.

**رله گوگل (ابزار):** مرورگر شما از راه یک اسکریپت گوگل که خودتان در حساب خودتان ساخته‌اید (و اگر روشن کنید، یک ورکر روی حساب کلودفلر خودتان) به اینترنت می‌رسد. برای خواندن درخواست مرورگر، یک گواهی روی خود گوشی ساخته می‌شود و کلیدش هیچ‌وقت از گوشی بیرون نمی‌رود. هر صفحه‌ای که باز کنید از اسکریپت شما در حساب گوگل خودتان می‌گذرد؛ یعنی گوگل (و کلودفلر، اگر روشن باشد) آن را در حساب شما می‌بیند، نه Dr.Net. رمز رله و شناسه‌ی اسکریپت‌ها با کلید Keystore رمز می‌شوند و جایی فرستاده نمی‌شوند. با «پاک کردن رله» و حذف گواهی از تنظیمات اندروید همه چیز برمی‌گردد.

## گزارش اتصال

گزارش اتصال فقط در حافظه‌ی برنامه است (۱۰۰ خط آخر) و با بسته شدن برنامه پاک می‌شود. در نسخه‌ی منتشرشده اسم سایت‌ها و آدرس‌ها در آن ثبت نمی‌شود.

## گزارش مشکل

فقط وقتی خودتان «گزارش مشکل» را بزنید، تلگرام با یک پیام آماده باز می‌شود: مدل گوشی، نسخه‌ی اندروید، اسم اپراتور، روش اتصال، زمان، و چند خط آخر گزارش اتصال. لینک‌ها، کلیدها و شناسه‌ها از آن حذف شده‌اند. پیام را قبل از فرستادن می‌بینید و می‌توانید نفرستید.

## برنامه خودش به کجا وصل می‌شود

- **GitHub (و آینه‌اش jsDelivr):** دیدن نسخه‌ی جدید برنامه، لیست عمومی دستگاه‌های وارپ، و اگر اضافه‌شان کرده باشید، فهرست کانفیگ‌های رایگان.
- **سرورهای سایفون و پل‌های تور:** گرفتن لیست سرورها و پل‌ها، برای همان روش‌ها.
- **سرورهای لنترن (فقط اگر روش «لنترن» را بزنید):** ساختن یک حساب رایگان ناشناس برای این نصب، گرفتن فهرست سرورها (از راه CDNهای پوششی و Cloudflare) و سهمیه‌ی رایگان. موتور لنترن فقط یک شناسه‌ی تصادفیِ مخصوص خودش، زبان و منطقه‌ی زمانی را می‌فرستد و تله‌متری لنترن خاموش است. مثل هر سرویس VPN، سرورهای لنترن آدرس گوشی و سایت‌هایی را که از آن‌ها باز می‌شوند می‌بینند. موتور لنترن برای دانستن آدرس اینترنتی خودش مستقیم از checkip.amazonaws.com، icanhazip.com، ipinfo.io و سرورهای STUN کلادفلر و Nextcloud می‌پرسد.
- **Cloudflare:** ساخت هویت وارپ؛ و اگر پنل دارید، فقط حساب و ورکرهای خود شما.
- **script.google.com (فقط اگر «رله گوگل» را راه بیندازید):** «سنجش رله» به اسکریپت خودتان یک درخواست آزمایشی می‌فرستد، و خود رله ترافیک مرورگر را با اتصالی به یک آدرس گوگل (با نام www.google.com در دست‌دهی) به همان اسکریپت می‌رساند. اگر «شتاب‌دهنده‌ی کلودفلر» را روشن کنید، برنامه با توکن خودتان یک ورکر روی حساب کلودفلر خودتان می‌سازد.
- **ipwho.is یا ifconfig.co:** از داخل تونل، فقط برای نشان دادن کشور خروجی.
- **عیب‌یابی و تست سرعت:** فقط وقتی خودتان اجرا کنید، به همان سایت‌هایی که تست می‌شوند.

## اطلاعات ذخیره‌شده روی گوشی

کانفیگ‌ها، تنظیمات و اطلاعات حساب‌های پنل فقط روی گوشی خودتان می‌ماند. توکن‌ها با کلید Keystore اندروید رمز می‌شوند و هیچ‌چیز از برنامه در پشتیبان‌گیری گوگل نمی‌رود.

---

# Privacy — Dr.Net

In short: Dr.Net collects nothing about you and sends nothing anywhere. It has no account, no analytics, no ads, and it does not know which sites you open.

## What the app does not have

- **No analytics, tracking or ad SDK** (no Firebase, Crashlytics, Google Analytics or similar).
- **No device identifiers are read:** no IMEI, phone number, ANDROID_ID, Google accounts or contacts.
- **Your location is not collected.** The location permission is asked only when you choose to see the Wi-Fi name on the connection screen (Android gates the Wi-Fi name behind it), and that name is only shown on your own screen.
- **Your browsing history, likes, comments or page contents** are never seen, stored or sent.

## Your traffic and DNS

In every connection method DNS travels inside the tunnel and does not leak around it:

| Method | Where DNS goes |
|---|---|
| Configs | DNS over HTTPS inside the tunnel. Only Iranian sites (`.ir` and a short list) go direct so they stay fast; this can be turned off in the DNS settings. |
| MASQUE, WireGuard, WARP-in-WARP, AmneziaWG | Inside the WARP tunnel; the carrier's DNS is left out. |
| Psiphon | Inside the Psiphon tunnel. |
| Tor | Tor's own DNS only. |
| Lantern | Inside the Lantern tunnel; names are resolved on Lantern's servers. |
| Google relay | No name is resolved on the phone: apps are given made-up addresses and the names are resolved on the other side by your own Google script. |

Where a method has no IPv6, IPv6 is blocked or routed into the tunnel, so it never leaves beside it.

**Free configs:** only if you add them yourself, from the + on the configs page. They are public servers run by other people, not by Dr.Net. Your traffic stays encrypted as always, but whoever runs a server can see which sites you connect to. Deleting their batch stops them being used.

**Domain fronting:** to reach Google, YouTube and Instagram without a server, a certificate is created on your own phone. Its key never leaves the phone; traffic only passes through the phone and nothing of it is stored or sent. Turning the option off and removing the certificate in Android's settings undoes it completely.

**Google relay (a tool):** your browser reaches the internet through a Google script that you made yourself in your own account (and, if you turn it on, a worker on your own Cloudflare account). To read the browser's requests a certificate is made on the phone itself, and its key never leaves it. Every page you open passes through your script in your Google account - so Google (and Cloudflare, if it is on) sees it in your account, not Dr.Net. The relay's key and the scripts' ids are encrypted with an Android Keystore key and are not sent anywhere. "Remove the relay", and removing the certificate in Android's settings, undoes it.

## Connection log

The connection log lives in the app's memory only (the last 100 lines) and is gone when the app closes. In a release build it does not record site names or addresses.

## Problem reports

Only when you tap "Report a problem", Telegram opens with a prepared message: phone model, Android version, operator name, connection method, time, and the last lines of the connection log, with links, keys and IDs removed. You see the message before sending it and can choose not to.

## Where the app itself connects

- **GitHub (and its jsDelivr mirror):** checking for a new version of the app, the public list of WARP devices, and, if you added them, the free config list.
- **Psiphon's servers and Tor's bridge service:** fetching server and bridge lists for those methods.
- **Lantern's servers (only if you use the Lantern method):** making an anonymous free account for this install, fetching Lantern's server list (over domain-fronting CDNs and Cloudflare) and the free allowance. Lantern's engine sends only a random id of its own, the language and the time zone, and Lantern's telemetry is off. Like any VPN's, Lantern's servers see the phone's address and the sites opened through them. To learn its own public address, Lantern's engine asks checkip.amazonaws.com, icanhazip.com, ipinfo.io and Cloudflare's and Nextcloud's STUN servers directly.
- **Cloudflare:** registering a WARP identity; and, if you use a panel, only your own account and workers.
- **script.google.com (only if you set up the Google relay):** "Test the relay" sends your own script a test request, and the relay itself carries the browser's traffic to that script over a connection to a Google address (with www.google.com as the name in the handshake). If you turn on the Cloudflare accelerator, the app uses your own token to make a worker on your own Cloudflare account.
- **ipwho.is or ifconfig.co:** through the tunnel, only to show the exit country.
- **Diagnosis and speed tests:** only when you run them, to the sites being tested.

## Data stored on the phone

Configs, settings and panel account details stay on your phone. Tokens are encrypted with a key in the Android Keystore, and nothing of the app goes into Google backups.

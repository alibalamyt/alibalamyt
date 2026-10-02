# راهنمای راه‌اندازی

## ۱) اجرای فوری روی گوشی (بدون اتصال گوگل)
فایل index.html را در مرورگر گوشی باز کنید. همه‌چیز خودکار روی گوشی ذخیره می‌شود.
برای نسخه پشتیبان: تنظیمات > دریافت فایل پشتیبان.

## ۲) نسخه قابل نصب روی گوشی (رایگان، بدون نیاز به کامپیوتر)
۱. در گوشی یک حساب GitHub بسازید و یک مخزن (Repository) عمومی بسازید.
۲. با گزینه Add file > Upload files چهار فایل index.html، manifest.json، sw.js و icon.svg را آپلود کنید.
۳. در Settings > Pages شاخه main را فعال کنید. بعد از چند دقیقه آدرس https://USERNAME.github.io/REPO پدید می‌آید.
۴. آدرس را در Chrome باز کنید و Add to Home screen (یا Install app) را بزنید. مثل یک اپ نصب می‌شود و آفلاین هم کار می‌کند.
(جایگزین: سایت Netlify Drop یا Cloudflare Pages)

## ۳) اتصال به حساب گوگل (Google Drive)
فقط روی آدرس https (مرحله ۲) کار می‌کند، نه روی فایل محلی.
۱. console.cloud.google.com > پروژه جدید.
۲. APIs & Services > Library > Google Drive API را Enable کنید.
۳. OAuth consent screen: نوع External، ایمیل خودتان را در Test users اضافه کنید.
۴. Credentials > Create credentials > OAuth client ID > Web application.
۵. در Authorized JavaScript origins آدرس سایت خود را بدون اسلش آخر بنویسید (مثل https://USERNAME.github.io).
۶. Client ID را در برنامه، بخش تنظیمات، وارد کنید و «اتصال و همگام‌سازی» را بزنید.
روی گوشی و کامپیوتر با همان Client ID وصل شوید تا داده‌ها بین هر دو یکی شود.
داده‌ها فقط در پوشه خصوصی برنامه در Drive شما ذخیره می‌شوند (scope: drive.appdata).

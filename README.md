# راه‌اندازی برنامه‌ریز

## ۱) انتشار (رایگان، از خود گوشی)
چهار فایل index.html، manifest.json، sw.js و icon.svg را در یک مخزن GitHub آپلود کنید و Settings > Pages را روی شاخه main فعال کنید (یا Netlify Drop).
آدرس https://USERNAME.github.io/REPO را در Chrome باز کنید و Add to Home screen بزنید.

## ۲) ورود با گوگل برای همه کاربران
1. console.cloud.google.com > پروژه جدید > APIs & Services > Library > Google Drive API را Enable کنید.
2. OAuth consent screen: نوع External. اطلاعات پایه را پر کنید و روی Publish app (In production) بزنید؛ اسکوپ drive.appdata حساس نیست و نیاز به تایید گوگل ندارد، پس هر کسی با Gmail می‌تواند وارد شود.
3. Credentials > Create credentials > OAuth client ID > Web application. در Authorized JavaScript origins آدرس سایت را بدون اسلش آخر بنویسید (مثل https://USERNAME.github.io).
4. Client ID را در index.html، خط اول اسکریپت (CLIENT_ID)، قرار دهید و دوباره آپلود کنید. (یا هنگام اولین ورود در صفحه لاگین وارد کنید.)
هر کاربر داده‌ها را فقط در Drive شخصی خودش (پوشه خصوصی برنامه) دارد و سرور یا هزینه‌ای در کار نیست.

## ۳) ثبت خودکار از پیامک
مرورگر و PWA اجازه خواندن مستقیم پیامک را ندارند. راه‌ها داخل برنامه، بخش «پیامک» توضیح داده شده: چسباندن، اشتراک‌گذاری (Share) و اتوماسیون با MacroDroid/Tasker.

# سطح‌های اجرایی در سیستم‌های یونیکس/لینوکس

در سیستم‌عامل‌های مبتنی بر یونیکس و لینوکس، **سطح‌های اجرایی** نشان‌دهنده وضعیت کنونی سیستم از نظر فرآیندهای در حال اجرا و سطح دسترسی‌ها هستند. هر سطح اجرا با یک عدد مشخص می‌شود و هر یک از این سطوح تعیین می‌کنند که سیستم چگونه باید عمل کند.

## سطوح مختلف اجرا

### سطح اجرا 0
- **معنی:** خاموش کردن سیستم
- **کاربرد:** این سطح برای خاموش کردن کامل سیستم استفاده می‌شود. تمامی فرآیندها متوقف می‌شوند و سیستم به صورت امن خاموش می‌شود.

### سطح اجرا 1
- **معنی:** حالت تک‌کاربره
- **کاربرد:** برای عملیات نگهداری و بازیابی که نیاز به دسترسی محدود به سیستم دارد. تنها کاربر اصلی (Root) می‌تواند وارد شود و دسترسی شبکه غیرفعال است.

### سطح اجرا 2
- **معنی:** حالت چندکاربره بدون شبکه
- **کاربرد:** چند کاربر می‌توانند وارد شوند، اما سرویس‌های شبکه (مثل NFS) غیرفعال هستند.

### سطح اجرا 3
- **معنی:** حالت چندکاربره با شبکه
- **کاربرد:** همه کاربران می‌توانند به سیستم دسترسی داشته باشند و تمامی سرویس‌های شبکه فعال هستند. معمولاً برای سرورها استفاده می‌شود.

### سطح اجرا 4
- **معنی:** تعریف نشده یا حالت کاربر سفارشی
- **کاربرد:** برای استفاده سفارشی که می‌تواند توسط مدیر سیستم تعریف شود. در بسیاری از توزیع‌ها استفاده نمی‌شود.

### سطح اجرا 5
- **معنی:** حالت چندکاربره با شبکه و محیط گرافیکی
- **کاربرد:** شبیه به سطح 3 است اما علاوه بر آن، محیط گرافیکی (مثل X Window System) نیز بارگذاری می‌شود. معمولاً برای دسکتاپ‌ها استفاده می‌شود.

### سطح اجرا 6
- **معنی:** راه‌اندازی مجدد سیستم
- **کاربرد:** این سطح برای ری‌استارت کردن سیستم استفاده می‌شود. همه فرآیندها متوقف می‌شوند و سپس سیستم مجدداً راه‌اندازی می‌شود.

## Systemd و سطوح اجرا

در سیستم‌های مدرن لینوکس که از سیستم مدیریت سرویس **systemd** استفاده می‌کنند، مفهوم سطوح اجرا با "اهداف" (targets) جایگزین شده‌اند. هر هدف عملکرد مشابهی با سطوح اجرایی سنتی دارد، اما انعطاف‌پذیری بیشتری را ارائه می‌دهد. برای مثال:

- **poweroff.target** معادل سطح اجرا 0
- **rescue.target** معادل سطح اجرا 1
- **multi-user.target** معادل سطح اجرا 3
- **graphical.target** معادل سطح اجرا 5
- **reboot.target** معادل سطح اجرا 6

Systemd از این اهداف استفاده می‌کند تا سیستم را به حالت‌های مختلف بوت کند یا از آن خارج کند.
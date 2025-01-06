فایل .bash_profile یک فایل پیکربندی در سیستم‌های یونیکس و لینوکس است که هنگام ورود کاربر به سیستم از طریق پوسته (Shell) اجرا می‌شود. این فایل معمولاً در دایرکتوری خانگی هر کاربر قرار دارد و برای پیکربندی محیط شل استفاده می‌شود. bash_profile به طور خاص برای پوسته‌ی bash استفاده می‌شود که یکی از رایج‌ترین پوسته‌های مورد استفاده در این سیستم‌ها است.

## کاربردهای فایل .bash_profile
تنظیم متغیرهای محیطی: در .bash_profile، کاربران می‌توانند متغیرهای محیطی مانند PATH، HOME، USER و دیگر متغیرهای مورد نیاز برای اجراهای سیستم و برنامه‌های کاربردی را تنظیم کنند.

راه‌اندازی نرم‌افزارها: این فایل می‌تواند برای راه‌اندازی برنامه‌ها یا سرویس‌هایی که کاربر نیاز دارد هنگام ورود به سیستم اجرا شوند، استفاده شود. مثلاً اجرای یک دیمون خاص یا راه‌اندازی یک محیط توسعه.

سفارشی‌سازی محیط شل: کاربران می‌توانند تنظیمات پوسته‌ی خود را مانند تغییر اعلان‌ها (prompt)، تنظیمات تاریخچه‌ی دستورات و سفارشی‌سازی دیگر را در این فایل تعریف کنند.

منابع‌دهی به فایل‌های پیکربندی دیگر: .bash_profile می‌تواند فایل‌های پیکربندی دیگر مانند .bashrc یا .bash_aliases را منابع‌دهی کند تا تنظیمات و تنظیمات سفارشی‌سازی بیشتری اعمال شود.


### نمونه‌ای از یک فایل .bash_profile
```bash
export PATH=$PATH:$HOME/bin

# تنظیم تاریخچه دستورات
export HISTSIZE=1000
export HISTFILESIZE=2000

# نمایش یک پیام خوش‌آمدگویی
echo "Welcome to your shell session, $USER!"

# منابع‌دهی به فایل .bashrc برای تنظیمات بیشتر
if [ -f ~/.bashrc ]; then
    . ~/.bashrc
fi
```

### تفاوت بین .bash_profile و .bashrc

## .bashrc
موقعیت استفاده: هر بار که یک ترمینال جدید باز می‌شود، اجرا می‌شود.

کاربرد اصلی: تنظیمات سریع برای پوسته‌ی bash مانند aliasها، متغیرهای محیطی، و تنظیمات دیگر.

مخاطب: برای جلسات تعاملی که کاربر مستقیماً دستورات را وارد می‌کند.
## .bash_profile
موقعیت استفاده: زمانی که کاربر به سیستم وارد می‌شود، اجرا می‌شود.

کاربرد اصلی: تنظیم متغیرهای محیطی و راه‌اندازی برنامه‌هایی که باید هنگام ورود به سیستم اجرا شوند.

مخاطب: بیشتر برای تنظیمات کلی سیستم و محیط کاربری که نیاز است هنگام ورود کاربر به سیستم اعمال شوند.


## تفاوت کلیدی
زمان اجرا: .bashrc در هر ترمینال جدید، و .bash_profile فقط هنگام ورود به سیستم اجرا می‌شود.

محتوا: .bash_profile بیشتر برای تنظیمات اولیه و محیطی است، در حالی که .bashrc برای تنظیمات پوسته و جلسات تعاملی است.
# دستور `uname` و اطلاعات کرنل در سیستم‌های یونیکس و لینوکس

## دستور `uname`

دستور `uname` برای نمایش اطلاعاتی درباره سیستم عامل و کرنل (هسته) سیستم استفاده می‌شود. این دستور می‌تواند نام سیستم، نسخه کرنل، نسخه سیستم‌عامل و نوع ماشین را نمایش دهد.

### سینتکس

```bash
uname [OPTION]...
```

### گزینه‌های معمول uname

-s: نمایش نام سیستم عامل.

-n: نمایش نام میزبان (hostname).

-r: نمایش نسخه کرنل.

-v: نمایش تاریخ و زمان کامپایل کرنل.

-m: نمایش نوع معماری ماشین (مثلاً x86_64).

-p: نمایش نوع پردازنده (در برخی سیستم‌ها ممکن است نتیجه نداشته باشد).

-i: نمایش پلتفرم سخت‌افزاری.

-o: نمایش نام سیستم‌عامل.

-a: نمایش تمامی اطلاعات بالا به صورت یکجا.


## دستورات دیگر برای بدست آوردن اطلاعات کرنل

علاوه بر uname، دستورات زیر نیز اطلاعات بیشتری درباره کرنل و سیستم‌عامل ارائه می‌دهند:

دستور cat /proc/version: این دستور اطلاعات دقیق‌تری درباره نسخه کرنل و نسخه GCC که برای کامپایل کرنل استفاده شده است، ارائه می‌دهد.


دستور cat /etc/os-release: اطلاعاتی در مورد توزیع لینوکس، شامل نام توزیع، نسخه و سایر مشخصات.


دستور lsb_release -a: اطلاعات جامع‌تر در مورد نسخه توزیع لینوکس.


دستور hostnamectl: ارائه اطلاعات کامل‌تر از جمله نسخه سیستم‌عامل، کرنل، معماری و سایر جزئیات.


استفاده از این دستورات به شما کمک می‌کند تا درک بهتری از سیستم و کرنل خود داشته باشید و در صورت نیاز به دیباگ یا پشتیبانی، اطلاعات لازم را در اختیار داشته باشید.


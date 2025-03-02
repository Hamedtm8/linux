# دستور `route` در لینوکس

دستور `route` برای مشاهده و تنظیم جدول مسیریابی شبکه در سیستم‌عامل‌های مشابه یونیکس و لینوکس استفاده می‌شود. جدول مسیریابی تعیین می‌کند که داده‌ها چگونه از طریق شبکه به مقصد خود هدایت شوند.

## مفاهیم اصلی

- **مقصد (Destination):** آدرس شبکه یا هاست مقصد.
- **دروازه (Gateway):** آدرس روتر یا دستگاهی که داده‌ها را به شبکه دیگر هدایت می‌کند.
- **ماسک شبکه (Netmask):** تعیین محدوده شبکه مقصد.
- **رابط (Interface):** رابط شبکه محلی که داده‌ها از آن ارسال یا دریافت می‌شوند.

## دستورات اصلی `route`

### نمایش جدول مسیریابی

برای مشاهده جدول مسیریابی فعلی:

```bash
route -n
```

فلگ -n باعث می‌شود تا آدرس‌ها به صورت عددی نمایش داده شوند، که سرعت نمایش اطلاعات را افزایش می‌دهد.



### افزودن یک مسیر جدید

برای افزودن یک مسیر جدید به جدول مسیریابی:

```bash
sudo route add -net <network_address> netmask <netmask> gw <gateway> dev <interface>
```

<network_address>: آدرس شبکه مقصد.

<netmask>: ماسک شبکه برای مقصد.

<gateway>: آدرس دروازه‌ای که باید بسته‌ها از آن عبور کنند.

<interface>: رابط شبکه‌ای که باید از آن استفاده شود.

### حذف یک مسیر

```bash
sudo route del -net <network_address> netmask <netmask> dev <interface>
```


### تنظیم Gateway پیش‌فرض

```bash
sudo route add default gw <gateway> dev <interface>
```


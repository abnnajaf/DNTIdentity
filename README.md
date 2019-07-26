﻿<div dir="rtl">

سفارشی سازی ASP.NET Core Identity SDK-2.2.300
=======



![dnt-identity-02](/src/ASPNETCoreIdentitySample/wwwroot/images/dnti02.png)



![dnt-identity-01](/src/ASPNETCoreIdentitySample/wwwroot/images/dnti01.png)




برای اجرای این پروژه
------
- ابتدا نیاز است بر اساس شماره [SDK](https://dotnet.microsoft.com/download) ای که در عنوان پروژه مشاهده می‌کنید، نگارش متناظری را نصب کنید. به این معنا که این پروژه وابستگی خاصی به نگارش ویژه‌ای از Visual Studio ندارد. همینقدر که NET Core. را نصب کنید، می‌توانید آن‌را اجرا کنید. برای توسعه‌ی این برنامه از [VSCode](https://www.dotnettips.info/learningpaths/details/60) استفاده شده‌است. شماره نگارش SDK این پروژه توسط فایل [global.json‌](https://github.com/VahidN/DNTIdentity/blob/master/global.json#L3) قفل شده‌است تا اگر نگارش‌های دیگری را نصب کردید، با آن تداخل پیدا نکنند.
- یک نکته: اگر قصد کار با [ویژوال استودیو 2017](https://github.com/dotnet/announcements/issues/108) را دارید، این برنامه دیگر از SDKهای جدید پشتیبانی نمی‌کند و حتما باید از نگارش 2019 آن استفاده کنید و یا می‌توانید شماره نگارش SDK را در فایل [global.json‌](https://github.com/VahidN/DNTIdentity/blob/master/global.json#L3) به شماره نگارشی که [ویژوال استودیو 2017](https://github.com/dotnet/announcements/issues/108) شما پشتیبانی می‌کند تغییر داده و سپس کار ری‌استور پروژه را انجام دهید.
- سپس آخرین نگارش [NodeJS](https://nodejs.org/en/download/current/) را نیز نصب کنید. از npm آن برای دریافت کتابخانه‌های سمت کلاینت پروژه که در فایل [package.json](https://github.com/VahidN/DNTIdentity/blob/master/src/ASPNETCoreIdentitySample/package.json) ذکر شده‌اند، استفاده می‌شود.
- بانک اطلاعاتی پیش‌فرض برنامه [LocalDB](https://www.dotnettips.info/post/2409) است که [از اینجا](https://download.microsoft.com/download/E/F/2/EF23C21D-7860-4F05-88CE-39AA114B014B/SqlLocalDB.msi) قابل دریافت و نصب است (البته می‌توانید حالت in-memory را نیز در فایل [appsettings.json](https://github.com/VahidN/DNTIdentity/blob/master/src/ASPNETCoreIdentitySample/appsettings.json#L47) انتخاب کنید که وابستگی به بانک اطلاعاتی خاصی ندارد).
- سپس فایل [restore.bat](https://github.com/VahidN/DNTIdentity/blob/master/src/ASPNETCoreIdentitySample/_0-restore.bat) را اجرا کنید تا تمام وابستگی‌های سمت سرور و کلاینت پروژه، دریافت و نصب شوند.
- در آخر فایل [dotnet_run.bat](https://github.com/VahidN/DNTIdentity/blob/master/src/ASPNETCoreIdentitySample/_1-dotnet_run.bat) را اجرا کنید، تا پروژه در آدرس https://localhost:5001 قابل دسترسی شود.  مشخصات پیش‌فرض ورود به سیستم را در فایل [appsettings.json](https://github.com/VahidN/DNTIdentity/blob/master/src/ASPNETCoreIdentitySample/appsettings.json) می‌توانید مشاهده کنید.





دارای قسمت‌های
------
ثبت نام به همراه تائید ایمیل، لاگین، برگه‌ی اطلاعات کاربری، تنظیمات کاربری، تغییر کلمه‌ی عبور، بازیابی کلمه‌ی عبور، اعتبارسنجی دو مرحله‌ای توسط ایمیل، مدیریت کاربران و نقش‌های ثابت. مدیریت سطوح دسترسی پویای به صفحات و مشاهده‌ی لاگ خطاهای برنامه.



با امکانات
----------
* اضافه کردن Remote validationها به قسمت‌های ثبت نام، تغییر کلمه‌ی عبور، بازیابی کلمه‌ی عبور و تنظیمات کاربری
* پیاده سازی امکان ویرایش تنظیمات کاربری به همراه آپلود تصویر شخص و فیلدهای سفارشی مانند تاریخ تولد، مکان و امثال آن
* پیاده سازی کامل قسمت‌های ارسال ایمیل و همچنین پشتیبانی از تهیه‌ی قالب‌های ایمیل توسط Razor Views
* پیاده سازی مدیریت نقش‌های ثابت سیستم
* پیاده سازی جزئیات مدیریت کاربران به همراه جستجوی آن‌ها
* پیاده سازی سطوح دسترسی پویای به صفحات مختلف سایت به کمک ویژگی جدید پالیسی در ASP.NET Core
* پیاده سازی مفهوم Security Trimming جهت عدم نمایش لینک‌هایی که کاربر جاری به آن‌ها دسترسی پویا ندارد
* پیاده سازی ویجت کاربران آنلاین
* پیاده سازی ویجت تولدهای امروز با سفارشی سازی موجودیت و همچنین سرویس مدیریت کاربران سایت



سفارشی سازی تنظیمات کلاینت
--------
* استفاده از بوت استرپ 3 راست به چپ
* استفاده از قلم فارسی مناسب
* تنظیم Unobtrusive jQuery Ajax & Validation
* تنظیم Bundling & minification اسکریپت‌ها و شیوه‌نامه‌ها



سفارشی سازی لایه‌های برنامه
------
* جدا سازی کامل لایه‌ها به همراه تزریق وابستگی‌ها و پیاده سازی الگوی واحد کار
* انتقال تمام مباحث مدیریت کاربران به یک Area جدید به نام Identity جهت سهولت استفاده‌ی از آن در سایر برنامه‌ها



سفارشی سازی لایه‌ها‌ی دسترسی به داده‌ها و موجودیت‌ها
--------
* سفارشی سازی موجودیت‌های Identity جهت افزودن خواصی بیشتر و همچنین تغییر نوع کلید اصلی جداول به int
* DbContext مورد استفاده، به لایه‌ی مخصوص خود انتقال یافته و همچنین تنظیمات Migrations نیز از برنامه‌ی اصلی وب خارج و به این لایه منتقل شده‌اند.
* سفارشی سازی کامل DbContext برنامه جهت افزودن امکان استفاده‌ی از بانک‌های اطلاعاتی مختلف، سفارشی سازی نام جداول Identity، افزودن Shadow properties ویژه‌ی ثبت جزئیات کاربر ثبت کننده و ویرایش کننده‌ی رکوردها، به همراه IP‌ و زمان تغییرات.
* یک دست سازی ی و ک ثبت شده‌ی توسط EF Core با سفارشی سازی Change Tracker آن



سفارشی سازی لایه‌ی سرویس‌های Identity
--------
* پیاده سازی متد Seed جهت افزودن کاربر ادمین و همچنین نقش آن به سیستم در اولین بار اجرای برنامه
* سفارشی سازی تمام سرویس‌های توکار Identity مانند مدیریت کاربران و نقش‌ها
* سفارشی سازی مدیریت Claims جهت افزودن مسیر تصویر شخص جهت کاهش رفت و برگشت به بانک اطلاعاتی
* سفارشی سازی نرمال ساز ایمیل‌ها و همچنین نام کاربری جهت اعمال یک دست سازی به ایمیل‌هایی یکسان با چند نوع قابل قبول مانند ایمیل‌های جی‌میل
* پیاده سازی یک Ticket Store مبتنی بر بانک اطلاعاتی جهت کاهش اندازه‌ی کوکی‌های حاصل از تعریف سطوح دسترسی پویای به صفحات مختلف برنامه
* سفارشی سازی اعتبارسنجی کلمات عبور برنامه جهت عدم قبول مواردی ساده و یا قابل حدس
* تدارک یک لاگر پیاده سازی شده‌ی با EF Core جهت ثبت خطاهای برنامه به همراه صفحه‌ای مدیریتی مخصوص جهت مشاهده‌ی این خطاها
* پیاده سازی سرویس ذخیره سازی سابقه‌ی کلمات عبور کاربران و ارائه‌ی اخطارهای لازم به آن‌ها
* سفارشی سازی طول عمر توکن صادر شده‌ی جهت تائید ایمیل شخص در حین ثبت نام که به صورت پیش فرض تنها یک روز است
* انتقال تمام تنظیمات Identity و برنامه به یک فایل json، جهت سهولت تغییر آن‌ها بدون نیازی به تغییری در برنامه
* تهیه‌ی یک رجیستری جهت سهولت افزودن تمام تنظیمات تزریق وابستگی‌های سفارشی سازی شده‌ی برنامه توسط یک متد در کلاس آغازین آن



بومی سازی
-------
* فارسی بودن تمام قسمت‌های برنامه به همراه کلیه‌ی خطاها و اخطارهای توکار Identity



آزمون‌های واحد
------
* تهیه و تنظیم کامل زیر ساخت نوشتن آزمون‌های واحد درون حافظه‌ای EF Core به کمک فریم ورک MS Test



پیش از مشارکت
------
[« آشنایی با ساختار یک Pull Request خوب »](http://www.dotnettips.info/post/2033)


------------------------------------------------------------------------------------------------------


جزئیات و توضیحات بیشتر این موارد را می‌توانید در گروه [ASP.NET Core Identity](http://www.dotnettips.info/search/label/asp.net%20core%20identity) پیگیری نمائید.
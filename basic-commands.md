# دستورات پایه Git

در این بخش با دستورات اصلی Git آشنا می‌شوید که هر روز در کار با پروژه‌ها از آن‌ها استفاده خواهید کرد.

## ۱. تنظیم اولیه Git (git config)

قبل از اولین استفاده، باید نام و ایمیل خود را به Git معرفی کنید. این اطلاعات روی هر Commit شما ثبت می‌شود.

```bash
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
```

برای بررسی تنظیمات:

```bash
git config --list
```

> نکته: ایمیل را همان ایمیلی بگذارید که با آن در GitHub ثبت‌نام کرده‌اید.

## ۲. ساخت مخزن جدید (git init)

اگر یک پوشه پروژه دارید و می‌خواهید Git آن را مدیریت کند:

```bash
mkdir my-project
cd my-project
git init
```

بعد از اجرای این دستور، یک پوشه مخفی به نام `.git` ساخته می‌شود که تاریخچه پروژه در آن نگهداری می‌شود.

## ۳. دریافت یک پروژه موجود (git clone)

برای دانلود یک مخزن از GitHub روی سیستم خودتان:

```bash
git clone https://github.com/USERNAME/REPO-NAME.git
```

این دستور یک پوشه با نام مخزن می‌سازد و کل پروژه به همراه تاریخچه‌اش را در آن قرار می‌دهد.

| دستور | کاربرد |
|-------|--------|
| `git init` | شروع یک پروژه جدید از صفر |
| `git clone` | دریافت پروژه‌ای که قبلاً وجود دارد |


## ۴. مشاهده وضعیت پروژه (git status)

نشان می‌دهد کدام فایل‌ها تغییر کرده‌اند و کدام‌ها آماده Commit هستند.

```bash
git status
```

## ۵. آماده‌سازی تغییرات (git add)

قبل از Commit باید مشخص کنید کدام تغییرات وارد آن شوند.

```bash
git add file.txt     # اضافه کردن یک فایل
git add .            # اضافه کردن همه تغییرات
```

## ۶. ثبت تغییرات (git commit)

Commit مثل یک «عکس از وضعیت پروژه» در یک لحظه است. پیام Commit باید توضیح دهد چه کاری انجام داده‌اید.

```bash
git commit -m "Add login page"
```

مثال پیام خوب و بد:

| پیام بد | پیام خوب |
|---------|----------|
| `update` | `Fix typo in README title` |
| `test` | `Add user registration form` |

## ۷. ارسال تغییرات به GitHub (git push)

: «در کار تیمی مستقیم روی main پوش نمی‌کنیم و از شاخه مستقل استفاده می‌کنیم.» 

```bash
git push -u origin feature/my-branch
```

اولین بار برای یک Branch جدید:

```bash
git push -u origin feature/my-branch
```

## ۸. دریافت تغییرات دیگران (git pull)

قبل از شروع کار، تغییرات جدید تیم را بگیرید:
دستور git pull origin main تغییرات شاخه main را در شاخه‌ای که
اکنون روی آن هستید ادغام می‌کند؛ خودش شما را وارد main نمی‌کند. 

```bash
git pull origin main
```

## ۹. مشاهده تاریخچه (git log)

```bash
git log
git log --oneline    # نمایش خلاصه
```

خروجی نمونه:

```
a1b2c3d Add status, add, commit sections
e4f5a6b Add git config, init and clone sections
```

## جمع‌بندی: چرخه کار روزانه

```bash
git pull                    # دریافت آخرین تغییرات
# ... انجام تغییرات ...
git add .                   # آماده‌سازی
git commit -m "پیام معنادار"  # ثبت
git push                    # ارسال
```
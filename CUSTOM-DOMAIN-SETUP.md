# راهنمای تنظیم دامنه سفارشی hoomanhedayati.ir

## مشکل فعلی
GitHub Pages نمی‌تواند DNS records دامنه شما را پیدا کند. باید DNS records را در registrar دامنه خود تنظیم کنید.

---

## مرحله 1: اضافه کردن CNAME فایل

✅ فایل `CNAME` در repository اضافه شده است.

---

## مرحله 2: تنظیم DNS Records

به پنل مدیریت دامنه خود بروید (جایی که دامنه `hoomanhedayati.ir` را خریداری کرده‌اید).

### گزینه 1: استفاده از Apex Domain (hoomanhedayati.ir)

اگر می‌خواهید از `hoomanhedayati.ir` (بدون www) استفاده کنید:

**A Records** اضافه کنید:
```
Type: A
Name: @
Value: 185.199.108.153
TTL: 3600 (یا Automatic)

Type: A
Name: @
Value: 185.199.109.153
TTL: 3600

Type: A
Name: @
Value: 185.199.110.153
TTL: 3600

Type: A
Name: @
Value: 185.199.111.153
TTL: 3600
```

**نکته**: این IP addresses مربوط به GitHub Pages هستند و ممکن است تغییر کنند. برای IP های به‌روز، به این لینک مراجعه کنید:
https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site#configuring-an-apex-domain

### گزینه 2: استفاده از www (www.hoomanhedayati.ir)

اگر می‌خواهید از `www.hoomanhedayati.ir` استفاده کنید:

**CNAME Record** اضافه کنید:
```
Type: CNAME
Name: www
Value: hoomanehedayati.github.io
TTL: 3600 (یا Automatic)
```

### گزینه 3: هر دو (پیشنهادی)

برای استفاده از هر دو `hoomanhedayati.ir` و `www.hoomanhedayati.ir`:

1. **A Records** برای apex domain (همان بالا)
2. **CNAME Record** برای www:
```
Type: CNAME
Name: www
Value: hoomanehedayati.github.io
TTL: 3600
```

---

## مرحله 3: تنظیم در GitHub

1. به repository بروید:
   https://github.com/hoomanehedayati/html-css-personal-website/settings/pages

2. در بخش **Custom domain**:
   - دامنه را وارد کنید: `hoomanhedayati.ir`
   - یا `www.hoomanhedayati.ir` (اگر از www استفاده می‌کنید)
   - ✅ گزینه **Enforce HTTPS** را فعال کنید (بعد از فعال شدن DNS)

3. **Save** را بزنید

---

## مرحله 4: صبر برای Propagation

- DNS changes معمولاً 24-48 ساعت طول می‌کشد
- اما معمولاً 1-2 ساعت کافی است
- می‌توانید با این ابزارها چک کنید:
  - https://dnschecker.org
  - https://www.whatsmydns.net

---

## مرحله 5: بررسی

بعد از propagation:

1. به `https://hoomanhedayati.ir` بروید
2. باید سایت شما نمایش داده شود
3. در GitHub Pages settings، باید ✅ سبز ببینید

---

## مشکلات رایج

### مشکل: "InvalidDNSError"

**راه حل:**
1. مطمئن شوید DNS records درست اضافه شده‌اند
2. 1-2 ساعت صبر کنید
3. دوباره در GitHub Pages settings چک کنید

### مشکل: "DNS record could not be retrieved"

**راه حل:**
1. بررسی کنید که دامنه درست ثبت شده است
2. مطمئن شوید A Records یا CNAME درست تنظیم شده‌اند
3. TTL را روی 3600 یا Automatic بگذارید

### مشکل: سایت با www کار می‌کند اما بدون www کار نمی‌کند

**راه حل:**
- A Records را برای apex domain اضافه کنید (4 IP addresses بالا)

---

## نکات مهم

1. ✅ فایل `CNAME` باید در root directory باشد (انجام شده)
2. ✅ DNS records باید در registrar دامنه تنظیم شوند
3. ✅ بعد از تنظیم DNS، 1-2 ساعت صبر کنید
4. ✅ بعد از فعال شدن، **Enforce HTTPS** را فعال کنید

---

## Registrar های معروف ایرانی

اگر دامنه را از یکی از این registrar ها خریده‌اید:

- **Nic.ir**: پنل مدیریت دامنه .ir
- **ایران هاست**
- **میهن وب‌هاست**
- **وب‌هاستینگ**

در پنل هر کدام، بخش **DNS Management** یا **مدیریت DNS** را پیدا کنید.

---

**بعد از تنظیم DNS، فایل CNAME را commit و push کنید!**


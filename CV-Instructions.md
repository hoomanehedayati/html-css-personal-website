# راهنمای تبدیل CV به PDF

## روش 1: استفاده از مرورگر (ساده‌ترین روش)

1. فایل `cv.html` را در مرورگر باز کنید:
   ```bash
   open cv.html
   ```
   یا دوبار کلیک روی فایل

2. در مرورگر:
   - **Chrome/Safari**: Cmd+P (یا File → Print)
   - **Firefox**: Cmd+P (یا File → Print)

3. تنظیمات Print:
   - **Destination**: Save as PDF
   - **Layout**: Portrait
   - **Paper Size**: A4
   - **Margins**: Default یا Minimum
   - **Options**: Background graphics را فعال کنید

4. Save را بزنید و PDF را ذخیره کنید

---

## روش 2: استفاده از VS Code (اگر نصب دارید)

1. Extension "Markdown PDF" را نصب کنید
2. روی `cv.html` راست‌کلیک
3. "Print to PDF" را انتخاب کنید

---

## روش 3: استفاده از Online Converter

1. به یکی از این سایت‌ها بروید:
   - html2pdf.com
   - htmlpdfapi.com
   - ilovepdf.com/html-to-pdf

2. فایل `cv.html` را آپلود کنید
3. PDF را دانلود کنید

---

## روش 4: استفاده از Command Line (Mac)

اگر wkhtmltopdf نصب دارید:
```bash
wkhtmltopdf cv.html cv.pdf
```

یا با Chrome:
```bash
/Applications/Google\ Chrome.app/Contents/MacOS/Google\ Chrome --headless --disable-gpu --print-to-pdf=cv.pdf cv.html
```

---

## نکات مهم

1. **قبل از Print:**
   - فونت‌ها را بررسی کنید
   - Layout را چک کنید
   - مطمئن شوید تمام محتوا نمایش داده می‌شود

2. **کیفیت PDF:**
   - از مرورگر Chrome یا Safari استفاده کنید (بهترین کیفیت)
   - Background graphics را فعال کنید
   - Paper size را A4 تنظیم کنید

3. **بررسی نهایی:**
   - PDF را باز کنید و بررسی کنید
   - مطمئن شوید تمام متن‌ها خوانا هستند
   - Layout درست است

---

## سفارشی‌سازی CV

اگر می‌خواهید CV را تغییر دهید:
- فایل `cv.html` را در ویرایشگر متن باز کنید
- اطلاعات را ویرایش کنید
- استایل‌ها در بخش `<style>` هستند

---

## فایل نهایی

بعد از تبدیل، فایل PDF را با نام مناسب ذخیره کنید:
- `Hooman-Hedayati-CV.pdf`
- `Resume-Hooman-Hedayati.pdf`


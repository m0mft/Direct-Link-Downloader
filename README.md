# Direct Link Downloader

A powerful set of GitHub Actions workflows to download files from any direct link at maximum speed using `aria2` (with multiple connections) and automatically upload them to your GitHub Releases or cloud storage (like ArvanCloud).

---

## 🇬🇧 English

### Features
- **High-Speed Downloads**: Uses `aria2c` with 16 parallel connections to maximize download speeds from any direct link.
- **Custom Filenames**: Option to rename files on the fly during download.
- **Flexible Compression**: Automatically compress downloaded files into ZIP, TAR, TAR.GZ, or RAR formats.
- **RAR Split Support**: Split huge files into smaller RAR parts (e.g., 1.9GB chunks) to bypass GitHub's 2GB file size limit per release asset.
- **Cloud Storage Upload**: Built-in workflow (`Arvan.yml`) to upload directly to ArvanCloud Object Storage (S3-compatible).

### How to Use
1. Fork or import this repository.
2. Go to the **Actions** tab.
3. Select a workflow from the left sidebar (e.g., *Ultimate File Downloader (Release)*).
4. Click **Run workflow**.
5. Provide the required inputs:
   - `url`: The direct download link of the file.
   - `filename`: (Optional) A custom name for the downloaded file.
   - `compression`: Choose if you want to compress the file.
   - `rar_split_size`: Volume size for RAR splits (e.g., `1900M`).
6. Click **Run workflow**. Wait for the process to finish, and the files will appear in the **Releases** tab!

### Requirements
- No extra setup for the GitHub Releases workflow!
- For the ArvanCloud workflow, you must set `ARVAN_ACCESS_KEY` and `ARVAN_SECRET_KEY` in the repository **Secrets**.

---

## 🇮🇷 فارسی (Persian)

### ویژگی‌ها
- **دانلود با بالاترین سرعت**: استفاده از موتور `aria2c` با ۱۶ کانکشن موازی برای دانلود فایل‌ها از لینک مستقیم با نهایت سرعت.
- **تغییر نام دلخواه**: امکان انتخاب نام سفارشی برای فایل در حال دانلود.
- **فشرده‌سازی منعطف**: پشتیبانی از فشرده‌سازی فایل دانلود شده به فرمت‌های ZIP, TAR, TAR.GZ و RAR.
- **تکه‌تکه کردن (Split) فایل‌ها**: قابلیت تکه‌تکه کردن فایل‌های حجیم به پارت‌های کوچکتر (مثلاً ۱.۹ گیگابایتی) برای دور زدن محدودیت ۲ گیگابایتی گیت‌هاب در بخش Releases.
- **آپلود در فضای ابری**: شامل ورک‌فلوی اختصاصی (`Arvan.yml`) برای آپلود فایل به صورت مستقیم در فضای ابری آروان‌کلود (سازگار با پروتکل S3).

### نحوه استفاده
۱. این مخزن را Fork کنید یا به اکانت خود منتقل نمایید.
۲. به تب **Actions** بروید.
۳. یکی از ورک‌فلوها را از منوی سمت چپ انتخاب کنید (مثلاً *Ultimate File Downloader (Release)*).
۴. روی دکمه **Run workflow** کلیک کنید.
۵. مقادیر خواسته‌شده را وارد کنید:
   - `url`: لینک دانلود مستقیم فایل شما.
   - `filename`: (اختیاری) نام دلخواه برای ذخیره فایل.
   - `compression`: انتخاب نوع فشرده‌سازی.
   - `rar_split_size`: حجم هر پارت در صورت استفاده از فرمت RAR (مثلاً `1900M`).
۶. ورک‌فلو را اجرا کنید. در پایان عملیات، فایل‌های شما در بخش **Releases** در دسترس خواهند بود.

### پیش‌نیازها
- ورک‌فلوی دانلود در گیت‌هاب نیاز به هیچ تنظیماتی ندارد!
- برای استفاده از ورک‌فلوی آروان‌کلود، باید `ARVAN_ACCESS_KEY` و `ARVAN_SECRET_KEY` را در بخش **Secrets** مخزن خود ذخیره کنید.

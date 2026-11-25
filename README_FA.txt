NOVA Planner - پروژه اندروید

این پروژه یک پوسته اندرویدی برای فایل HTML فعلی NOVA Planner است.
برای ساخت APK باید Android Studio، Android SDK و اتصال لازم برای دریافت Gradle dependencies در دسترس باشد.
در حال حاضر APK کامپایل‌شده نیست؛ این فایل‌ها سورس کامل پروژه هستند.

روش باز کردن:
1) فایل ZIP را از حالت فشرده خارج کنید.
2) Android Studio را باز کنید.
3) از صفحه شروع، Open را بزنید و پوشه NOVA_Planner_Android را انتخاب کنید.
4) صبر کنید Gradle Sync کامل شود.
5) از منوی Build > Build Bundle(s) / APK(s) > Build APK(s) خروجی بگیرید.

مشخصات:
- زبان: Kotlin
- رابط: WebView
- شناسه برنامه: com.nova.planner
- حداقل نسخه: Android 6.0 (API 23)
- فایل HTML داخل app/src/main/assets/index.html قرار دارد.
- ذخیره‌سازی داده‌ها با DOM Storage / localStorage انجام می‌شود.
- برای اعلان‌ها یک پل ساده بومی اندروید اضافه شده است.

نکته:
اعلان‌ها در زمان اجرای برنامه و با اجازه کاربر قابل استفاده‌اند. برای یادآوری دقیق در پس‌زمینه، حتی وقتی برنامه بسته است، در مرحله بعد باید زمان‌بندی بومی اندروید (WorkManager یا AlarmManager) اضافه و آزمایش شود.

ساخت APK با GitHub Actions (بدون نصب SDK روی لپ‌تاپ):
1) یک Repository جدید در GitHub بسازید.
2) تمام محتویات همین پوشه را در ریشه Repository آپلود/Push کنید؛ پوشه .github هم باید همراه بقیه فایل‌ها باشد.
3) به تب Actions بروید. در صورت درخواست، گزینه فعال‌سازی workflowها را تأیید کنید.
4) workflow با هر Push به شاخه main یا master اجرا می‌شود. برای اجرای دستی: Actions > Build NOVA Planner APK > Run workflow.
5) پس از سبز شدن اجرا، وارد همان اجرای workflow شوید و از بخش Artifacts فایل NOVA-Planner-debug-APK را دانلود کنید.
6) ZIP دانلودشده را باز کنید؛ فایل app-debug.apk داخل آن است و می‌توانید آن را روی گوشی نصب و آزمایش کنید.

این workflow روی سرورهای GitHub، JDK، Android SDK و Gradle را آماده می‌کند؛ بنابراین لازم نیست SDK را روی رایانه خودتان نصب کنید. برای انتشار عمومی در Google Play بعداً باید نسخه release و امضای امن (keystore) جداگانه تنظیم شود.

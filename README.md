# تطبيق إدارة الشبكة - Modem Management App

تطبيق Android متقدم وكامل لإدارة المودمات والسويتشات والأعطال والمستخدمين.

## المتطلبات

- **Android Studio** (أحدث إصدار)
- **Java Development Kit (JDK) 11** أو أحدث
- **Android SDK** (API 34)
- **Gradle 8.5** أو أحدث

## التثبيت والبناء

### الخطوة 1: فتح المشروع في Android Studio

1. افتح Android Studio
2. اختر `File → Open`
3. اختر مجلد `ModemManagement-Android`
4. انتظر حتى ينتهي Gradle من التحميل والمزامنة

### الخطوة 2: بناء ملف APK

#### الطريقة الأولى: من واجهة Android Studio
1. اذهب إلى `Build → Build Bundle(s) / APK(s) → Build APK(s)`
2. انتظر حتى ينتهي البناء
3. سيظهر إشعار بموقع ملف APK

#### الطريقة الثانية: من سطر الأوامر
```bash
cd ModemManagement-Android
./gradlew assembleRelease
```

### الخطوة 3: تثبيت على الهاتف

#### عبر Android Studio
1. اتصل هاتفك بجهازك عبر USB
2. فعّل وضع المطور على الهاتف
3. اذهب إلى `Run → Run 'app'`
4. اختر جهازك من القائمة

#### عبر سطر الأوامر
```bash
adb install app/build/outputs/apk/release/app-release.apk
```

#### عبر نقل الملف يدوياً
1. انسخ ملف APK إلى جهازك
2. افتح الملف من مدير الملفات
3. اتبع التعليمات على الشاشة

## هيكل المشروع

```
ModemManagement-Android/
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── kotlin/com/modem/management/
│   │   │   │   └── MainActivity.kt
│   │   │   ├── res/
│   │   │   │   ├── layout/
│   │   │   │   ├── values/
│   │   │   │   └── drawable/
│   │   │   └── AndroidManifest.xml
│   │   ├── test/
│   │   └── androidTest/
│   ├── build.gradle.kts
│   └── proguard-rules.pro
├── build.gradle.kts
├── settings.gradle.kts
├── gradle.properties
└── README.md
```

## الميزات الرئيسية

- ✅ إدارة المودمات (عرض، إضافة، تعديل، حذف)
- ✅ إدارة السويتشات
- ✅ إدارة الأعطال وإرسال الرسائل
- ✅ إدارة المستخدمين
- ✅ واجهة عربية احترافية
- ✅ اتصال آمن بـ API

## المتطلبات الدنيا للجهاز

- **Android 9.0 (API 28)** أو أحدث
- **100 MB** من مساحة التخزين الحرة�ل إنترنت

## استكشاف الأخطاء

### المشكلة: فشل البناء

**الحل:**
1. تأكد من تثبيت JDK 11 أو أحدث
2. تأكد من تثبيت Android SDK API 34
3. قم بتشغيل `File → Sync Now` في Android Studio
4. احذف مجلد `.gradle` و `build` وحاول مرة أخرى

### المشكلة: لا يمكن تثبيت التطبيق

**الحل:**
1. تأكد من تفعيل وضع المطور على الهاتف
2. فعّل تصحيح USB
3. حاول إعادة تشغيل الهاتف
4. تأكد من توصيل USB بشكل صحيح

### المشكلة: التطبيق يتعطل عند الفتح

**الحل:**
1. تحقق من سجلات Logcat في Android Studio
2. تأكد من توفر اتصال إنترنت
3. حاول حذف بيانات التطبيق وإعادة تثبيته

## الدعم والمساعدة

للمساعدة أو الإبلاغ عن مشاكل:
- البريد الإلكتروني: support@modem-management.com
- الموقع: https://modemdash-5pqebd33.manus.space/

## الترخيص

جميع الحقوق محفوظة © 2024

---

تم تطوير هذا التطبيق بواسطة فريق التطوير

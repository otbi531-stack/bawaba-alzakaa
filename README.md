# بوابة الذكاء — ألعاب تعليمية للأطفال

موقع ثابت (HTML واحد + صور) يعمل على GitHub Pages، والحسابات عبر Firebase.

## الملفات
- `index.html` — الموقع كاملًا (الألعاب، الشراء، الحسابات، لوحة ولي الأمر)
- `hero.jpg` و `img/` — الصور
- `firestore.rules` — قواعد حماية قاعدة البيانات

## تفعيل الحسابات الحقيقية (Firebase)
1. ادخل https://console.firebase.google.com وأنشئ مشروعًا جديدًا.
2. **Authentication** ← Get started ← فعّل **Email/Password**.
3. **Firestore Database** ← Create database ← اختر أقرب منطقة.
4. من تبويب **Rules** الصق محتوى `firestore.rules` ثم Publish.
5. **Project settings** ← Your apps ← أضف تطبيق ويب `</>` وانسخ كائن `firebaseConfig`.
6. افتح `index.html` وابحث عن `const FIREBASE_CONFIG = null;` وضع مكان `null` الإعدادات التي نسختها.
7. في Authentication ← Settings ← **Authorized domains** أضف نطاق موقعك (مثل `username.github.io`).

بدون الخطوة 6 يعمل الموقع بالوضع التجريبي: الحسابات محفوظة في المتصفح فقط.

## النشر على GitHub Pages
ارفع كل الملفات إلى مستودع جديد ← Settings ← Pages ← Branch: `main` ← Save.

## الدفع وموافقة الإدارة
- الطفل يحوّل المبلغ عبر STC Bank مع رمز مرجعي، ثم يرسل طلبًا من الموقع.
- المدير (otbi531@gmail.com بعد تأكيد البريد) يفتح «ملفي ← لوحة الإدارة» أو الرابط `#admin`، ويوافق على الطلب بعد التأكد من التحويل.
- بعد الموافقة تُضاف النجوم للطفل تلقائيًا.
- قواعد الحماية في `firestore.rules` يجب نشرها في Firebase Console ← Firestore ← Rules.

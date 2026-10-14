# Clary Client — نسخة البداية

مشروع Fabric Client-side لماينكرافت Java 1.21.11، بواجهة صغيرة داكنة بنفسجية.

## الموجود حالياً
- فتح الواجهة بزر Right Shift.
- أزرار تبديل Auto Detect وESP وHide Names وFreecam وAim Assist وTarget Lock.
- حقل اسم محلي داخل الواجهة.
- إعدادات الأزرار تحفظ داخل الذاكرة خلال جلسة اللعب فقط.

## مهم جداً
هذه **نسخة واجهة أولية** وليست كلاينتاً كاملاً بعد. أزرار الميزات المتقدمة حالياً تغيّر حالتها في الواجهة فقط؛ لم تُنفّذ بعد وظائف ESP الفعلية أو Freecam أو Aim Assist أو اعتراض أسماء اللاعبين أو حفظ الاسم على القرص. الاسم المدخل لا يغيّر اسم حساب Minecraft ولا اسمك الذي يراه السيرفر.

## البناء على الكمبيوتر
1. ثبّت JDK 21.
2. ثبّت Git (اختياري) وGradle أو افتح المشروع في IntelliJ IDEA.
3. من مجلد المشروع نفّذ:
   - Windows: `gradle build`
   - Linux/macOS: `gradle build`
4. بعد نجاح البناء ستجد الملف داخل `build/libs/` باسم قريب من `ClaryClient-0.1.0.jar`.
5. انسخ ملف JAR إلى مجلد `mods` الخاص بملف تعريف Fabric 1.21.11. ثبّت Fabric API المطابق للإصدار نفسه.

## البناء من الهاتف عبر GitHub Actions
يوجد ملف Workflow داخل `.github/workflows/build.yml`. ارفع المشروع إلى مستودع GitHub، ثم افتح تبويب Actions وشغّل Build Clary Client. سيظهر ملف JAR كـ Artifact بعد نجاح البناء.

## PojavLauncher
يجب أن يكون ملف تعريف Pojav على Minecraft Java 1.21.11 مع Fabric وJava 21. الأداء والتوافق يختلفان حسب الجهاز. لا تضع ملف JAR في مجلد resourcepacks؛ مكانه مجلد `mods`.

## روابط رسمية
- Fabric docs: https://docs.fabricmc.net/
- Fabric installer: https://fabricmc.net/use/installer/

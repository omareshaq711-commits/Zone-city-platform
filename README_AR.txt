ZONE CITY CFW — حزمة جاهزة للنشر على Cloudflare Workers Static Assets

مهم:
- هذه الحزمة تحافظ على الموقع الحالي وصفحة الترحيب والمنتجات والصور والفيديو.
- اسم Worker مضبوط على zone-city-platform-test حتى يكون النشر نسخة اختبار منفصلة ولا يستبدل الموقع الحالي.
- هذه الحزمة تنشر الموقع الثابت الحالي فقط. لا تتضمن بعد نظام حسابات حقيقي أو قاعدة بيانات أو لوحة إدارة أو نظام تقديمات؛ هذه تحتاج إعداد Backend وقاعدة بيانات وربط خدمات قبل تفعيلها.

طريقة النشر من Windows:
1) فك ضغط الملف إلى مجلد عادي.
2) ثبّت Node.js من https://nodejs.org/ (إصدار LTS).
3) افتح CMD داخل مجلد Zone_City_Cloudflare_Ready نفسه، حيث يوجد package.json.
4) نفّذ:
   npm install
5) ثم:
   npx wrangler login
   سيفتح المتصفح؛ سجّل الدخول إلى Cloudflare واسمح بالربط.
6) انشر نسخة الاختبار:
   npm run deploy

التطوير المحلي قبل النشر:
   npm run dev

بعد النشر سيظهر لك رابط Worker تجريبي باسم قريب من:
   https://zone-city-platform-test.<your-subdomain>.workers.dev

لا ترفع هذه الحزمة من زر Upload assets في لوحة Cloudflare؛ استخدم الأوامر أعلاه من CMD.
لا تشارك كلمة مرور Cloudflare أو API Token مع أي شخص.

مشروع Osama Alhawary - Cloudflare Workers

مهم: هذا مشروع جاهز كبداية للنشر، لكنه يحتاج إنشاء D1 وR2 على Cloudflare وربط database_id ثم ضبط ADMIN_PASSWORD قبل أن تعمل وظائف الرفع.

المتطلبات:
1) Node.js وWrangler على كمبيوتر أو بيئة طرفية.
2) إنشاء D1 database باسم osama-alhawary-db.
3) إنشاء R2 bucket باسم osama-alhawary-files.
4) وضع D1 database_id في wrangler.toml.
5) ضبط السر: npx wrangler secret put ADMIN_PASSWORD
6) تنفيذ: npx wrangler d1 migrations apply osama-alhawary-db --remote
7) النشر: npx wrangler deploy

ملاحظة أمنية: نظام الجلسة في هذا الإصدار تجريبي؛ لا تستخدمه لرفع ملفات خاصة أو حساسة قبل تقوية المصادقة. الملفات المرفوعة متاحة للزوار.
8) ضبط السر الثاني: npx wrangler secret put SESSION_SECRET (استخدم قيمة طويلة وعشوائية).

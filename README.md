# ✦ AI Hub — دليل النشر

## هيكل المشروع
```
ai-hub/
├── index.html                  ← الواجهة الرئيسية
├── netlify.toml                ← إعدادات Netlify
└── netlify/
    └── functions/
        └── chat.js             ← البروكسي الآمن (يخفي مفتاح API)
```

---

## خطوات النشر على Netlify

### 1. ارفع المجلد
- اذهب إلى https://netlify.com
- سجّل دخول أو أنشئ حساباً مجاناً
- اسحب مجلد `ai-hub` كاملاً وأفلته في صفحة Netlify

### 2. أضف مفتاح API
بعد رفع الملفات:
- اذهب إلى: **Site Settings → Environment Variables**
- اضغط **Add variable**
- المفتاح: `ANTHROPIC_API_KEY`
- القيمة: مفتاحك من https://console.anthropic.com

### 3. أعد النشر
- اذهب إلى **Deploys**
- اضغط **Trigger deploy → Deploy site**

### 4. ✅ جاهز!
ستحصل على رابط مثل: `https://your-site.netlify.app`

---

## ربط دومين خاص (اختياري)
- اذهب إلى **Domain settings**
- اضغط **Add custom domain**
- اتبع التعليمات لإعداد DNS

---

## ملاحظات مهمة
- لا تشارك ملف `chat.js` مع أي أحد — لكنه آمن لأن المفتاح محفوظ في متغيرات البيئة وليس في الكود
- راقب استهلاكك على https://console.anthropic.com
- يمكن تحديد حد أقصى للإنفاق من إعدادات Anthropic

# ERP System – Django + React

نظام إدارة موارد المؤسسات (ERP) كامل مبني باستخدام:

- 🔧 **Backend**: Django + Django REST Framework
- 💻 **Frontend**: React + TailwindCSS + ShadCN UI
- ☁️ **Deployment**: Render.com باستخدام `render.yaml`

---

## 📁 بنية المشروع

```
erp-complete/
│
├── backend/               ← مشروع Django API
│   ├── manage.py
│   ├── requirements.txt
│   └── backend/           ← مجلد Django الرئيسي
│
├── frontend/              ← مشروع React + Vite
│   ├── package.json
│   ├── vite.config.js
│   └── src/
│
└── render.yaml            ← ملف النشر التلقائي (Blueprint)
```

---

## 🚀 خطوات النشر على Render

### 1. تحميل المشروع على GitHub
- أنشئ مستودع جديد مثل: `erp-complete`
- ارفع إليه ملفات المشروع (من المجلد المضغوط `erp-complete-structured.zip`)

### 2. نشر تلقائي عبر Render

- اذهب إلى: [https://dashboard.render.com/blueprint](https://dashboard.render.com/blueprint)
- اضغط: **"New Blueprint Instance"**
- اربط مستودع GitHub الذي رفعته
- سيتم إنشاء:
  - خدمة `erp-api`: خدمة Django
  - خدمة `erp-frontend`: React frontend
- انتظر حتى تكتمل عمليتا build

---

## 🔐 المتغيرات البيئية (Environment Variables)

### backend (Django):
| Key              | Value                        |
|------------------|------------------------------|
| `DJANGO_SECRET_KEY` | أي مفتاح سري قوي           |
| `DEBUG`          | `false`                      |
| `ALLOWED_HOSTS`  | `erp-api.onrender.com`       |

### frontend (React):
| Key                  | Value                                |
|----------------------|--------------------------------------|
| `VITE_API_BASE_URL`  | `https://erp-api.onrender.com/api`  |

---

## 🧪 بيانات تجريبية

يتم توليد بيانات وهمية تلقائيًا بعد التهيئة عبر ملف:

```bash
python generate_fake_data.py
```

وذلك ضمن أمر النشر في `render.yaml`.

---

## 📝 المزايا الحالية

- فواتير مبيعات ومشتريات
- إدارة العملاء والموردين
- إدارة الأصناف والمخزون
- نظام إعدادات كامل
- لوحة تحكم + رسوم بيانية
- نظام صلاحيات وتوثيق JWT
- واجهة حديثة وتفاعلية (React + Tailwind + ShadCN)

---

## 🛠️ تطوير محلي

### backend
```bash
cd backend
python -m venv env
source env/bin/activate
pip install -r requirements.txt
python manage.py runserver
```

### frontend
```bash
cd frontend
npm install
npm run dev
```

---

## 📦 تنبيه

تمت تهيئة كل شيء لتعمل بسلاسة على [Render.com](https://render.com) بنشر تلقائي.

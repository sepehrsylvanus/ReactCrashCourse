# ShopHub - React E-Commerce Application

یک اپلیکیشن فروشگاه آنلاین ساخته شده با React که ویژگی‌های احراز هویت، مدیریت سبد خرید و نمایش محصولات را ارائه می‌دهد.

## 🎯 ویژگی‌های پروژه

### 1. **سیستم احراز هویت**

- ثبت‌نام و ورود کاربران
- ذخیره‌سازی اطلاعات کاربر در localStorage
- مدیریت وضعیت ورود با Context API
- اعتبارسنجی فرم با React Hook Form

### 2. **مدیریت سبد خرید**

- افزودن محصول به سبد خرید
- به‌روزرسانی تعداد محصولات
- حذف محصول از سبد خرید
- محاسبه خودکار مجموع قیمت‌ها
- پاک کردن کامل سبد خرید

### 3. **نمایش محصولات**

- صفحه اصلی با لیست تمام محصولات
- صفحه جزئیات هر محصول
- نمایش قیمت، تصویر و توضیحات محصول
- لینک‌دهی بین صفحات با React Router

### 4. **فرآیند خرید**

- صفحه checkout با خلاصه سفارش
- امکان تغییر تعداد محصولات
- نمایش قیمت نهایی
- ثبت نهایی سفارش

## 🛠️ تکنولوژی‌های استفاده شده

- **React 19.2.7** - کتابخانه اصلی برای ساخت UI
- **Vite 8.1.1** - ابزار build و dev server
- **React Router DOM 7.18.1** - مدیریت مسیریابی
- **React Hook Form 7.81.0** - مدیریت و اعتبارسنجی فرم‌ها
- **Context API** - مدیریت state سراسری (احراز هویت و سبد خرید)
- **localStorage** - ذخیره‌سازی داده‌های کاربر

## 📁 ساختار پروژه

```
src/
├── components/
│   └── ProductCard.jsx          # کارت نمایش محصول
├── context/
│   ├── AuthContext.jsx          # مدیریت احراز هویت
│   └── CartContext.jsx          # مدیریت سبد خرید
├── data/
│   └── product.js               # داده‌های محصولات
├── pages/
│   ├── Auth.jsx                 # صفحه ورود/ثبت‌نام
│   ├── Checkout.jsx             # صفحه پرداخت
│   ├── Home.jsx                 # صفحه اصلی
│   └── ProductDetails.jsx       # صفحه جزئیات محصول
├── App.jsx                      # کامپوننت اصلی با routing
├── App.css                      # استایل‌های全局
└── main.jsx                     # نقطه ورود اپلیکیشن
```

## 🚀 نحوه اجرا

### پیش‌نیازها

- Node.js (نسخه 16 یا بالاتر)
- npm یا yarn

### مراحل نصب و اجرا

1. **کلون کردن repository**

```bash
git clone https://github.com/sepehrsylvanus/ReactCrashCourse.git
cd ReactCrashCourse
```

2. **نصب وابستگی‌ها**

```bash
npm install
```

3. **اجرای سرور توسعه**

```bash
npm run dev
```

4. **باز کردن مرورگر**

```
http://localhost:5173
```

## 📝 دستورات موجود

```bash
npm run dev      # اجرای سرور توسعه با hot reload
npm run build    # ساخت نسخه production
npm run preview  # پیش‌نمایش نسخه build شده
npm run lint     # بررسی کد با ESLint
```

## 🔄 مسیرهای اپلیکیشن

| مسیر            | صفحه           | توضیحات                  |
| --------------- | -------------- | ------------------------ |
| `/`             | Home           | لیست تمام محصولات        |
| `/auth`         | Auth           | ورود یا ثبت‌نام          |
| `/checkout`     | Checkout       | مشاهده سبد خرید و پرداخت |
| `/products/:id` | ProductDetails | جزئیات محصول             |

## 💡 نحوه کار پروژه

### مدیریت State با Context API

پروژه از دو Context اصلی استفاده می‌کند:

**1. AuthContext** - مدیریت احراز هویت:

- `user`: اطلاعات کاربر فعلی
- `signup()`: ثبت‌نام کاربر جدید
- `login()`: ورود کاربر
- `logout()`: خروج از حساب

**2. CartContext** - مدیریت سبد خرید:

- `cartItems`: لیست محصولات در سبد
- `addToCart()`: افزودن محصول
- `updateQuantity()`: تغییر تعداد
- `removeFromCart()`: حذف محصول
- `getCartTotal()`: محاسبه مجموع قیمت

### ذخیره‌سازی داده‌ها

- **localStorage**: اطلاعات کاربران و session فعلی
- **Memory State**: سبد خرید (در حافظه موقت)

### مدیریت فرم‌ها

از **React Hook Form** برای:

- مدیریت state فرم
- اعتبارسنجی فیلدها
- نمایش خطاها
- ارسال داده‌ها

## 🎨 ویژگی‌های UI

- طراحی responsive و mobile-friendly
- کارت‌های محصول با تصویر، نام و قیمت
- دکمه‌های تعاملی برای افزودن به سبد خرید
- فرم‌های ورود/ثبت‌نام با اعتبارسنجی
- صفحه checkout با خلاصه سفارش

## 📊 داده‌های نمونه

پروژه شامل 8 محصول نمونه است:

1. Wireless Headphones - $99.99
2. Smart Watch - $249.99
3. Laptop Stand - $49.99
4. Mechanical Keyboard - $129.99
5. USB-C Hub - $39.99
6. Wireless Mouse - $29.99
7. Monitor Stand - $79.99
8. Webcam HD - $89.99

## 🔧 توسعه و گسترش

### افزودن محصول جدید

فایل `src/data/product.js` را ویرایش کنید و آبجکت جدیدی به آرایه `products` اضافه کنید.

### اتصال به Backend

برای استفاده از API واقعی:

1. Context‌ها را برای fetch از API تغییر دهید
2. localStorage را با API calls جایگزین کنید
3. سیستم احراز هویت را با JWT یا session پیاده‌سازی کنید

### اضافه کردن پرداخت واقعی

صفحه Checkout را با یک درگاه پرداخت مانند Stripe یا PayPal یکپارچه کنید.

## 📚 یادگیری از این پروژه

این پروژه مفاهیم زیر را پوشش می‌دهد:

- ✅ React Hooks (useState, useEffect, useContext)
- ✅ Context API برای state management
- ✅ React Router برای navigation
- ✅ Form handling و validation
- ✅ Component composition
- ✅ Props drilling و راه‌حل‌های آن
- ✅ LocalStorage برای persistence
- ✅ Vite به عنوان build tool

## 🤝 مشارکت

برای گزارش bug یا پیشنهاد بهبود:

1. Issue جدید ایجاد کنید
2. Pull Request ارسال کنید

## 📄 لایسنس

این پروژه برای اهداف آموزشی ایجاد شده است.

---

**ساخته شده با ❤️ برای یادگیری React**

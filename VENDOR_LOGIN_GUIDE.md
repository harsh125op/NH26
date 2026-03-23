# 🛍️ Vendor Login Guide / वेंडर लॉगिन गाइड

## ✅ Vendor Ke Liye Login Process

### Option 1: Register Karke (Naye Vendor)

1. **Register Page Pe Jao**: http://localhost:5173/register

2. **Form Fill Karo**:
   - Name: Apna naam
   - Email: Apna email
   - Password: Strong password
   - **Role: "Vendor" select karo** ⭐ (Ye important hai!)

3. **Sign Up Button Click Karo**

4. **Automatic Redirect**: Registration ke baad aap automatically **Vendor Dashboard** pe redirect ho jaoge!

### Option 2: OTP Se Login (Existing User)

1. **Login Page Pe Jao**: http://localhost:5173/login

2. **Email Enter Karo** aur "Send OTP" click karo

3. **Email Check Karo**: Aapko 6-digit OTP milega

4. **OTP Enter Karo** aur "Verify & Login" click karo

5. **Automatic Redirect**: 
   - Agar aap **vendor** ho → Vendor Dashboard pe jaoge
   - Agar aap **customer** ho → Home page pe jaoge

## 🎯 Vendor Dashboard Features

Vendor Dashboard pe aap ye kar sakte ho:

### 1. AI-Powered Product Listing
- Product name, category, price enter karo
- Image URLs add karo (comma separated)
- **"Generate with Gemini"** button click karo
- AI automatically generate karega:
  - SEO-optimized title
  - Social media caption
  - Complete product description

### 2. Stats & Performance
- Total sales dekh sakte ho
- Reel views track kar sakte ho
- Analytics dashboard

## 🔑 Test Vendor Account

Agar aap test karna chahte ho, to ye credentials use kar sakte ho:

**Email**: jeetverma0721@gmail.com (already registered)
**Login Method**: OTP se login karo

Ya phir apna naya vendor account banao!

## 📍 Important URLs

- **Home**: http://localhost:5173/
- **Login**: http://localhost:5173/login
- **Register**: http://localhost:5173/register
- **Vendor Dashboard**: http://localhost:5173/vendor-dashboard
- **Shop**: http://localhost:5173/shop
- **Reels**: http://localhost:5173/reels

## 🎨 Navbar Features (Vendor Ke Liye)

Jab aap vendor ke roop mein login hoge, to navbar mein dikhega:
- **"Seller Hub"** link (green color mein)
- Aapka naam
- Logout button

## ⚡ Quick Start

```bash
# Backend already running on port 5000
# Frontend already running on port 5173

# Bas browser mein jao:
http://localhost:5173/register

# Vendor select karo aur register karo!
```

## 🔧 Technical Details

### Backend API Endpoints
- `POST /api/auth/register` - New vendor registration
- `POST /api/auth/send-otp` - OTP bhejne ke liye
- `POST /api/auth/verify-otp` - OTP verify karne ke liye
- `POST /api/products` - Product create karne ke liye (vendor only)

### Role-Based Routing
- **Vendor** → `/vendor-dashboard`
- **Customer** → `/` (home page)

## 🎉 Features Available

✅ OTP-based secure login
✅ Role-based automatic redirect
✅ AI content generation (Gemini API)
✅ Product management
✅ Sales analytics
✅ Reel integration

---

**Note**: Email service ab properly configured hai, to OTP emails successfully send ho rahe hain!

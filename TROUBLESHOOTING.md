# 🔧 Troubleshooting Guide

## Common Errors & Solutions

### 1. `ERR_BLOCKED_BY_CLIENT`

**Cause:** Browser extension (Ad Blocker, Privacy Badger, etc.) blocking requests

**Solution:**
```
1. Disable ad blocker for localhost
2. Or use Incognito/Private mode
3. Or whitelist localhost:5173 and localhost:5000
```

**Not a Critical Error** - Application will still work!

---

### 2. `runtime.lastError: A listener indicated an asynchronous response...`

**Cause:** Browser extension communication issue (Chrome/Edge extensions)

**Solution:**
```
This is a harmless warning from browser extensions.
Your application is NOT affected by this error.
You can safely ignore it.
```

**To Remove Warning:**
1. Disable unnecessary browser extensions
2. Or ignore it (doesn't affect functionality)

---

### 3. Email Service Errors

**Error:** `❌ Email service not available`

**Solution:**
- Already fixed! Email service is working
- OTP emails are being sent successfully

---

### 4. MongoDB Connection Issues

**Error:** `❌ MongoDB connection error`

**Solution:**
- Check MONGODB_URI in backend/.env
- Ensure internet connection is active
- Verify MongoDB Atlas credentials

**Current Status:** ✅ Connected successfully!

---

### 5. Port Already in Use

**Error:** `Port 5000 is already in use`

**Solution:**
```bash
# Windows
netstat -ano | findstr :5000
taskkill /PID <PID> /F

# Or change port in backend/.env
PORT=5001
```

---

### 6. Module Not Found Errors

**Error:** `Cannot find module 'xyz'`

**Solution:**
```bash
# Backend
cd backend
npm install

# Frontend
cd frontend
npm install
```

---

## ✅ Current Application Status

### Backend (Port 5000)
- ✅ Server running
- ✅ MongoDB connected
- ✅ Email service working
- ✅ All routes loaded

### Frontend (Port 5173)
- ✅ Vite dev server running
- ✅ React app loaded
- ✅ All routes configured
- ✅ Vendor dashboard accessible

---

## 🧪 Quick Tests

### Test 1: Backend API
```bash
# Open browser and visit:
http://localhost:5000/

# Should show:
"AI Commerce Engine API is running..."
```

### Test 2: Frontend
```bash
# Open browser and visit:
http://localhost:5173/

# Should show home page
```

### Test 3: Vendor Dashboard
```bash
# Login as vendor and visit:
http://localhost:5173/vendor-dashboard

# Should show dashboard with sidebar
```

---

## 🔍 Debug Steps

### Step 1: Check Console
```
1. Press F12 in browser
2. Go to Console tab
3. Look for RED errors (not warnings)
4. Ignore extension warnings
```

### Step 2: Check Network
```
1. Press F12 in browser
2. Go to Network tab
3. Refresh page
4. Look for failed requests (red)
5. Check if API calls are working
```

### Step 3: Check Servers
```
# Backend terminal should show:
🚀 Server is running on port 5000
✅ Connected to MongoDB

# Frontend terminal should show:
VITE v8.0.1  ready in XXXXms
➜  Local:   http://localhost:5173/
```

---

## 🚨 Critical vs Non-Critical Errors

### ❌ Critical (Need to Fix):
- Server not starting
- MongoDB connection failed
- Module not found
- Syntax errors in code
- API returning 500 errors

### ⚠️ Non-Critical (Can Ignore):
- `runtime.lastError` (browser extension)
- `ERR_BLOCKED_BY_CLIENT` (ad blocker)
- HMR update messages (normal)
- Deprecation warnings
- Console warnings from extensions

---

## 📞 Still Having Issues?

### Provide These Details:
1. **Error Message** - Exact error from console
2. **Browser** - Chrome/Firefox/Edge/Safari
3. **OS** - Windows/Mac/Linux
4. **Extensions** - List of installed extensions
5. **Screenshots** - Console and Network tab

### Quick Restart:
```bash
# Stop both servers (Ctrl + C)
# Then restart:

# Terminal 1 - Backend
cd backend
npm run dev

# Terminal 2 - Frontend
cd frontend
npm run dev
```

---

## ✅ Everything Working?

If you can:
- ✅ Open http://localhost:5173
- ✅ Login as vendor
- ✅ See vendor dashboard with sidebar
- ✅ Navigate between pages

**Then your application is working perfectly!** 🎉

Browser extension warnings can be safely ignored.

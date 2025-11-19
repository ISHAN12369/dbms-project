
# 🏨 Hostel Management System  
**Full-Stack Application — Express.js + SQLite + Vanilla HTML/CSS/JS**

A complete hostel management solution with authentication, room allocation, guest handling, fees & payments, complaints, visitor logs, inventory, audit logs, and a responsive frontend.

---

## 🔗 Live Demo  
**Live App:** https://debanik213.github.io/hostdbms/
**Demo Video:** https://drive.google.com/file/d/1ap8cw81U4JXssXhfq_ccCshHCnVNndfK/view?usp=sharing

---

## 🚀 Tech Stack

### **Backend**
- Node.js (Express.js)
- SQLite3 database
- JWT Authentication
- Role-Based Access Control (RBAC)
- Multer for file uploads

### **Frontend**
- Pure HTML, CSS, JavaScript (No frameworks)
- SPA with hash-based routing
- Fetch API for backend communication

---

# ⚙️ Project Setup

## 📌 Prerequisites
- Node.js 16+
- npm 9+

---

# 🛠️ Backend Setup

```bash
cd backend
npm install
cp .env .env.local
npm run seed
npm run dev
```

Server runs at: **http://localhost:3000**

### Seed Creates
- 7 users (admin, warden, staff, 3 students)
- 3 hostel blocks + 12 rooms
- Allocations, guest requests, fees, inventory, complaints

### Test Accounts

| Email | Password | Role |
|-------|----------|------|
| admin@hostel.com | admin123 | superadmin |
| warden@hostel.com | warden123 | warden |
| accountant@hostel.com | acc123 | accountant |
| caretaker@hostel.com | care123 | caretaker |
| john@student.com | pass123 | student |

---

# 🎨 Frontend Setup

## Option 1 — Full Testing (Recommended)

```bash
cd frontend-vanilla
npm install
npm run mock
npm run serve
```

- Mock API: **http://localhost:4000**
- Frontend: **http://localhost:5173**

## Option 2 — Direct Open

Just open `index.html`  
⚠ Some API features & file uploads won’t work due to CORS.

---

# 🧩 Combined Features

### 👨‍🎓 Students
- View allocations  
- Submit guest visit requests  
- Upload ID proof  
- Pay fees  
- Submit complaints  
- Request room transfer  

### 🧑‍🔧 Staff / Warden
- Approve guest requests  
- Assign guest rooms  
- Check-in/check-out  
- Manage rooms, blocks, inventory  
- Handle complaints  
- View calendar  

### 🛡 Admin
- Full user management  
- View audit logs  
- PII deletion system  

---

# 🗄 API Overview

### Auth
- `/api/auth/login`
- `/api/auth/register`
- `/api/auth/me`

### Rooms & Blocks
- CRUD for rooms & blocks

### Guest Requests
- Create → Approve → Assign Room → Check-In → Checkout

### Fees & Payments
- Create fee  
- Mark paid  
- View payment logs  

### Complaints
- Create & manage lifecycle  

### Others
- Inventory  
- Transfers  
- Waitlist  
- Audit Logs  

---

# 🗃 Database Tables (15 Total)

Includes:

- `users`, `students`  
- `hostel_blocks`, `rooms`, `room_allocations`  
- `guest_visit_requests`, `visitor_log`  
- `fees`, `payments`  
- `complaints`, `inventory`  
- `audit_log`, `pii_deletion_log`  

---

# 🔐 Security

- JWT (7‑day expiry)  
- bcrypt password hashing  
- Role-based access  
- File upload validation  
- Audit logs  
- PII deletion workflow  

---

# 🌐 Deployment

### Frontend
Upload **frontend-vanilla/** to Netlify or Vercel  
Update `API_BASE_URL` in `config.js`

### Backend (PM2)
```bash
pm2 start server.js --name hostel-api
pm2 save
pm2 startup
```

---

# 📁 Project Structure

```
project/
├── backend/
│   ├── server.js
│   ├── routes/
│   ├── middleware/
│   ├── config/
│   ├── scripts/
│   └── data/
└── frontend-vanilla/
    ├── index.html
    ├── css/
    ├── js/
    └── mock/
```

---


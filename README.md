🛒 NEXTKART – SSR E-Commerce Product Management Dashboard

NEXTKART is a production-grade, full-stack Server-Side Rendered (SSR) e-commerce product management dashboard built using Next.js, Node.js, Prisma, and AWS.
It provides an admin interface to manage products, inventory, users, expenses, and sales analytics, deployed on real AWS cloud infrastructure.

🚀 Live Deployment
Frontend (SSR)

Platform: AWS Amplify

URL:
👉 https://main.d3bew0nxud1hkz.amplifyapp.com

Backend (API)

Platform: AWS API Gateway + EC2

URL:
👉 https://2ezuzbxr51.execute-api.ap-south-1.amazonaws.com/prod

🎥 Demo Video

Duration: 3–5 minutes

Link: (Add Google Drive / YouTube link here)

🔐 Dummy Admin Credentials
Email: admin@nextkart.com
Password: admin123

✨ Features
📊 Dashboard

Sales summary (weekly / monthly)

Purchase summary

Expense breakdown with charts

Customer growth analytics

Dues & pending orders overview

📦 Inventory Management

Product listing with stock quantity

Price & rating visibility

🛍 Products

Product cards with images

Stock availability

Ratings display

Create product UI

👥 Users

User listing

User ID, name, and email display

⚙️ Settings

Profile settings

Notification toggle

Dark mode toggle

Language preference

💸 Expenses

Filter by category and date

Pie-chart visualization

Category-wise expense analysis

🧠 Tech Stack
Frontend

Next.js (App Router, SSR)

TypeScript

Tailwind CSS

Redux Toolkit

Recharts

Backend

Node.js

Express.js

TypeScript

Prisma ORM

PostgreSQL

Cloud & DevOps

AWS Amplify

AWS EC2 (Amazon Linux 2023)

AWS RDS (PostgreSQL)

AWS S3

AWS API Gateway

PM2

📁 Project Structure
product-management/
├── client/        # Next.js SSR frontend
├── server/        # Node.js backend with Prisma
└── README.md

🛠 Local Setup
1️⃣ Clone Repository
git clone https://github.com/AJmark26/product-management.git
cd product-management

2️⃣ Frontend Setup
cd client
npm install
npm run dev


Local URL: http://localhost:3000

3️⃣ Backend Setup
cd server
npm install

Environment Variables (.env)
DATABASE_URL=postgresql://username:password@localhost:5432/productmanagement
PORT=8000

Prisma Commands
npx prisma generate
npx prisma migrate deploy
npm run seed

Start Backend
npm run dev


Local URL: http://localhost:8000

🗄 Database Design

Type: PostgreSQL

ORM: Prisma

Tables

Products

Users

Sales

Purchases

Expenses

ExpenseByCategory

Seeding

JSON-based seed data

Command: npm run seed

☁️ AWS Architecture

Request Flow:

User Browser
   ↓
AWS Amplify (SSR Frontend)
   ↓
AWS API Gateway
   ↓
AWS EC2 (Node.js Backend)
   ↓
AWS RDS (PostgreSQL)
   ↓
AWS S3 (Images)

🚢 Backend Deployment (EC2)

OS: Amazon Linux 2023

Process Manager: PM2

pm2 start ecosystem.config.js
pm2 save
pm2 startup

🖼 Image Storage

Service: AWS S3

Usage:

Product images

Profile images

Access: Public read access

🔁 CI/CD Pipeline
Frontend

Tool: AWS Amplify

Trigger: GitHub push

Result:

Automatic build

Automatic deployment

🔒 Security Practices

Environment variables for secrets

RDS is not publicly accessible

EC2 protected via security groups

API Gateway used for controlled access

⚡ Performance & SSR Benefits

Faster initial page load

SEO-friendly pages

Optimized server-side data fetching

👨‍💻 Author

Anuj Kumar

B.Tech (ECE), IIT Roorkee

Full-Stack Developer
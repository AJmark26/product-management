project:
  name: NEXTKART – SSR E-Commerce Product Management Dashboard
  type: Full Stack SSR Web Application
  description: >
    NEXTKART is a production-grade Server-Side Rendered (SSR) e-commerce
    product management dashboard built using Next.js, Node.js, Prisma,
    and AWS. It provides an admin interface to manage products, inventory,
    users, expenses, and sales analytics with real-world cloud deployment.

live_deployment:
  frontend:
    platform: AWS Amplify
    url: https://main.d3bew0nxud1hkz.amplifyapp.com
  backend:
    platform: AWS API Gateway + EC2
    url: https://2ezuzbxr51.execute-api.ap-south-1.amazonaws.com/prod

demo:
  video_duration: 3 minutes
  demo_video_link: "LINK"

features:
  dashboard:
    - Sales summary (weekly/monthly)
    - Purchase summary
    - Expense breakdown with charts
    - Customer growth analytics
    - Dues and pending orders
  inventory:
    - Product list with stock quantity
    - Price and rating visibility
  products:
    - Product cards with images
    - Stock availability
    - Ratings display
    - Create product UI
  users:
    - User listing
    - User ID, name, and email display
  settings:
    - Profile settings
    - Notification toggle
    - Dark mode toggle
    - Language preference
  expenses:
    - Filter by category and date
    - Pie-chart visualization
    - Category-wise expense analysis

tech_stack:
  frontend:
    - Next.js (App Router, SSR)
    - TypeScript
    - Tailwind CSS
    - Redux Toolkit
    - Recharts
  backend:
    - Node.js
    - Express.js
    - TypeScript
    - Prisma ORM
    - PostgreSQL
  cloud_and_devops:
    - AWS Amplify
    - AWS EC2 (Amazon Linux 2023)
    - AWS RDS (PostgreSQL)
    - AWS S3
    - AWS API Gateway
    - PM2

project_structure:
  root:
    - client:
        description: Next.js SSR frontend
    - server:
        description: Node.js backend with Prisma
    - README.md

local_setup:
  clone_repository:
    command: |
      git clone https://github.com/AJmark26/product-management.git
      cd product-management
  frontend_setup:
    commands: |
      cd client
      npm install
      npm run dev
    local_url: http://localhost:3000
  backend_setup:
    commands: |
      cd server
      npm install
    environment_variables:
      DATABASE_URL: postgresql://username:password@localhost:5432/productsmanagement
      PORT: 8000
    prisma_commands: |
      npx prisma generate
      npx prisma migrate deploy
      npm run seed
    start_backend: |
      npm run dev
    local_url: http://localhost:8000

database:
  type: PostgreSQL
  orm: Prisma
  tables:
    - Products
    - Users
    - Sales
    - Purchases
    - Expenses
    - ExpenseByCategory
  seeding:
    method: JSON-based seed files
    command: npm run seed

aws_architecture:
  flow:
    - User Browser
    - AWS Amplify (SSR Frontend)
    - AWS API Gateway
    - AWS EC2 (Node.js Backend)
    - AWS RDS (PostgreSQL)
    - AWS S3 (Images)

backend_deployment:
  ec2:
    os: Amazon Linux 2023
    process_manager: PM2
    commands: |
      pm2 start ecosystem.config.js
      pm2 save
      pm2 startup

image_storage:
  service: AWS S3
  usage:
    - Product images
    - Profile images
  access: Public read access

ci_cd:
  frontend:
    tool: AWS Amplify
    trigger: GitHub push
    result:
      - Automatic build
      - Automatic deployment

security:
  practices:
    - Environment variables for secrets
    - RDS not publicly accessible
    - EC2 protected via security groups
    - API Gateway used for controlled access

performance:
  rendering: Server-Side Rendering (SSR)
  benefits:
    - Faster initial load
    - SEO-friendly pages
    - Optimized data fetching

learning_outcomes:
  - Full-stack application development
  - Production-level AWS deployment
  - Prisma ORM with PostgreSQL
  - SSR with Next.js App Router
  - CI/CD using AWS Amplify
  - Cloud image hosting with S3

future_enhancements:
  - Authentication and authorization
  - Product CRUD operations
  - Order management
  - Pagination and advanced filters
  - Email notifications
  - Persistent dark mode

author:
  name: Anuj Kumar
  education: B.Tech (ECE), IIT Roorkee
  role: Full-Stack Developer

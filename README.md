# 📚 Lápiz de Encanto
A modern and functional online e-commerce store built with modern web technologies, designed to be easily deployed using Docker containers. It includes a complete admin panel, order system, email notifications, and product management.

![](https://github.com/josew383/lapiz-de-encanto/blob/master/LapizDeEncantoDemo.gif)

---

## 🚀 Technologies Used

### Frontend & Admin Panel
- **Astro** for modern and fast rendering
- **React** for dynamic components
- **Tailwind CSS** for responsive design
- **Umami** for lightweight, privacy-friendly analytics

### Backend (API)
- **Python with FastAPI** for a fast and modern REST API
- **SQLite** as a lightweight database for simple and self-contained environments
- **Email Notifier** integrated for order and status alerts

### Containerization & DevOps
- **Docker** for containerization
- **Docker Compose** for orchestration
- **DevContainers** for development in VSCode
- **Centralized environment variables** for flexible configuration

---

## 📋 Prerequisites
- Node.js (v18 or higher recommended)
- Python 3.10 or higher
- Docker and Docker Compose
- SMTP account or email delivery service for notifications

---

## Installation and Usage

1. **Clone the repository**

2. **Configure environment variables**:

   Each subproject (`admin`, `api`, `frontend`) has its own `.env` file.

   For full system configuration (email, Bizum, shipping), create and configure the `.env` file in each subproject:

   - **Admin**: Copy `admin/.env.example` to `admin/.env` and edit with your real values.
   - **Frontend**: Copy `frontend/.env.example` to `frontend/.env` and edit with your real values.
   - **API**: Copy `api/.env.example` to `api/.env` and edit with your real values.

3. **Run with Docker**:

```bash
docker compose up --build
```

4. **Access**:
   - Store: http://localhost:3000
   - Admin: http://localhost:3001
   - API: http://localhost:4000

## Development with Dev Containers (VS Code)

You can use [Dev Containers](https://code.visualstudio.com/docs/devcontainers/containers) for an integrated development environment, with hot-reload and real-time changes in all three services (API, Admin, and Frontend).

### Prerequisites

- Docker and Docker Compose installed
- Visual Studio Code
- "Dev Containers" extension by Microsoft

### First Use

1. Open a terminal in the project root.
2. If this is your first time, make sure you have the `.env` files configured as described below.
3. (If you don't have the Dev Containers CLI installed, install it with `npm install -g @devcontainers/cli`)
4. Run the following command to open the development environment in VS Code using Dev Containers:

   ```bash
   devcontainer up --workspace-folder=.
   ```

5. VS Code will automatically open in the development environment, without entering directly into any subproject.
6. The services will start in development mode and changes in the `api/`, `admin/`, and `frontend/` files will be instantly reflected (hot-reload).

---

## 🔗 Frontend-Backend Integration
- The frontend communicates with the backend via a **REST API using FastAPI**
- **Environment variables** are used to define routes and services
- Emails are sent via SMTP to notify about new orders and status changes
- Updates are logged with notes

---

## 💼 Functional Features

### Admin Functionalities

#### 📊 Dashboard
- Overview of orders, messages, and products
- Key performance indicators
- Quick access to pending tasks
- Notifications for new orders and messages

#### 📦 Order Management
- Unique ID generation with public link and QR code
- **Bizum** payment validation
- Logs recorded for every status change
- Email notifications to users and admin at each event

#### ✉️ Product Reviews
- User-submitted product reviews
- Admin review and moderation tools
- Visibility toggle and deletion tools

#### 🍭 Product Management
- Multiple images per product
- Highlighted discounted prices
- Limited or unlimited stock
- Configurable shipping costs with free shipping above a minimum amount
- Initial product load from `.json`

#### 💬 Messages (Contact Inquiries)
- Admin inbox for messages from contact form
- Message reading and reply management
- Archiving or deletion tools

#### 📧 Email Management
- Centralized log of all emails sent (orders, newsletters, contact replies)
- Templates for different email types
- SMTP delivery status overview

#### 📢 Newsletter
- Public subscription form
- Promotional email campaigns
- Export subscribers as `.csv`

#### 🔀 Coupons
- Coupon creation and management
- Discount application during checkout
- Configurable expiration dates and limits

#### 🧳 Sections
- Section manager for creating and editing landing page content
- Visual management of homepage blocks and promotions

### Frontend Functionalities

#### 📱 User Experience
- Fully responsive design
- Simplified menu on mobile devices
- Contact page
- Terms and conditions page

#### 📧 Email Notifications
- Users receive emails at every stage of the order
- Templates styled with inline CSS for compatibility

#### 💭 Messaging
- Contact form to reach the store
- Direct communication forwarded to admin panel

#### 📌 Order Tracking
- Public tracking page per order
- Live status updates
- QR code and direct link from confirmation email

#### 🔍 Product Filtering
- Filter by category, price range, and availability
- Sorting options (e.g. newest, most popular)
- Responsive filters for mobile devices

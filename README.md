# Food Delivery Application

A full-stack **MERN** (MongoDB, Express.js, React.js, Node.js) Food Delivery project that enables users to browse restaurants, place orders, and track deliveries in real time.

---

## 🚀 Features

* **User Registration & Authentication**

  * Secure signup/login with JWT
* **Restaurant & Menu Browsing**

  * List of restaurants with menus, search and filters
* **Cart & Checkout**

  * Add/remove items, apply discounts, calculate totals
* **Real-Time Order Tracking**

  * Live order status updates via Socket.io
* **Payment Integration**

  * Stripe for secure payment processing
* **Notifications**

  * SMS updates through Twilio (order confirmation, delivery status)
* **Responsive UI**

  * Mobile-first design using Tailwind CSS and React Router

---

## 🧰 Tech Stack

| Layer              | Technology                        |
| ------------------ | --------------------------------- |
| **Frontend**       | React, React Router, Tailwind CSS |
| **Backend**        | Node.js, Express.js               |
| **Database**       | MongoDB, Mongoose                 |
| **Real-Time**      | Socket.io                         |
| **Payments**       | Stripe API                        |
| **Messaging**      | Twilio API                        |
| **Authentication** | JSON Web Tokens (JWT)             |
| **Styling**        | Tailwind CSS                      |

---

## 📦 Project Structure

```
food-delivery/
├── backend/                  # Express API server
│   ├── controllers/          # Route handlers
│   ├── models/               # Mongoose schemas
│   ├── routes/               # API endpoints
│   ├── middleware/           # Auth, error handling
│   ├── sockets/              # Socket.io event handlers
│   ├── utils/                # Helpers (Stripe, Twilio)
│   ├── server.js             # App entry point
│   └── .env.example          # Environment variables template

├── frontend/                 # React client
│   ├── public/
│   ├── src/
│   │   ├── components/       # Reusable UI components
│   │   ├── pages/            # Route pages (Home, Menu, Cart, etc.)
│   │   ├── hooks/            # Custom React hooks
│   │   ├── services/         # API calls
│   │   ├── sockets/          # Socket.io client setup
│   │   ├── styles/           # Tailwind config
│   │   └── App.jsx           # App entry point
│   └── tailwind.config.js    # Tailwind CSS configuration

├── README.md                 # Project documentation
└── package.json              # Root scripts & dependencies
```

---

## 🔧 Prerequisites

* Node.js v14+ and npm or Yarn
* MongoDB (local or Atlas)
* Stripe account and API keys
* Twilio account and API credentials

---

## ⚙️ Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/food-delivery.git
cd food-delivery
```

### 2. Backend Setup

```bash
cd backend
npm install
```

* Copy `.env.example` to `.env` and configure:

```env
PORT=5000
MONGO_URI=your_mongo_connection_string
JWT_SECRET=your_jwt_secret
STRIPE_SECRET_KEY=your_stripe_secret_key
TWILIO_ACCOUNT_SID=your_twilio_sid
TWILIO_AUTH_TOKEN=your_twilio_token
TWILIO_PHONE_NUMBER=your_twilio_phone
```

### 3. Frontend Setup

```bash
cd ../frontend
npm install
```

* Create `.env.local`:

```env
VITE_API_BASE_URL=http://localhost:5000/api
```

### 4. Run the Application

* **Backend** (`backend/`):

  ```bash
  npm run dev
  # http://localhost:5000
  ```
* **Frontend** (`frontend/`):

  ```bash
  npm run dev
  # http://localhost:3000
  ```

Open your browser at `http://localhost:3000`.

---

## 📝 API Endpoints

* **Auth**

  * `POST /api/auth/register` – Sign up
  * `POST /api/auth/login` – Log in and receive JWT

* **Restaurants**

  * `GET /api/restaurants` – List all
  * `GET /api/restaurants/:id` – Details

* **Menu**

  * `GET /api/restaurants/:id/menu` – Menu items

* **Cart & Orders**

  * `POST /api/cart` – Add to cart
  * `GET /api/cart` – Get current cart
  * `POST /api/orders` – Place order (payment)
  * `GET /api/orders/:id` – Order status

* **Real-Time**

  * Socket.io events: `orderCreated`, `orderUpdated`

---

## 🎨 Customization

* **Tailwind**: Edit `tailwind.config.js` for theme settings.
* **Stripe**: Configure webhooks in `utils/stripe.js`.
* **Twilio**: Update messaging templates in `utils/twilio.js`.

---

## 📄 License

This project is developed solely by me and presented as my personal work. All rights reserved.

---

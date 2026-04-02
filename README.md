# Hotel Booking App

A full-stack web application for hotel room bookings, featuring user authentication, hotel management, and secure payment processing.

## 🚀 Features

### For Users

- **Browse Hotels & Rooms**: Explore available hotels and room types with detailed information
- **Secure Authentication**: User registration and login via Clerk
- **Room Booking**: Book rooms with date selection and guest count
- **My Bookings**: View and manage personal booking history
- **Payment Integration**: Secure payments through Stripe
- **Responsive Design**: Mobile-friendly interface built with Tailwind CSS

### For Hotel Owners

- **Hotel Registration**: Register and manage hotel properties
- **Room Management**: Add, list, and manage room inventory
- **Dashboard**: Owner dashboard for business insights
- **Image Upload**: Cloudinary integration for room photos

## 🛠️ Tech Stack

### Frontend

- **React 19** - Modern React with hooks and concurrent features
- **Vite** - Fast build tool and development server
- **Tailwind CSS** - Utility-first CSS framework
- **React Router** - Client-side routing
- **Axios** - HTTP client for API calls
- **Clerk** - Authentication and user management
- **React Hot Toast** - Toast notifications

### Backend

- **Node.js** - JavaScript runtime
- **Express.js** - Web application framework
- **MongoDB** - NoSQL database with Mongoose ODM
- **Clerk** - Server-side authentication
- **Stripe** - Payment processing
- **Cloudinary** - Image hosting and management
- **Nodemailer** - Email services
- **JWT** - JSON Web Tokens for authorization

## 📁 Project Structure

```
Hotel_Booking/
├── client/                 # React frontend
│   ├── public/
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   ├── pages/          # Page components
│   │   ├── context/        # React context for state management
│   │   └── assets/
│   ├── package.json
│   └── vite.config.js
├── server/                 # Node.js backend
│   ├── configs/            # Configuration files
│   ├── controllers/        # Route controllers
│   ├── middleware/         # Custom middleware
│   ├── models/             # MongoDB schemas
│   ├── routes/             # API routes
│   ├── package.json
│   └── server.js
└── README.md
```

## 🔧 Installation & Setup

### Prerequisites

- Node.js (v16 or higher)
- MongoDB database
- Clerk account for authentication
- Stripe account for payments
- Cloudinary account for image storage

### Backend Setup

1. Navigate to the server directory:

   ```bash
   cd server
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Create a `.env` file in the server directory with the following variables:

   ```env
   PORT=3000
   MONGODB_URI=your_mongodb_connection_string
   CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
   CLERK_SECRET_KEY=your_clerk_secret_key
   STRIPE_SECRET_KEY=your_stripe_secret_key
   CLOUDINARY_NAME=your_cloudinary_name
   CLOUDINARY_API_KEY=your_cloudinary_api_key
   CLOUDINARY_SECRET_KEY=your_cloudinary_secret_key
   EMAIL_USER=your_email_user
   EMAIL_PASS=your_email_password
   ```

4. Start the server:
   ```bash
   npm run server
   ```

### Frontend Setup

1. Navigate to the client directory:

   ```bash
   cd client
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Create a `.env` file in the client directory:

   ```env
   VITE_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
   VITE_BACKEND_URL=http://localhost:3000
   ```

4. Start the development server:
   ```bash
   npm run dev
   ```

## 🚀 Usage

1. **User Registration/Login**: Users can sign up or log in using Clerk authentication
2. **Browse Rooms**: Visit the homepage to see featured destinations and recommended hotels
3. **Room Details**: Click on any room to view detailed information, amenities, and pricing
4. **Make Booking**: Select check-in/check-out dates and number of guests to book a room
5. **Payment**: Complete payment securely through Stripe integration
6. **Hotel Owner Registration**: Hotel owners can register their properties
7. **Manage Rooms**: Owners can add rooms, upload images, and manage availability

## 📡 API Endpoints

### User Routes

- `POST /api/user/register` - User registration
- `POST /api/user/login` - User login
- `GET /api/user/profile` - Get user profile

### Hotel Routes

- `GET /api/hotels` - Get all hotels
- `POST /api/hotels` - Create new hotel (owner only)
- `GET /api/hotels/:id` - Get hotel details

### Room Routes

- `GET /api/rooms` - Get all rooms
- `POST /api/rooms` - Add new room (owner only)
- `GET /api/rooms/:id` - Get room details
- `PUT /api/rooms/:id` - Update room (owner only)

### Booking Routes

- `POST /api/bookings` - Create new booking
- `GET /api/bookings/user` - Get user's bookings
- `PUT /api/bookings/:id/cancel` - Cancel booking

## 🔐 Authentication

The application uses Clerk for authentication, providing:

- User registration and login
- Secure session management
- User profile management
- Social login options

## 💳 Payment Integration

Stripe is integrated for secure payment processing:

- Card payments
- Payment confirmation
- Webhook handling for payment status updates

## 🖼️ Image Management

Cloudinary is used for image storage and optimization:

- Room photo uploads
- Image resizing and optimization
- Secure image URLs

## 📧 Email Services

Nodemailer handles email communications:

- Booking confirmations
- Payment receipts
- Owner notifications

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the ISC License.

## 📞 Support

For support or questions, please open an issue in the GitHub repository.

---

Built with ❤️ using React, Node.js, and MongoDB

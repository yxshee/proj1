# MyShop - E-Commerce Website

A full-featured e-commerce platform built with Next.js, MongoDB, and modern web technologies. This application provides a complete shopping experience with user authentication, product management, shopping cart, checkout process, and admin dashboard.

## 🚀 Features

### Customer Features
- **Product Browsing**: Browse products with featured carousel and category filtering
- **User Authentication**: Secure login/signup with NextAuth.js
- **Shopping Cart**: Add/remove products, update quantities
- **Checkout Process**: Complete order placement with shipping and payment
- **Order History**: View past orders and order status
- **Product Reviews**: Rate and review products
- **Search Functionality**: Search products by name and category
- **Responsive Design**: Mobile-friendly interface with Tailwind CSS

### Admin Features
- **Dashboard**: Overview of sales, orders, and products
- **Product Management**: Add, edit, delete products with image upload
- **Order Management**: View and update order status, mark as delivered
- **User Management**: View and manage user accounts
- **Analytics**: Sales charts and statistics

### Payment & Media
- **PayPal Integration**: Secure payment processing
- **Cloudinary Integration**: Image upload and management
- **MongoDB Database**: Robust data storage with Mongoose ODM

## 🛠️ Tech Stack

- **Frontend**: Next.js 13, React 18, Tailwind CSS
- **Backend**: Next.js API Routes, MongoDB with Mongoose
- **Authentication**: NextAuth.js
- **Payment**: PayPal React SDK
- **Media**: Cloudinary
- **Charts**: Chart.js with react-chartjs-2
- **Forms**: React Hook Form
- **Notifications**: React Toastify
- **Icons**: Heroicons
- **UI Components**: Headless UI

## 📋 Prerequisites

Before running this application, make sure you have:
- Node.js (v16 or higher)
- MongoDB database (local or cloud)
- PayPal developer account
- Cloudinary account

## 🔧 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yxshee/proj1.git
   cd proj1
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Environment Setup**
   - Copy the sample environment file:
     ```bash
     cp sample_ENV_file.txt .env.local
     ```
   - Update the `.env.local` file with your actual credentials:
     ```
     MONGODB_URL=your_mongodb_connection_string
     NEXTAUTH_URL=http://localhost:3000
     NEXTAUTH_SECRET=your_nextauth_secret
     NEXT_PUBLIC_CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
     NEXT_PUBLIC_CLOUDINARY_API_KEY=your_cloudinary_api_key
     CLOUDINARY_SECRET=your_cloudinary_secret
     ```

4. **Database Setup**
   - Ensure MongoDB is running locally or use a cloud service like MongoDB Atlas
   - The application will automatically create collections and indexes

## 🚀 Running the Application

### Development Mode
```bash
npm run dev
```
Open [http://localhost:3000](http://localhost:3000) in your browser.

### Production Build
```bash
npm run build
npm start
```

### Linting
```bash
npm run lint
```

## 📁 Project Structure

```
my-shop/
├── components/          # Reusable React components
│   ├── Layout.js       # Main layout component
│   ├── ProductItem.js  # Product display component
│   ├── CheckoutWizard.js # Checkout steps component
│   └── ...
├── models/             # MongoDB models
│   ├── Product.js      # Product schema
│   ├── User.js         # User schema
│   ├── Order.js        # Order schema
│   └── ...
├── pages/              # Next.js pages and API routes
│   ├── index.js        # Home page
│   ├── cart.js         # Shopping cart page
│   ├── login.js        # Login page
│   ├── api/            # API endpoints
│   │   ├── auth/       # Authentication routes
│   │   ├── products/   # Product CRUD routes
│   │   ├── orders/     # Order management routes
│   │   └── admin/      # Admin-only routes
│   └── admin/          # Admin pages
│       ├── dashboard.js
│       ├── products.js
│       └── ...
├── public/             # Static assets
├── styles/             # Global styles
│   └── globals.css
├── utils/              # Utility functions
│   ├── db.js           # Database connection
│   ├── Store.js        # Global state management
│   └── error.js        # Error handling
├── package.json
├── next.config.js
├── tailwind.config.js
└── README.md
```

## 🔐 Authentication

The application uses NextAuth.js for authentication with the following providers:
- Credentials (email/password)
- Custom signup functionality

Admin users can be created by setting `isAdmin: true` in the user document in MongoDB.

## 💳 Payment Integration

PayPal integration is handled through the PayPal React SDK. The payment flow includes:
1. Order creation
2. PayPal approval
3. Payment capture
4. Order status update

## 🖼️ Media Management

Product images are uploaded to Cloudinary with the following features:
- Image optimization
- Multiple format support
- Secure URL generation

## 📊 Admin Dashboard

The admin dashboard provides:
- Sales overview with charts
- Order management (view, update status, mark delivered)
- Product CRUD operations
- User management
- Analytics and reporting

## 🔒 Security Features

- Password hashing with bcryptjs
- JWT tokens for session management
- Protected API routes
- Input validation and sanitization
- CORS configuration

## 📱 Responsive Design

The application is fully responsive and optimized for:
- Desktop computers
- Tablets
- Mobile devices

Built with Tailwind CSS for consistent styling and responsive breakpoints.

## 🧪 Testing

Currently, the application does not include automated tests. Manual testing is recommended for:
- User registration and login
- Product browsing and search
- Cart functionality
- Checkout process
- Admin operations

## 🚀 Deployment

### Vercel (Recommended)
1. Connect your GitHub repository to Vercel
2. Add environment variables in Vercel dashboard
3. Deploy automatically on push

### Other Platforms
The application can be deployed to any platform supporting Node.js:
- Heroku
- DigitalOcean App Platform
- AWS Elastic Beanstalk
- Self-hosted with PM2

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Built with [Next.js](https://nextjs.org/)
- UI components from [Tailwind CSS](https://tailwindcss.com/)
- Icons from [Heroicons](https://heroicons.com/)
- Charts from [Chart.js](https://www.chartjs.org/)

## 📞 Support

If you have any questions or need help, please open an issue on GitHub.

---

**Note**: This is a learning project and may contain bugs or security vulnerabilities. Use at your own risk in production environments.
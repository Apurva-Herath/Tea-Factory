Tea Factory Management System

A comprehensive full-stack web application for managing tea factory operations, including employee management, inventory tracking, supplier coordination, customer orders, delivery logistics, and maintenance scheduling.

Features

Core Modules
- **Employee Management** - Employee records, attendance tracking, leave management, salary processing
- **Inventory Management** - Stock tracking, warehouse management, reorder alerts, purchase orders
- **Supplier Portal** - Supplier registration, order management, communication system
- **Customer Management** - Customer accounts, bulk orders, sales tracking, auctions
- **Delivery System** - Real-time GPS tracking, route optimization, driver management
- **Maintenance** - Equipment maintenance scheduling and tracking
- **Department Management** - Department organization and administration
- **Technician Management** - Technician records and assignments

Additional Features
- Role-based authentication (Admin, Employee, Supplier, Customer)
- Real-time notifications
- Interactive dashboards with charts and analytics
- PDF report generation
- Excel export functionality
- AI-powered chatbot assistance
- Mobile-responsive design

Tech Stack

Frontend
- **React** 19.1.1 - UI framework
- **React Router DOM** - Navigation
- **Material-UI (MUI)** - Component library
- **TailwindCSS** - Styling
- **Chart.js & Recharts** - Data visualization
- **Axios** - HTTP client
- **React Leaflet** - Map integration
- **jsPDF** - PDF generation
- **React Toastify** - Notifications

Backend
- **Node.js** with **Express** 5.1.0
- **MongoDB** with **Mongoose** 8.17.1
- **JWT** - Authentication
- **Bcrypt** - Password hashing
- **Multer** - File uploads
- **Nodemailer** - Email notifications
- **OpenAI** - AI integration
- **PDFKit** - PDF generation
- **Node-cron** - Scheduled tasks

Prerequisites

- Node.js (v14 or higher)
- MongoDB (v4.4 or higher)
- npm or yarn package manager

Installation

1. Clone the repository
```bash
git clone https://github.com/Apurva-Herath/Tea-Factory.git
cd tea
```

2. Backend Setup
```bash
cd backend
npm install
```

Create a `.env` file in the backend directory with the following variables:
```env
PORT=5000
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
EMAIL_USER=your_email@example.com
EMAIL_PASS=your_email_password
OPENAI_API_KEY=your_openai_api_key
```

3. Frontend Setup
```bash
cd ../frontend
npm install
```

Create a `.env` file in the frontend directory:
```env
REACT_APP_API_URL=http://localhost:5000
```
Running the Application

### Start Backend Server
```bash
cd backend
node server.js
```
The backend will run on `http://localhost:5000`

### Start Frontend Development Server
```bash
cd frontend
npm start
```
The frontend will run on `http://localhost:3000`

Database Seeding

To populate the database with initial data:

```bash
cd backend
npm run seed:all
```

Or seed individually:
```bash
npm run seed              # Seed suppliers
npm run seed:inventory    # Seed inventory
```

 Project Structure

```
tea/
├── backend/
│   ├── controllers/      # Request handlers
│   ├── model/           # Mongoose models
│   ├── routes/          # API routes
│   ├── services/        # Business logic
│   ├── middleware.js    # Custom middleware
│   ├── server.js        # Entry point
│   └── package.json
│
├── frontend/
│   ├── public/          # Static files
│   ├── src/
│   │   ├── components/  # React components
│   │   ├── pages/       # Page components
│   │   ├── contexs/     # Context providers
│   │   ├── utils/       # Helper functions
│   │   ├── services/    # API services
│   │   └── App.js       # Main app component
│   └── package.json
│
└── README.md
```

User Roles

- **Admin** - Full system access and management
- **Employee** - Access to employee portal and assigned tasks
- **Supplier** - Supplier portal for order management
- **Customer** - Customer portal for placing orders and tracking

Key Functionalities

### For Administrators
- Manage employees, departments, and salaries
- Track inventory and generate purchase orders
- Monitor deliveries and assign drivers
- View comprehensive analytics and reports
- Manage suppliers and customers

### For Employees
- Clock in/out for attendance
- Apply for and track leave requests
- View salary information
- Access assigned tasks

### For Suppliers
- Receive and manage orders
- Update product availability
- Track payment status
- Communicate with admin

### For Customers
- Browse tea varieties
- Place bulk orders
- Participate in auctions
- Track order status and deliveries

Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

License

This project is licensed under the ISC License.

##  Authors

- Apurva Herath

##  Contact

For any queries or support, please contact the development team.

---

**Note:** Make sure to configure all environment variables properly before running the application. Never commit `.env` files to version control.

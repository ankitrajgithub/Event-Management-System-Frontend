# Event Horizon Frontend

A modern React-based frontend application for an event management and booking platform. Built with Vite, React Router, and Tailwind CSS.

## 🌟 Features

- **User Authentication**: Secure login and registration with OTP verification
- **Event Discovery**: Browse and explore available events
- **Event Booking**: Book tickets for events with integrated payment processing
- **Admin Dashboard**: Manage events and view booking confirmations
- **User Dashboard**: View booking history and manage profile
- **Responsive Design**: Mobile-friendly interface using Tailwind CSS
- **State Management**: Context API for authentication and user state

## 🛠️ Tech Stack

- **Frontend Framework**: React 18
- **Build Tool**: Vite
- **Styling**: Tailwind CSS
- **Routing**: React Router DOM v6
- **HTTP Client**: Axios
- **Icons**: React Icons
- **Task Automation**: PostCSS with Autoprefixer

## 📋 Prerequisites

- Node.js (v14 or higher)
- npm or yarn

## 🚀 Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd Event\ Horizon\ Frontend
```

2. Navigate to the client directory:
```bash
cd client
```

3. Install dependencies:
```bash
npm install
```

4. Create a `.env` file in the client directory:
```env
VITE_BACKEND_URL=https://event-horizon-9udy.onrender.com
```

## 🏃 Running the Application

### Development Server
```bash
npm run dev
```
The application will be available at `http://localhost:5173` by default.

### Build for Production
```bash
npm run build
```

### Preview Production Build
```bash
npm run preview
```

### Lint Code
```bash
npm run lint
```

## 📁 Project Structure

```
client/
├── src/
│   ├── components/
│   │   └── Navbar.jsx              # Navigation component
│   ├── context/
│   │   └── AuthContext.jsx         # Authentication context
│   ├── pages/
│   │   ├── AdminDashboard.jsx      # Admin management panel
│   │   ├── EventDetail.jsx         # Event details page
│   │   ├── Home.jsx                # Home/Events listing
│   │   ├── Login.jsx               # Login with OTP
│   │   ├── PaymentFailed.jsx       # Payment failure page
│   │   ├── PaymentSuccess.jsx      # Payment success page
│   │   ├── Register.jsx            # User registration
│   │   └── UserDashboard.jsx       # User bookings dashboard
│   ├── utils/
│   │   └── axios.js                # Axios instance with interceptors
│   ├── App.jsx                     # Main app component
│   ├── main.jsx                    # Entry point
│   └── index.css                   # Global styles
├── index.html
├── package.json
├── vite.config.js
├── tailwind.config.js
└── postcss.config.js
```

## 🔐 Authentication Flow

1. **Registration**: Users create an account with email and password
2. **OTP Verification**: An OTP is sent to the registered email
3. **Login**: Authenticated users receive a JWT token stored in localStorage
4. **Role-based Routing**: Users are redirected based on their role (admin/user)

## 🌐 API Integration

All backend API calls are made through the centralized Axios instance in `src/utils/axios.js`, which:
- Uses the `VITE_BACKEND_URL` environment variable
- Automatically attaches JWT tokens to requests via interceptors
- Handles authentication headers

## 📝 Environment Variables

Create a `.env` file in the `client` directory:

```env
VITE_BACKEND_URL=<your-backend-url>
```

## 🎯 Key Components

### AuthContext.jsx
Provides global authentication state management:
- `login()`: Authenticate user with email/password
- `register()`: Create new user account
- `verifyOTP()`: Verify OTP for account activation
- User and loading states

### Pages
- **Home**: Displays list of available events
- **EventDetail**: Shows detailed information about a selected event
- **Login**: User authentication with OTP support
- **Register**: New user account creation
- **UserDashboard**: User's booking history and profile
- **AdminDashboard**: Event and booking management
- **PaymentSuccess/PaymentFailed**: Payment status pages

## 🔗 API Endpoints Used

- `POST /auth/login` - User login
- `POST /auth/register` - User registration
- `POST /auth/verify-otp` - OTP verification
- `GET /events` - Fetch all events
- `POST /events` - Create new event (admin)
- `DELETE /events/:id` - Delete event (admin)
- `GET /bookings/my` - Fetch user bookings
- `PUT /bookings/:id/confirm` - Confirm booking with payment status (admin)

## 🎨 Styling

The project uses Tailwind CSS for styling with a responsive design approach. Global styles are defined in `src/index.css`.

## 📄 License

This project is part of the Event Horizon platform.

## 👨‍💻 Contributing

To contribute to this project:
1. Create a feature branch
2. Make your changes
3. Test thoroughly
4. Submit a pull request

## 🤝 Support

For issues or questions, please contact the development team.

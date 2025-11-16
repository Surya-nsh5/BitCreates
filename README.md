# 🐛 FinBug - Personal Finance Tracker

A modern, AI-powered finance tracking application that helps you manage your income and expenses with beautiful visualizations and intelligent insights.

## ✨ Features

- 📊 **Visual Analytics** - Beautiful charts and graphs to understand your spending patterns
- 🤖 **AI-Powered Insights** - Get intelligent financial advice using Google Gemini AI
- 📸 **Bill Scanning** - Upload and extract data from bills automatically
- 📥 **Bulk Import/Export** - Import transactions via CSV and export to Excel
- 🎨 **Custom Categories** - Organize expenses with emoji icons and custom categories
- 🔐 **Secure Authentication** - JWT-based authentication with encrypted passwords
- 📱 **Responsive Design** - Works seamlessly on desktop and mobile devices
- 🌙 **Modern UI** - Clean interface built with React and Tailwind CSS

## 🛠️ Tech Stack

### Frontend
- **React 19** - UI library
- **Vite** - Build tool and dev server
- **Tailwind CSS** - Styling
- **React Router** - Navigation
- **Recharts** - Data visualization
- **Axios** - HTTP client
- **React Hot Toast** - Notifications
- **Moment.js** - Date handling

### Backend
- **Node.js & Express** - Server framework
- **MongoDB & Mongoose** - Database
- **JWT** - Authentication
- **bcryptjs** - Password hashing
- **Multer** - File uploads
- **XLSX** - Excel file generation
- **Google Gemini AI** - AI-powered insights

## 📋 Prerequisites

- Node.js (v14 or higher)
- MongoDB (local or Atlas)
- Google Gemini API key
- Web3Forms access key (for contact form)

## 🚀 Installation

### 1. Clone the repository
```bash
git clone <your-repo-url>
cd <project-folder>
```

### 2. Backend Setup
```bash
cd backend
npm install
```

Create a `.env` file in the `backend` folder:
```env
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
PORT=8000
GEMINI_API_KEY=your_gemini_api_key
```

Start the backend server:
```bash
npm start
# or for development with auto-reload
npm run dev
```

### 3. Frontend Setup
```bash
cd frontend/finance-tracker
npm install
```

Create a `.env` file in the `frontend/finance-tracker` folder:
```env
VITE_WEB3FORMS_ACCESS_KEY=your_web3forms_access_key
VITE_API_URL=http://localhost:8000
```

Start the frontend development server:
```bash
npm run dev
```

The application will be available at `http://localhost:5173`

## 📁 Project Structure

```
├── backend/
│   ├── config/          # Database configuration
│   ├── controllers/     # Request handlers
│   ├── middleware/      # Auth & file upload middleware
│   ├── models/          # MongoDB schemas
│   ├── routes/          # API routes
│   ├── services/        # Business logic
│   ├── utils/           # Helper functions
│   └── server.js        # Entry point
│
└── frontend/
    └── finance-tracker/
        ├── src/
        │   ├── assets/      # Images & videos
        │   ├── components/  # Reusable components
        │   ├── context/     # React context
        │   ├── hooks/       # Custom hooks
        │   ├── pages/       # Page components
        │   └── utils/       # Helper functions
        └── dist/            # Production build
```

## 🔑 Environment Variables

### Backend (.env)
| Variable | Description |
|----------|-------------|
| `MONGO_URI` | MongoDB connection string |
| `JWT_SECRET` | Secret key for JWT tokens |
| `PORT` | Server port (default: 8000) |
| `GEMINI_API_KEY` | Google Gemini API key for AI features |

### Frontend (.env)
| Variable | Description |
|----------|-------------|
| `VITE_WEB3FORMS_ACCESS_KEY` | Web3Forms API key for contact form |
| `VITE_API_URL` | Backend API URL |

## 📡 API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - Login user

### Income
- `POST /api/income/add` - Add income
- `GET /api/income/get` - Get all income
- `DELETE /api/income/:id` - Delete income
- `GET /api/income/downloadexcel` - Download income as Excel
- `POST /api/income/bulk-upload` - Bulk upload via CSV

### Expenses
- `POST /api/expense/add` - Add expense
- `GET /api/expense/get` - Get all expenses
- `DELETE /api/expense/:id` - Delete expense
- `GET /api/expense/downloadexcel` - Download expenses as Excel
- `POST /api/expense/bulk-upload` - Bulk upload via CSV

### Dashboard
- `GET /api/dashboard/stats` - Get financial statistics

### AI Insights
- `POST /api/ai/insights` - Get AI-powered financial advice

### Bill Scanning
- `POST /api/bill/scan` - Upload and scan bill

## 🎯 Features in Detail

### Income & Expense Tracking
- Add transactions with custom categories and emoji icons
- View transaction history sorted by date
- Delete transactions individually

### Data Visualization
- Pie charts for expense distribution
- Line charts for income vs expense trends
- Monthly spending analysis

### Bulk Operations
- Import multiple transactions via CSV upload
- Export all data to Excel format
- Automatic data validation and error reporting

### AI Financial Advisor
- Get personalized financial insights
- Spending pattern analysis
- Budget recommendations

### Bill Scanning
- Upload bill images
- Automatic data extraction
- Quick transaction creation

## 🚢 Deployment

### Frontend (Vercel/Netlify)
1. Push code to GitHub
2. Connect repository to Vercel/Netlify
3. Set environment variables in platform settings
4. Deploy

### Backend (Render/Railway)
1. Push code to GitHub
2. Connect repository to hosting platform
3. Set environment variables
4. Deploy with build command: `npm install`
5. Start command: `npm start`

## 🔒 Security

- Passwords are hashed using bcryptjs
- JWT tokens for secure authentication
- Protected API routes with middleware
- Environment variables for sensitive data
- CORS enabled for frontend-backend communication

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 👨‍💻 Author

Made with ❤️ by 

## 🐛 Bug Reports

If you find any bugs, please open an issue on GitHub.

---

**Note:** Remember to never commit your `.env` files to version control. They contain sensitive information and are already included in `.gitignore`.

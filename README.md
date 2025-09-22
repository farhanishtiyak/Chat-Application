# Real-Time Chat Application

A full-stack real-time messaging application built with the MERN stack, featuring instant messaging, user authentication, and live online status tracking.

![Chat Application](https://img.shields.io/badge/MERN-Stack-blue) ![Socket.IO](https://img.shields.io/badge/Socket.IO-Real--time-green) ![JWT](https://img.shields.io/badge/JWT-Authentication-orange)

## 🌐 Live Demo

🔗 **[Try the Live Application](https://pingme-ojyy.onrender.com/login)**

*Note: The app may take a moment to load initially due to Render's free tier cold start.*

## 🚀 Features

- **Real-time Messaging**: Instant message delivery using Socket.IO
- **User Authentication**: Secure signup/login with JWT tokens and bcrypt password hashing
- **Online Status**: Live tracking of online/offline users
- **Responsive Design**: Modern UI built with React, Tailwind CSS, and DaisyUI
- **Avatar Generation**: Automatic profile picture generation based on gender
- **Message History**: Persistent conversation storage in MongoDB
- **Protected Routes**: Secure navigation with authentication middleware
- **Toast Notifications**: User-friendly feedback with react-hot-toast
- **State Management**: Efficient state handling with Zustand
- **Docker Support**: Containerized deployment ready

## 🛠️ Tech Stack

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** - Database with Mongoose ODM
- **Socket.IO** - Real-time bidirectional communication
- **JWT** - JSON Web Tokens for authentication
- **bcryptjs** - Password hashing
- **cookie-parser** - Cookie handling middleware

### Frontend
- **React 18** - UI library with hooks
- **Vite** - Build tool and dev server
- **Tailwind CSS** - Utility-first CSS framework
- **DaisyUI** - Component library for Tailwind
- **React Router DOM** - Client-side routing
- **Socket.IO Client** - Real-time connection
- **Zustand** - Lightweight state management
- **React Hot Toast** - Notification system
- **React Icons** - Icon library

### DevOps & Tools
- **Docker** - Containerization
- **Docker Compose** - Multi-container deployment
- **Nodemon** - Development server auto-restart
- **ESLint** - Code linting
- **PostCSS** - CSS processing
- **Autoprefixer** - CSS vendor prefixing

## 📦 Installation

### Prerequisites
- Node.js (v18 or higher)
- MongoDB (local or cloud)
- npm or yarn

### Local Development

1. **Clone the repository**
   ```bash
   git clone https://github.com/farhanishtiyak/Chat-Application.git
   cd Chat-Application
   ```

2. **Install dependencies**
   ```bash
   # Install backend dependencies
   npm install
   
   # Install frontend dependencies
   cd frontend
   npm install
   cd ..
   ```

3. **Environment Setup**
   Create a `.env` file in the root directory:
   ```env
   PORT=5000
   MONGO_DB_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret_key
   NODE_ENV=development
   ```

4. **Start the application**
   
   **Development mode (with auto-reload):**
   ```bash
   npm run server
   ```
   
   **Or start frontend and backend separately:**
   ```bash
   # Terminal 1 - Backend
   npm run server
   
   # Terminal 2 - Frontend
   cd frontend
   npm run dev
   ```

5. **Access the application**
   - Frontend: `http://localhost:3000`
   - Backend API: `http://localhost:5000`

### Docker Deployment

1. **Using Docker Compose**
   ```bash
   docker-compose up --build
   ```

2. **Access the application**
   - Application: `http://localhost:3000`

## 🏗️ Project Structure

```
Chat-Application/
├── backend/
│   ├── controllers/          # Route handlers
│   │   ├── auth.controller.js
│   │   ├── message.controller.js
│   │   └── user.controller.js
│   ├── db/                   # Database configuration
│   │   └── connectToMongoDB.js
│   ├── middleware/           # Custom middleware
│   │   └── protectRoute.js
│   ├── models/               # Mongoose schemas
│   │   ├── conversation.model.js
│   │   ├── message.model.js
│   │   └── user.model.js
│   ├── routes/               # API routes
│   │   ├── auth.routes.js
│   │   ├── message.routes.js
│   │   └── user.routes.js
│   ├── socket/               # Socket.IO configuration
│   │   └── socket.js
│   ├── utils/                # Utility functions
│   │   └── generateToken.js
│   └── server.js             # Main server file
├── frontend/
│   ├── public/               # Static assets
│   ├── src/
│   │   ├── components/       # React components
│   │   │   ├── messages/
│   │   │   ├── sidebar/
│   │   │   └── skeletons/
│   │   ├── context/          # React contexts
│   │   ├── hooks/            # Custom hooks
│   │   ├── pages/            # Page components
│   │   ├── utils/            # Utility functions
│   │   └── zustand/          # State management
│   └── package.json
├── docker-compose.yml
├── Dockerfile
└── package.json
```

## 🔌 API Endpoints

### Authentication
- `POST /api/auth/signup` - User registration
- `POST /api/auth/login` - User login
- `POST /api/auth/logout` - User logout

### Messages
- `GET /api/messages/:id` - Get conversation messages
- `POST /api/messages/send/:id` - Send message

### Users
- `GET /api/users` - Get users for sidebar

## 🔧 Environment Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `PORT` | Server port | `5000` |
| `MONGO_DB_URI` | MongoDB connection string | `mongodb://localhost:27017/chatapp` |
| `JWT_SECRET` | JWT signing secret | `your-secret-key` |
| `NODE_ENV` | Environment mode | `development` or `production` |

## 🚀 Deployment

### Production Build
```bash
npm run build
npm start
```

### Docker Production
```bash
docker-compose -f docker-compose.prod.yml up --build
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the ISC License - see the [LICENSE](LICENSE) file for details.

## 👤 Author

**Farhan Ishtiyak**
- GitHub: [@farhanishtiyak](https://github.com/farhanishtiyak)

## 🙏 Acknowledgments

- Icons from React Icons
- UI components from DaisyUI
- Real-time functionality powered by Socket.IO

---

⭐ Star this repository if you found it helpful!

# IPL Auction Platform 🏏

A comprehensive web-based IPL auction management system built with React, Node.js, and MongoDB. This platform enables real-time bidding, player management, and team coordination for IPL-style cricket auctions.

## 🚀 Project Overview

The IPL Auction Platform is a full-stack application that provides:
- **Real-time bidding system** with WebSocket support
- **Player management** with detailed statistics and images
- **Team management** for IPL franchises
- **Admin dashboard** for auction control
- **Live auction interface** for participants
- **Responsive design** for mobile and desktop

## 🏗️ Architecture

This project follows a microservices architecture with three main components:

### Frontend Applications
- **Admin Panel** (`IPL_AUCTION_ADMIN/`) - Administrative interface
- **Client Application** (`IPL_AUCTION_CLIENT/`) - User-facing auction interface

### Backend Services
- **API Server** (`IPL_AUCTION_BACKEND/`) - RESTful API with WebSocket support
- **Database** - MongoDB for data persistence

## 📁 Project Structure

```
IPL_AUCTION/
├── IPL_AUCTION_ADMIN/          # Admin Dashboard
│   ├── src/
│   │   ├── Pages/             # Admin pages
│   │   ├── components/        # Reusable components
│   │   └── ...
│   └── public/                # Static assets
├── IPL_AUCTION_BACKEND/       # Node.js API
│   ├── controllers/           # API controllers
│   ├── model/                 # Database models
│   ├── routes/                # API routes
│   ├── src/                   # WebSocket server
│   └── ...
├── IPL_AUCTION_CLIENT/        # User Interface
│   ├── src/
│   │   ├── Pages/             # User pages
│   │   ├── components/        # UI components
│   │   └── ...
│   └── public/                # Static assets
└── README.md
```

## 🛠️ Technology Stack

### Frontend
- **React 18** - UI framework
- **Vite** - Build tool
- **Tailwind CSS** - Styling
- **React Router** - Navigation
- **Axios** - HTTP client
- **WebSocket** - Real-time updates

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** - Database
- **Mongoose** - ODM
- **Socket.io** - Real-time communication
- **JWT** - Authentication

### Deployment
- **Vercel** - Frontend hosting
- **Render/Heroku** - Backend hosting
- **MongoDB Atlas** - Database hosting

## 🚀 Quick Start

### Prerequisites
- Node.js (v16 or higher)
- MongoDB
- npm or yarn

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/your-username/IPL_AUCTION.git
cd IPL_AUCTION
```

2. **Install backend dependencies**
```bash
cd IPL_AUCTION_BACKEND
npm install
```

3. **Install admin panel dependencies**
```bash
cd ../IPL_AUCTION_ADMIN
npm install
```

4. **Install client dependencies**
```bash
cd ../IPL_AUCTION_CLIENT
npm install
```

5. **Set up environment variables**
Create `.env` files in backend and frontend directories:
```bash
# Backend (.env)
MONGODB_URI=mongodb://localhost:27017/ipl_auction
JWT_SECRET=your_jwt_secret
PORT=5000

# Frontend (.env)
VITE_API_URL=http://localhost:5000/api
```

6. **Start the development servers**

Backend:
```bash
cd IPL_AUCTION_BACKEND
npm run dev
```

Admin Panel:
```bash
cd IPL_AUCTION_ADMIN
npm run dev
```

Client:
```bash
cd IPL_AUCTION_CLIENT
npm run dev
```

## 📊 Features

### Admin Features
- **Player Management**
  - Add/edit/delete players
  - Upload player images
  - Set base prices and categories

- **Team Management**
  - Create/edit teams
  - Assign team budgets
  - Manage team rosters

- **Auction Control**
  - Start/stop auctions
  - Set bidding timers
  - Monitor real-time bidding

- **Analytics Dashboard**
  - Track team spending
  - View player statistics

### User Features
- **Live Auction Interface**
  - Real-time bidding updates
  - Player countdown timers
  - Bid history tracking

- **Team Dashboard**
  - View team composition
  - Track remaining budget
  - Player statistics

- **Player Profiles**
  - Detailed player information
  - Performance statistics
  - Images and videos

## 🔌 API Endpoints

### Authentication
- `POST /api/auth/login` - User login
- `POST /api/auth/register` - User registration
- `POST /api/auth/logout` - User logout

### Players
- `GET /api/players` - Get all players
- `GET /api/players/:id` - Get specific player
- `POST /api/players` - Add new player (admin)
- `PUT /api/players/:id` - Update player (admin)
- `DELETE /api/players/:id` - Delete player (admin)

### Teams
- `GET /api/teams` - Get all teams
- `GET /api/teams/:id` - Get specific team
- `POST /api/teams` - Create team (admin)
- `PUT /api/teams/:id` - Update team (admin)
- `DELETE /api/teams/:id` - Delete team (admin)

### Auction
- `GET /api/auction/status` - Get auction status
- `POST /api/auction/start` - Start auction (admin)
- `POST /api/auction/stop` - Stop auction (admin)
- `POST /api/auction/bid` - Place bid
- `GET /api/auction/history` - Get bid history

## 🔄 Real-time Events

### WebSocket Events
- `player_update` - Player status changed
- `new_bid` - New bid placed
- `auction_start` - Auction started
- `auction_end` - Auction ended

## 🎨 UI Components

### Admin Components
- `AddPlayer` - Player creation form
- `AddTeam` - Team creation form
- `BidConfig` - Auction settings
- `UploadImages` - Image upload interface

### Client Components
- `Playercard` - Player display card
- `Teamcard` - Team display card
- `ParticleField` - Animated background
- `ConfettiComponent` - Celebration animation

## 🧪 Testing

### Running Tests
```bash
# Backend tests
cd IPL_AUCTION_BACKEND
npm test

# Frontend tests
cd IPL_AUCTION_ADMIN
npm test

cd ../IPL_AUCTION_CLIENT
npm test
```

## 🚀 Deployment

### Production Build
```bash
# Build admin panel
cd IPL_AUCTION_ADMIN
npm run build

# Build client
cd ../IPL_AUCTION_CLIENT
npm run build

# Start production server
cd ../IPL_AUCTION_BACKEND
npm start
```

### Environment Variables for Production
```bash
# Backend
MONGODB_URI=mongodb+srv://...
JWT_SECRET=production_secret
PORT=5000
NODE_ENV=production

# Frontend
VITE_API_URL=https://your-api-domain.com/api
```

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request
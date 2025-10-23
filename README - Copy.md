# AI Trip Planner

A comprehensive travel planning application powered by Google Gemini AI, built with React and Node.js.

## Features

- 🤖 **AI-Powered Recommendations**: Get personalized travel suggestions using Google Gemini AI
- 🗺️ **Smart Itinerary Generation**: Automatically create day-by-day itineraries
- 📸 **Photo Gallery**: Browse beautiful travel photos for inspiration
- 👤 **User Authentication**: Secure user accounts with preferences
- 💾 **Database Storage**: MongoDB for storing user data and travel plans
- 📱 **Responsive Design**: Works on desktop, tablet, and mobile devices
- 🎨 **Modern UI**: Beautiful, intuitive interface built with React

## Tech Stack

### Frontend
- React 18
- React Router DOM
- Styled Components
- React Hook Form
- React Toastify
- Framer Motion
- React Icons
- React DatePicker
- React Image Gallery

### Backend
- Node.js
- Express.js
- MongoDB with Mongoose
- JWT Authentication
- Google Gemini AI API
- Multer for file uploads
- Bcrypt for password hashing
- Helmet for security
- Express Rate Limit

## Prerequisites

- Node.js (v16 or higher)
- MongoDB (local or cloud)
- Google Gemini API key

## Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd ai-trip-planner
   ```

2. **Install dependencies**
   ```bash
   npm run install-all
   ```

3. **Set up environment variables**
   
   Create a `.env` file in the `server` directory:
   ```env
   PORT=5000
   MONGODB_URI=mongodb://localhost:27017/ai-trip-planner
   JWT_SECRET=your-super-secret-jwt-key-change-this-in-production
   GEMINI_API_KEY=your-gemini-api-key-here
   NODE_ENV=development
   ```

4. **Start MongoDB**
   - Make sure MongoDB is running on your system
   - Or use MongoDB Atlas for cloud database

5. **Get Google Gemini API Key**
   - Visit [Google AI Studio](https://makersuite.google.com/app/apikey)
   - Create a new API key
   - Add it to your `.env` file

## Running the Application

### Development Mode
```bash
npm run dev
```

This will start both the backend server (port 5000) and frontend development server (port 3000).

### Production Mode
```bash
# Build the frontend
npm run build

# Start the backend server
npm run server
```

## Project Structure

```
ai-trip-planner/
├── client/                 # React frontend
│   ├── public/
│   ├── src/
│   │   ├── components/    # Reusable components
│   │   ├── contexts/      # React contexts
│   │   ├── pages/         # Page components
│   │   └── index.js
│   └── package.json
├── server/                 # Node.js backend
│   ├── config/            # Database configuration
│   ├── middleware/        # Express middleware
│   ├── models/            # Mongoose models
│   ├── routes/            # API routes
│   ├── services/          # Business logic
│   ├── index.js
│   └── package.json
├── package.json           # Root package.json
└── README.md
```

## API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - Login user
- `GET /api/auth/me` - Get current user
- `PUT /api/auth/preferences` - Update user preferences

### Trips
- `GET /api/trips` - Get user's trips
- `POST /api/trips` - Create new trip
- `GET /api/trips/:id` - Get specific trip
- `PUT /api/trips/:id` - Update trip
- `DELETE /api/trips/:id` - Delete trip
- `POST /api/trips/:id/itinerary` - Generate itinerary
- `POST /api/trips/:id/itinerary/:day/activities` - Add activity

### Destinations
- `GET /api/destinations` - Get destinations
- `GET /api/destinations/:id` - Get specific destination
- `GET /api/destinations/:id/insights` - Get destination insights
- `GET /api/destinations/search/location` - Search by location

## Features in Detail

### AI-Powered Trip Planning
- Uses Google Gemini AI to generate personalized recommendations
- Creates detailed itineraries based on user preferences
- Provides destination insights and travel tips

### User Management
- Secure authentication with JWT tokens
- User preferences for personalized recommendations
- Profile management with travel preferences

### Trip Management
- Create and manage multiple trips
- Detailed itinerary planning
- Budget tracking
- Activity management

### Photo Gallery
- Browse travel photos by category
- Search and filter functionality
- High-quality images for inspiration

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

If you encounter any issues or have questions, please open an issue on GitHub.

## Roadmap

- [ ] Mobile app (React Native)
- [ ] Real-time collaboration
- [ ] Social features (sharing trips)
- [ ] Advanced AI features
- [ ] Offline support
- [ ] Multi-language support

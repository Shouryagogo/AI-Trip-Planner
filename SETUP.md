# AI Trip Planner - Setup Instructions

## Quick Start

1. **Install Dependencies**
   ```bash
   npm run install-all
   ```

2. **Set up Environment Variables**
   - Copy `server/env-example.txt` to `server/.env`
   - Add your Gemini API key to the `.env` file
   - Get your API key from: https://makersuite.google.com/app/apikey

3. **Start MongoDB**
   - Install MongoDB locally or use MongoDB Atlas
   - Make sure MongoDB is running on port 27017

4. **Run the Application**
   ```bash
   npm run dev
   ```

5. **Access the Application**
   - Frontend: http://localhost:3000
   - Backend: http://localhost:5000

## Environment Variables

Create a `.env` file in the `server` directory with the following variables:

```env
PORT=5000
MONGODB_URI=mongodb://localhost:27017/ai-trip-planner
JWT_SECRET=your-super-secret-jwt-key-change-this-in-production
GEMINI_API_KEY=your-gemini-api-key-here
NODE_ENV=development
```

## Getting a Gemini API Key

1. Visit [Google AI Studio](https://makersuite.google.com/app/apikey)
2. Sign in with your Google account
3. Click "Create API Key"
4. Copy the generated key
5. Add it to your `.env` file

## Database Setup

### Option 1: Local MongoDB
1. Install MongoDB Community Edition
2. Start MongoDB service
3. The app will automatically create the database

### Option 2: MongoDB Atlas (Cloud)
1. Create a free account at [MongoDB Atlas](https://www.mongodb.com/atlas)
2. Create a new cluster
3. Get your connection string
4. Replace `MONGODB_URI` in your `.env` file

## Sample Data

To populate the database with sample data:

```bash
cd server
node seed.js
```

This will create:
- Sample users
- Sample destinations (Paris, Tokyo)
- Sample trips

## Features

### ✅ Implemented Features
- User authentication (register/login)
- Trip planning with AI recommendations
- Interactive photo gallery
- Destination browsing
- User profile management
- Responsive design
- Database integration

### 🤖 AI Features
- Gemini API integration for travel recommendations
- Smart itinerary generation
- Personalized suggestions based on user preferences
- Destination insights and tips

### 📱 User Interface
- Modern React frontend
- Responsive design
- Interactive components
- Toast notifications
- Form validation
- Loading states

## Troubleshooting

### Common Issues

1. **MongoDB Connection Error**
   - Make sure MongoDB is running
   - Check your connection string
   - Verify MongoDB is accessible

2. **Gemini API Error**
   - Verify your API key is correct
   - Check if you have API access enabled
   - Ensure you have sufficient quota

3. **Port Already in Use**
   - Change the PORT in your `.env` file
   - Kill any processes using ports 3000 or 5000

4. **Dependencies Issues**
   - Delete `node_modules` folders
   - Run `npm run install-all` again

## Development

### Project Structure
```
ai-trip-planner/
├── client/          # React frontend
├── server/           # Node.js backend
├── package.json      # Root dependencies
└── README.md
```

### Available Scripts
- `npm run dev` - Start both frontend and backend
- `npm run server` - Start only backend
- `npm run client` - Start only frontend
- `npm run build` - Build for production
- `npm run install-all` - Install all dependencies

## Production Deployment

1. **Build the frontend**
   ```bash
   npm run build
   ```

2. **Set production environment variables**
   ```env
   NODE_ENV=production
   MONGODB_URI=your-production-mongodb-uri
   JWT_SECRET=your-production-jwt-secret
   GEMINI_API_KEY=your-production-gemini-key
   ```

3. **Deploy to your hosting platform**
   - Heroku
   - Vercel
   - AWS
   - DigitalOcean

## Support

If you encounter any issues:
1. Check the console for error messages
2. Verify all environment variables are set
3. Ensure MongoDB is running
4. Check your Gemini API key

## License

MIT License - feel free to use this project for learning and development!

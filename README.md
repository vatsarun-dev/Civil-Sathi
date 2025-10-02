# Civil-Sathi

🌱 Civil Sathi - Environmental Cleaning Platform
"Cleaning with Earning"

Civil Sathi is an innovative environmental platform that gamifies environmental cleaning activities. Users can record videos of their environmental actions, earn credits, and redeem them for rewards.

🚀 Quick Start Guide
Prerequisites
Node.js (v16 or higher)
Python 3.x (for frontend server)
Modern web browser with camera access
Installation & Setup
Clone the repository

git clone <your-repo-url>
cd civil-sathi
Install dependencies

npm install
Start the servers

Option 1: Quick Start (Recommended)

# Terminal 1 - Backend Server
npm run dev

# Terminal 2 - Frontend Server  
python -m http.server 8080
Option 2: Manual Start

# Terminal 1 - Backend Server
npm start

# Terminal 2 - Frontend Server
python -m http.server 8080
Access the application

Open your browser and go to: http://localhost:8080
Backend API: http://localhost:5000
🎥 Features
Video Recording System
Selfie Clean: Record environmental cleanup actions
Daily Tasks: Video recording for various environmental challenges
Credit System: Earn credits for each video submission
Video Storage: All videos stored securely on server
Environmental Challenges
♻️ Recycle Challenge: 50 credits
🌱 Plant a Tree: 100 credits
🧹 Community Cleanup: 75 credits
⚡ Energy Saving: 30 credits
📸 Selfie Clean: 10 credits
User Management
User registration and authentication
JWT-based secure sessions
User profiles and statistics
Credit tracking and rewards
🛠️ Development
Project Structure
civil-sathi/
├── routes/           # API endpoints
├── middleware/       # Authentication middleware
├── models/          # Data models
├── utils/           # Utility functions
├── uploads/         # File storage
│   ├── photos/      # Photo uploads
│   └── videos/      # Video uploads
├── data/            # JSON database
├── scripts/         # Setup scripts
└── public/          # Frontend files
API Endpoints
POST /api/auth/register - User registration
POST /api/auth/login - User login
POST /api/videos/upload - Video upload
GET /api/videos/user - User's videos
GET /api/health - Health check
Environment Variables
Create a .env file:

JWT_SECRET=your-secret-key
JWT_EXPIRE=7d
PORT=5000
NODE_ENV=development
🎯 Usage Instructions
For Users
Register/Login: Create an account or login
Record Videos:
Go to "Selfie Clean" section
Click "Start Camera" to begin recording
Perform your environmental action
Click "Stop Recording" when done
Submit the video to earn credits
Complete Tasks: Use the "Daily Tasks" section for more challenges
Redeem Rewards: Use your credits in the "Rewards" section
For Developers
Backend Development:
Server runs on port 5000
Uses nodemon for auto-restart
File-based JSON database
Frontend Development:
Served on port 8080
Uses vanilla JavaScript
Camera API for video recording
🔧 Troubleshooting
Common Issues
Port 5000 already in use:

# Find and kill the process
netstat -ano | findstr :5000
taskkill /PID <process-id> /F
Camera not working:

Ensure browser has camera permissions
Use HTTPS in production
Check browser console for errors
Video upload fails:

Check server logs
Verify file size (max 100MB)
Ensure user is authenticated
Server Management
Start servers:

# Backend (Terminal 1)
npm run dev

# Frontend (Terminal 2)  
python -m http.server 8080
Stop servers:

Press Ctrl+C in each terminal
Or kill processes manually
Reset database:

# Clear all data
rm -rf data/*.json
npm run init-data
📱 Browser Compatibility
Chrome 60+
Firefox 55+
Safari 11+
Edge 79+
Required Features:

Camera API support
MediaRecorder API
ES6+ JavaScript support
🔒 Security Features
JWT-based authentication
Password hashing with bcrypt
File upload validation
CORS protection
Rate limiting
Input validation
📊 Database
The application uses a file-based JSON database:

data/users.json - User accounts
data/videos.json - Video records
data/tasks.json - Task data
data/transactions.json - Transaction history
🎨 Customization
Logo
The logo is displayed in the navigation bar. To update:

Replace the logo in the HTML
Update the CSS styling
Ensure proper sizing and alignment
Styling
Main styles: styles.css
Responsive design included
Custom color scheme
Modern UI components
📈 Performance
File-based storage for simplicity
Efficient video compression
Optimized image handling
Minimal dependencies
🚀 Deployment
Production Setup
Set NODE_ENV=production
Use a proper database (MongoDB/PostgreSQL)
Set up HTTPS
Configure proper file storage
Set up monitoring and logging
Docker (Optional)
FROM node:16
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 5000
CMD ["npm", "start"]
🤝 Contributing
Fork the repository
Create a feature branch
Make your changes
Test thoroughly
Submit a pull request
📄 License
MIT License - see LICENSE file for details

🆘 Support
For issues and questions:

Check the troubleshooting section
Review server logs
Check browser console
Create an issue on GitHub
Civil Sathi - Making environmental action rewarding! 🌱✨
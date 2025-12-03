# 🖥️ PCease - PC Builder & Community Platform

> Your all-in-one solution for building the perfect PC. Browse components, get expert recommendations, and connect with the community.

🚀 **[Live Demo](https://pcease.vercel.app/)** | 💻 **[GitHub Repository](https://github.com/vaibhavshiroorkar/pc-builder)**

---

## ✨ Features

### 🔍 **Browse Components**
Explore a comprehensive database of PC components including CPUs, GPUs, motherboards, RAM, storage, and more. Filter by brand, specs, and price to find exactly what you need.

### 🛠️ **PC Builder**
- **Drag-and-drop interface** for easy build creation
- **Compatibility checking** to ensure all parts work together
- **Price tracking** across multiple vendors
- **Save & share** your builds with base64 encoded URLs
- **Load saved builds** and modify them anytime

### 🤖 **Build Advisor**
Get AI-powered recommendations based on your use case:
- Gaming builds (1080p, 1440p, 4K)
- Workstation setups for content creation
- Budget-friendly options
- High-performance configurations

### 💬 **Community Forum**
- Create discussion threads
- Share build ideas and get feedback
- Ask questions and help others
- Category-based organization

### 🎨 **Theme Toggle**
Switch between light and dark modes for comfortable browsing at any time.

### 🔐 **User Authentication**
Secure login and registration system with JWT tokens to save your builds and forum activity.

---

## 🚀 Tech Stack

### **Frontend**
- ⚛️ **React 18** - Modern UI library
- ⚡ **Vite** - Lightning-fast build tool
- 🎨 **Custom CSS** - Responsive design with theme support
- 🛣️ **React Router** - Client-side routing

### **Backend**
- 🟢 **Express.js** - RESTful API server
- 🍃 **MongoDB** - NoSQL database for components and user data
- 🔒 **JWT** - Secure authentication
- 🌐 **CORS** - Cross-origin resource sharing

### **Deployment**
- ☁️ **Vercel** - Serverless functions and static hosting
- 🗄️ **MongoDB Atlas** - Cloud database
- 🔄 **CI/CD** - Automatic deployments from GitHub

---

## 🛠️ Getting Started

### Prerequisites
- Node.js 18+ and npm
- MongoDB (local or Atlas account)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/vaibhavshiroorkar/pc-builder.git
   cd pc-builder
   ```

2. **Install frontend dependencies**
   ```bash
   npm install
   ```

3. **Install backend dependencies**
   ```bash
   cd backend
   npm install
   ```

4. **Set up environment variables**
   
   Create `backend/.env`:
   ```env
   MONGO_URI=your_mongodb_connection_string
   JWT_SECRET=your_secure_jwt_secret
   PORT=5000
   FRONTEND_URL=http://localhost:5173
   ```

5. **Seed the database (optional)**
   ```bash
   npm --prefix backend run seed
   ```

6. **Run development servers**
   
   Terminal 1 - Backend:
   ```bash
   cd backend
   npm start
   ```
   
   Terminal 2 - Frontend:
   ```bash
   npm run dev
   ```

7. **Open your browser**
   - Frontend: [http://localhost:5173](http://localhost:5173)
   - API: [http://localhost:5000](http://localhost:5000)

---

## 📁 Project Structure

```
pc-builder/
├── src/
│   ├── components/      # Reusable UI components
│   ├── pages/          # Route pages (Home, Browse, Builder, etc.)
│   ├── lib/            # Utilities (auth, theme)
│   ├── shared/         # Shared logic (API client)
│   └── styles/         # Page-specific CSS
├── backend/
│   ├── app.js          # Express server setup
│   ├── scripts/        # Database seeding scripts
│   └── .env            # Environment variables (not in git)
├── api/
│   └── index.js        # Vercel serverless function
└── dist/               # Production build (generated)
```

---

## 🌐 API Endpoints

### **Authentication**
- `POST /api/register` - Create new user account
- `POST /api/login` - Login and receive JWT token

### **Components**
- `GET /api/components` - List all components
- `GET /api/components?category=cpu` - Filter by category
- `POST /api/components` - Add new component (admin)

### **Forum**
- `GET /api/threads` - List all threads
- `POST /api/threads` - Create new thread (auth required)
- `GET /api/threads/:id` - Get thread with replies
- `POST /api/threads/:id/replies` - Add reply (auth required)
- `DELETE /api/threads/:id` - Delete thread (auth required)

### **Saved Builds**
- `GET /api/saved-builds` - Get user's saved builds (auth required)
- `POST /api/saved-builds` - Save a new build (auth required)
- `PUT /api/saved-builds/:id` - Update build (auth required)
- `DELETE /api/saved-builds/:id` - Delete build (auth required)

---

## 🚀 Deployment

The app is deployed on Vercel with the following configuration:

1. **Push to GitHub** - Automatic deployment triggers
2. **Environment Variables** - Set in Vercel Dashboard:
   - `MONGO_URI`
   - `JWT_SECRET`
   - `FRONTEND_URL`
3. **Build Settings**:
   - Build Command: `node node_modules/vite/bin/vite.js build`
   - Output Directory: `dist`

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

---

## 👨‍💻 Author

**Vaibhav Shiroorkar**
- GitHub: [@vaibhavshiroorkar](https://github.com/vaibhavshiroorkar)
- Project: [PCease](https://pcease.vercel.app)

---

## 🙏 Acknowledgments

- Component data sourced from various retailers
- Built with modern web technologies and best practices
- Deployed on Vercel's amazing platform

---

<div align="center">
  <strong>⭐ Star this repo if you found it helpful! ⭐</strong>
</div>

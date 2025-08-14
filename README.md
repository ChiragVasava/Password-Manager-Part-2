# 🔐 Password Manager Part 2 - Full Stack Application

This is a secure and responsive **Full Stack Password Manager** application built using **React 19**, **Vite**, **TailwindCSS v4**, **Node.js**, **Express.js**, **MongoDB**, and **React Toastify** with animated **Lordsicon** icons. This is the advanced version with backend database storage and RESTful API.

---

## 📦 Project Setup

### 1️⃣ Clone this repository

```bash
git clone https://github.com/ChiragVasava/Password-Manager-Part-2.git
```
```bash
cd Password-Manager-Part-2
```

### 2️⃣ Frontend Setup (React + Vite)

#### Navigate to root directory for frontend
```bash
# Already in root directory for frontend files
```

#### Install Frontend Dependencies
```bash 
npm install
```

#### Run Frontend Development Server
```bash
npm run dev
```

#### Build Frontend for Production
```bash
npm run build
```

#### Preview Production Build
```bash
npm run preview
```

### 3️⃣ Backend Setup (Node.js + Express + MongoDB)

#### Navigate to Backend directory
```bash
cd Backend
```

#### Install Backend Dependencies
```bash
npm install
```

#### Additional Required Backend Packages
```bash
npm install express mongodb cors dotenv body-parser
```

#### Create .env file in Backend directory:
```env
MONGO_URI=mongodb://localhost:27017
```

#### Start Backend Server
```bash
node server.js
```

### 4️⃣ MongoDB Setup

#### Install MongoDB Community Edition
- Download and install MongoDB from [https://www.mongodb.com/try/download/community](https://www.mongodb.com/try/download/community)
- Start MongoDB service:

##### Windows:
```bash
net start MongoDB
```

##### macOS:
```bash
brew services start mongodb/brew/mongodb-community
```

##### Linux:
```bash
sudo systemctl start mongod
```

#### Verify MongoDB Connection
```bash
mongosh
# Should connect to mongodb://localhost:27017
```

### 5️⃣ Frontend Package Installation

#### 1. Install UUID Package
```bash
npm install uuid
```

#### 2. Install React Toastify
```bash
npm install react-toastify
```

#### 3. Install TailwindCSS v4
```bash
npm install -D @tailwindcss/vite autoprefixer
```

#### 4. UUID Usage Example
```javascript
import { v4 as uuidv4 } from 'uuid';
const uniqueId = uuidv4(); // ⇨ '9b1deb4d-3b7d-4bad-9bdd-2b0d7b3dcb6d'
```

#### 5. React Toastify Usage
```javascript
import { toast, ToastContainer } from 'react-toastify';
import 'react-toastify/dist/ReactToastify.css';

// Success notification
toast.success("Password saved successfully!");

// Error notification  
toast.error("Failed to save password!");
```

### 6️⃣ TailwindCSS v4 Setup

#### 1. Create postcss.config.js:
```javascript
// postcss.config.js
import tailwindcss from '@tailwindcss/postcss';
import autoprefixer from 'autoprefixer';

export default {
  plugins: [tailwindcss(), autoprefixer()],
}
```

#### 2. Update src/index.css:
```css
/* src/index.css */
@import "tailwindcss";
@import 'react-toastify/dist/ReactToastify.css';
```

#### 3. Import in main.jsx:
```javascript
import './index.css';
```

### 7️⃣ Lordsicon Setup
#### Add Lordsicon to index.html:
```html
<script src="https://cdn.lordicon.com/lordicon.js"></script>
```

#### Usage Example:
```jsx
<lord-icon
    src="https://cdn.lordicon.com/example-icon.json"
    trigger="hover"
    colors="primary:#121331,secondary:#08a88a"
    style={{width: '50px', height: '50px'}}>
</lord-icon>
```

### ⚙️ Tech Stack

| Technology     | Version         | Purpose                    |
| -------------- | --------------- | -------------------------- |
| **Frontend**   |                 |                            |
| React          | ^19.1.1         | Frontend Framework         |
| Vite           | ^7.1.0          | Build Tool & Dev Server    |
| TailwindCSS    | ^4.1.11         | CSS Framework              |
| React Toastify | ^11.0.5         | Notification System        |
| UUID           | ^11.1.0         | Unique ID Generation       |
| LordsIcon      | Latest          | Animated Icons             |
| **Backend**    |                 |                            |
| Node.js        | Latest          | Backend Runtime            |
| Express        | ^5.1.0          | Backend Framework          |
| MongoDB        | ^6.18.0         | Database Driver            |
| CORS           | ^2.8.5          | Cross-Origin Requests      |
| Dotenv         | ^17.2.1         | Environment Variables      |
| Body-Parser    | ^2.2.0          | Request Body Parsing       |
| **Tools**      |                 |                            |
| Postman        | Latest          | API Testing                |
| MongoDB        | Latest          | Database                   |

### 🚀 Project Features

- **Full Stack Architecture** - Complete frontend and backend separation
- **MongoDB Integration** - Persistent database storage
- **RESTful API** - Well-structured API endpoints
- **Password Encryption** - Secure password storage
- **User Authentication** - Login/Register functionality
- **Password Generation** - Generate strong, random passwords
- **Search & Filter** - Find passwords quickly by website or service
- **Copy to Clipboard** - One-click password and username copying
- **Show/Hide Passwords** - Toggle password visibility
- **Animated UI** - Beautiful LordsIcon animations
- **Toast Notifications** - Real-time feedback with React Toastify
- **Responsive Design** - Works on desktop, tablet, and mobile
- **Modern Background** - Stylish TailwindCSS backgrounds from bg.ibelick.com
- **UUID-based IDs** - Unique identifiers for all entries
- **CRUD Operations** - Create, Read, Update, Delete passwords
- **API Testing** - Comprehensive Postman collection included

### 💡 Folder Structure

```
Password-Manager-Part-2/
│
├── Backend/
│   ├── node_modules/
│   ├── .env
│   ├── package-lock.json
│   ├── package.json
│   └── server.js
│
├── node_modules/
├── public/
│   ├── icons/
│   │   ├── eye.png
│   │   ├── eyecross.png
│   │   ├── github.svg
│   │   ├── heart.png
│   │   ├── favicon.png
│   │   └── vite.svg
│
├── src/
│   ├── assets/
│   │   └── react.svg
│   │
│   ├── components/
│   │   ├── Footer.jsx
│   │   ├── Manager.jsx
│   │   └── Navbar.jsx
│   │
│   ├── App.css
│   ├── App.jsx
│   ├── index.css
│   └── main.jsx
│
├── .gitignore
├── eslint.config.js
├── index.html
├── package-lock.json
├── package.json
├── README.md
└── vite.config.js
```

### 📋 Backend Package Installation Steps

#### 1. Initialize Backend Project
```bash
cd Backend
npm init -y
```

#### 2. Install Core Dependencies
```bash
npm install express mongodb cors dotenv body-parser
```

#### 3. Package Details:
- **express**: Web framework for Node.js
- **mongodb**: MongoDB database driver
- **cors**: Enable Cross-Origin Resource Sharing
- **dotenv**: Load environment variables from .env file
- **body-parser**: Parse incoming request bodies

### 🔧 Environment Configuration

#### Frontend (.env) - Create in root directory:
```env
VITE_API_URL=http://localhost:3000/api
```

#### Backend (.env) - Create in Backend directory:
```env
MONGO_URI=mongodb://localhost:27017
PORT=3000
DB_NAME=password_manager
```

### 📱 Usage Instructions

1. **Start Backend Server**:
   ```bash
   cd Backend
   node server.js
   ```

2. **Start Frontend Development Server**:
   ```bash
   npm run dev
   ```

3. **Access Application**: Open `http://localhost:5173` in your browser

4. **API Testing**: Import Postman collection to test API endpoints

5. **Database**: View data in MongoDB using MongoDB Compass or CLI

### 🧪 Testing with Postman

#### Import Collection:
1. Create Postman collection for all API endpoints
2. Test GET, POST, PUT, DELETE requests
3. Verify response structures
4. Test error handling

#### Sample API Requests:

##### Get All Passwords:
```
GET http://localhost:3000/api/passwords
```

##### Create New Password:
```
POST http://localhost:3000/api/passwords
Content-Type: application/json

{
  "website": "example.com",
  "username": "user@example.com",
  "password": "securePassword123"
}
```

### 🔒 Security Features

- **Environment Variables** - Sensitive data in .env files
- **CORS Configuration** - Controlled cross-origin requests
- **Input Validation** - Frontend and backend validation
- **Password Encryption** - Secure password storage
- **Error Handling** - Proper error responses

### 🎨 Design Features

- **Custom Backgrounds** - Unique TailwindCSS backgrounds from bg.ibelick.com
- **Animated Icons** - Beautiful LordsIcon animations
- **Toast Notifications** - Real-time user feedback
- **Responsive Layout** - Mobile-first design approach
- **Modern UI/UX** - Clean and intuitive interface

### 🚀 Deployment
#### Frontend Deployment:
```bash
npm run build
# Deploy dist/ folder to Vercel, Netlify, or any static hosting
```

#### Backend Deployment:
```bash
# Deploy to Railway, Render, Heroku, or any Node.js hosting
# Update MONGO_URI to cloud MongoDB (MongoDB Atlas)
```

#### MongoDB Atlas Setup:
1. Create account at [MongoDB Atlas](https://www.mongodb.com/cloud/atlas)
2. Create cluster and get connection string
3. Update MONGO_URI in .env file

### 🛠️ Development Scripts

#### Frontend:
```bash
npm run dev      # Start development server
npm run build    # Build for production
npm run preview  # Preview production build
npm run lint     # Run ESLint
```

#### Backend:
```bash
npm start        # Start server
npm run dev      # Start with nodemon (auto-restart)
```

### 🙌 Author

Made with 💻 and ❤️ by [Chirag Vasava](https://github.com/ChiragVasava)

### 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### 📄 License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

### 📞 Support

If you have any questions or need help, please open an issue or contact me at v.chirag.007@gmail.com

### 🌟 Live Demo

https://github.com/user-attachments/assets/71972b86-a015-4415-ab93-11fd44317440

---

### 📸 Screenshots

<img width="1920" height="906" alt="PassOp-Mongodb" src="https://github.com/user-attachments/assets/868b530a-cadc-4768-8eec-d35d27686080" />

---

<img width="1919" height="1020" alt="PassOp-Mongodb2" src="https://github.com/user-attachments/assets/9cb8651f-3189-4d6d-9e69-ecfa645fb235" />

### 🔄 Version History

- **v1.0.0** - Initial release with full stack implementation
- **Part 1** - Frontend-only version with localStorage
- **Part 2** - Full stack version with MongoDB backend

⭐ **Don't forget to star this repository if you found it helpful!** ⭐
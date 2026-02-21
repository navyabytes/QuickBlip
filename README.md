# QuickBlip 

A modern, Firebase-powered note-taking app designed for speed, simplicity and security.

---

## ✨ Features

- 🔐 **Secure Authentication** - Sign up and sign in with email/password
- ✍️ **Rich Text Editor** - WYSIWYG-style editing with formatting options
- 📊 **Smart Dashboard** - View, organize and manage all your notes in one place
- ☁️ **Cloud Sync** - Real-time synchronization with Firebase Firestore
- 📱 **Responsive Design** - Works perfectly on desktop and mobile
- ⚡ **Lightning Fast** - Optimized for speed and performance
- 🎨 **Clean Interface** - Distraction-free writing experience

---
## 🏗️ Architecture


```
Frontend: Vanilla JavaScript, HTML5, CSS3
Backend: Firebase Authentication & Firestore
Security: Custom Firestore rules
Deployment: Firebase Hosting ready
```

### Project Structure

```
QuickBlip/
├── 🏠 Core Pages
│   ├── index.html              # Landing page
│   ├── dashboard.html          # Notes dashboard
│   └── editor.html             # Note editor
│
├── 🔐 Authentication
│   ├── login.html              # Login interface
│   ├── signup.html             # Registration interface
│   ├── signin.js               # Login logic
│   └── register.js             # Registration logic
│
├── 📊 Dashboard Module
│   ├── dashboard.css           # Dashboard styling
│   ├── dashboard-ui.js         # UI interactions
│   └── dashboard-db.js         # Database operations
│
├── ✍️ Editor Module
│   ├── editor.css              # Editor styling
│   ├── editor-ui.js            # Editor interface
│   └── editor-db.js            # Note persistence
│
├── 🔧 Configuration
│   ├── firebase-config.js      # Firebase setup
│   ├── firestore.rules         # Security rules
│   └── styles.css              # Global styles
│
└── 🎨 Assets
    ├── logo-light.png          # Light theme logo
    └── logo-dark.png           # Dark theme logo
```

---

## 🔒 Security & Privacy

QuickBlip implements robust security measures:

### Firestore Security Rules
```javascript
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /notes/{noteId} {
      allow read, write: if request.auth != null && 
                          request.auth.uid == resource.data.userId;
    }
  }
}
```

**What this means:**
- Only authenticated users can access notes
- Users can only see and edit their own notes
- All data is encrypted in transit and at rest
  
---

## 👨‍💻 Author

**Saarthak Sabharwal**  
GitHub: [Saaarthak0102](https://github.com/Saaarthak0102)

---

# 🎉 itidoc - Online Cloud Storage System

Your itidoc app now has **complete cloud storage integration**! Work on your project from **any PC** with automatic file syncing.

## ✨ Features

✅ **Upload files** to Firebase Cloud Storage  
✅ **Download files** from anywhere  
✅ **List all files** stored online  
✅ **Delete files** from cloud  
✅ **Access from any PC** - No downloads needed  
✅ **Auto file metadata** tracking  
✅ **Support up to 100MB** per file  

## 🚀 Quick Start

### 1. Install Dependencies
```bash
npm install
```

### 2. Setup Firebase

1. Go to [Firebase Console](https://console.firebase.google.com/)
2. Create a new project
3. Enable **Cloud Storage** and **Firestore**
4. Create a service account:
   - Go to **Project Settings** → **Service Accounts**
   - Click **Generate New Private Key**
   - Save the JSON file

### 3. Configure Environment

Copy `.env.example` to `.env`:
```bash
cp .env.example .env
```

Add your Firebase credentials to `.env`:
```
FIREBASE_PROJECT_ID=your_project_id
FIREBASE_PRIVATE_KEY=your_private_key
FIREBASE_CLIENT_EMAIL=your_service_account_email
FIREBASE_STORAGE_BUCKET=your_storage_bucket
PORT=5000
```

### 4. Start Server
```bash
npm start
```

Server runs on **http://localhost:5000**

## 📡 API Usage

### Upload a File
```bash
curl -X POST -F "file=@myfile.txt" http://localhost:5000/api/storage/upload
```

### List All Files
```bash
curl http://localhost:5000/api/storage/list
```

### Download a File
```bash
curl http://localhost:5000/api/storage/download/fileName > myfile.txt
```

### Delete a File
```bash
curl -X DELETE http://localhost:5000/api/storage/delete/fileName
```

## 📁 Project Structure

```
├── config/
│   └── firebase.js              # Firebase setup
├── middleware/
│   └── upload.js                # File upload handler
├── routes/
│   └── storage.js               # Storage API routes
├── server.js                    # Express server
├── package.json                 # Dependencies
├── .env.example                 # Config template
├── .gitignore                   # Git ignore
└── README.md                    # This file
```

## 🔑 Next Steps

1. Extract your app files from the zip
2. Integrate with your frontend
3. Use the API endpoints to manage files
4. Continue work seamlessly from any PC!

---

**Now you have full cloud storage! Work from anywhere! 🌐✨**
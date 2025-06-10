
---

````markdown
# 📸 Wedding Moments – Capturing Real-Time Memories

**Wedding Moments** is a lightweight, user-friendly web app designed to collect photos from guests during a special event – the wedding day. With a modern and welcoming interface, it allows every guest to upload photos directly from their phone, without needing to install anything.

## 🎯 Purpose

To provide the bride, groom, and their guests with a fast and secure platform to save precious memories in real-time, as the event unfolds.

## 🔧 Key Features

- 📤 Instant photo upload — no account or app required  
- 🧠 Automatic unique ID generation per user  
- 🧾 Each guest gets a personalized dynamic album  
- 📁 Admin panel with authentication and per-user ZIP archive download  
- 🎨 Responsive design with customizable themes (beige-green, lavender, etc.)  
- ⚡ Load-tested for 70+ simultaneous users  
- 🔐 Fully self-hosted — no external storage required  

## 🛠️ Tech Stack

- **Node.js + Express** — backend and upload logic  
- **HTML/CSS/JS** — simple and responsive frontend  
- **Multer** — for file upload handling  
- **Archiver** — for ZIP album downloads  
- **PM2** — for continuous server operation  
- **K6** — for load and stress testing  

## 🚀 Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/wedding-moments.git
cd wedding-moments
````

### 2. Install Dependencies

```bash
npm install
```

### 3. Create Required Folders and Files

```bash
mkdir uploads
touch admin.json
```

**admin.json**

```json
{
  "admin": "your_password_here"
}
```

### 4. Start the App

```bash
pm2 start server.js --name wedding-app
```

Or, for development:

```bash
node server.js
```

The app runs by default on `http://localhost` or your server's LAN IP on port `80`.

## 🧪 Load Testing (Optional)

If you want to simulate multiple users, use [k6](https://k6.io/):

```bash
k6 run test_script.js
```

## 📝 License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

```



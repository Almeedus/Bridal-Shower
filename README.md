# 💍 Bridal Shower Invitation

A modern and easily shareable web-based invitation for a bridal shower.  
This project replaces traditional invitations with a simple, interactive web experience where guests can view event details and select gifts.

---

## 🚀 Live Demo

> ...


---

## ✨ Features

### 📄 Main Page (Invitation)
- Navigation header with:
  - Home
  - Gift List
  - WhatsApp Group
- Invitation designed in Canva following the bride’s color palette
- Quick access buttons:
  - Join WhatsApp group
  - View gift list
- Image carousel of the couple

### 🎁 Gift List Page
- Displays a list of suggested gifts
- Interactive selection system:
  - Confirmation before selecting an item
  - Selected items become unavailable for others
  - Visual feedback (items turn gray when selected)

---

## 🛠️ Tech Stack

- **Vue.js**
- **JavaScript (ES6+)**
- **HTML5 & CSS3**

---

## 📦 Installation & Setup

Make sure you have **Node.js** installed.

```bash
# Clone the repository
git clone https://github.com/Almeedus/Bridal-Shower.git

# Navigate into the project
cd bridal-shower

# Install dependencies
npm install

# Run development server
npm run dev
```

---

## 🔌 API Integration

This frontend consumes an external API for managing the gift list.

### Endpoints used:

```bash
GET /items        -> Fetch all items  
PATCH /items/:id  -> Update item status  
```
⚠️ The API is external, built with Python, and connected to a SQL database.

---

### 📁 Project Structure

```bash
```

---

## 👤 Author
### Eduardo Almeida
📧 almeedusa@gmail.com

--- 

## 📄 License
This project is for personal use (bridal shower event).

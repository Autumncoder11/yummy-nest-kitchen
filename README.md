# 🍽️ Yummy Nest Kitchen

> **From Our Nest to Your Plate** 🍃

A beautiful, mobile-first digital menu page for **Yummy Nest Kitchen** — a home-style food delivery service in Coimbatore, India. Built with HTML, Tailwind CSS, and Firebase.

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 📅 **Live Date & Day** | Automatically displays current date with ordinal suffix (e.g., 24th June 2026) |
| ⏰ **Order Deadline Countdown** | Real-time countdown showing how much time is left to order each meal |
| 🔍 **Smart Search** | Instantly search dishes by name |
| 🌿 **Diet Filters** | Filter by Veg, Non-Veg, or Best Sellers |
| ❤️ **Like & Vote** | Customers can like dishes — votes are saved permanently via Firebase |
| 📊 **Download Menu** | One-click download of full Excel menu |
| 📲 **Share Menu** | Share full menu or individual dishes via WhatsApp |
| 📞 **Quick Contact** | Direct Call & WhatsApp buttons |
| 🎨 **Responsive Design** | Optimized for mobile, tablet, and desktop |

---

## 🕐 Order Windows

| Meal | Serving Time | Order Before |
|------|-------------|--------------|
| 🥞 **Breakfast** | 7:30 AM – 10:30 AM | 8:00 AM |
| 🍛 **Lunch** | 11:30 AM – 3:30 PM | 12:00 PM |
| 🌙 **Dinner** | 7:00 PM – 10:30 PM | 6:30 PM |

> Orders placed after the deadline will be processed for the next available slot.

---

## 🛠️ Tech Stack

- **Frontend:** HTML5, Tailwind CSS (CDN), Custom CSS
- **Backend:** Firebase (Firestore, Authentication, Analytics, Storage)
- **Fonts:** Google Fonts (Playfair Display, Great Vibes, Inter, Playpen Sans)
- **Icons:** SVG + Emoji
- **Hosting:** GitHub Pages (or Firebase Hosting)

---

## 📁 Project Structure

```
Yummy_Nest_Kitchen/
├── index.html          # Main menu page (single-file application)
├── README.md           # This file
└── .gitattributes      # Line ending normalization (optional)
```

> **Note:** This is a single-file application. All CSS, JavaScript, and HTML are contained within `index.html` for simplicity and easy deployment.

---

## 🚀 Getting Started

### Prerequisites
- A modern web browser
- A Firebase project (for live menu data, likes, and analytics)

### Local Development

1. **Clone the repository**
   ```bash
   git clone https://github.com/YOUR_USERNAME/Yummy_Nest_Kitchen.git
   cd Yummy_Nest_Kitchen
   ```

2. **Open in browser**
   ```bash
   # Simply open the file
   start index.html        # Windows
   open index.html         # Mac
   xdg-open index.html     # Linux
   ```

   Or use a local server for full functionality:
   ```bash
   npx serve .
   # or
   python -m http.server 8000
   ```

3. **Firebase Setup** (Optional — for live data)
   - Create a Firebase project at [firebase.google.com](https://firebase.google.com)
   - Enable Firestore, Authentication (Anonymous), and Analytics
   - Update the Firebase config in `index.html` with your credentials
   - Create a `menu_items` collection and `daily_menus/today` document

---

## 📱 Firebase Data Structure

### Collection: `menu_items`
Each document represents a dish:

```json
{
  "name": "Chicken Biryani",
  "price": 180,
  "mealType": "lunch",
  "category": "nonveg",
  "description": "Aromatic basmati rice with tender chicken",
  "image": "https://firebasestorage.googleapis.com/.../biryani.jpg",
  "isEnabled": true,
  "isSpecial": true,
  "likes": 42,
  "prepTime": "15 mins",
  "ingredients": "Basmati rice, chicken, spices, herbs",
  "allergens": "Contains nuts",
  "nutrition": "High protein, 450 kcal per serving"
}
```

### Document: `daily_menus/today`
Controls daily settings:

```json
{
  "delivery_charge": 30,
  "isHoliday": false,
  "holidayMessage": ""
}
```

---

## 🎨 Customization Guide

### Change Order Deadlines
Edit these lines in `index.html`:

```javascript
const breakfastDeadline = 8 * 60;      // 8:00 AM
const lunchDeadline = 12 * 60;         // 12:00 PM
const dinnerDeadline = 18 * 60 + 30;   // 6:30 PM
```

### Change Contact Number
Search for `+919789327773` in `index.html` and replace with your number.

### Change Address
Search for `Flat B, Yummy Nest Arcade, Coimbatore` and update.

### Update Excel Menu Link
Find the download button `<a>` tag and replace the `href` with your new Firebase Storage URL.

---

## 📤 Deployment

### GitHub Pages (Free)
1. Push code to GitHub
2. Go to **Settings → Pages**
3. Source: **Deploy from a branch** → `master` / `main`
4. Your site will be live at `https://YOUR_USERNAME.github.io/Yummy_Nest_Kitchen/`

### Firebase Hosting (Alternative)
```bash
npm install -g firebase-tools
firebase login
firebase init hosting
firebase deploy
```

---

## 📞 Contact

| Method | Details |
|--------|---------|
| 📍 Address | Flat B, Yummy Nest Arcade, Coimbatore |
| 📞 Phone | +91 97893 27773 |
| 🕒 Hours | Daily: 11:30 AM – 10:30 PM |
| 💬 WhatsApp | [Click to Chat](https://wa.me/919789327773) |

---

## 📝 License

This project is proprietary to **Yummy Nest Kitchen**. All rights reserved.

---

<p align="center">
  <sub>Built with ❤️ for Yummy Nest Kitchen</sub>
</p>

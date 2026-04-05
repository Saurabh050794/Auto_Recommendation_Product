# 🛍️ ShopAI — AI Product Recommender

> **Ek standalone HTML file jisme 1000+ Amazon products ki smart recommendations milti hain — bina kisi server ke!**

🔗 **Live Demo:** [Click here to open ShopAI](https://saurabh050794.github.io/Auto_Recommendation_Product/ShopAI.html)

---

## ✨ Features

- 🔍 **Smart Search** — Koi bhi product search karo (shoes, helmet, electronics...)
- 🔥 **Trending** — Sabse zyada reviewed aur popular products
- 📦 **Category Filter** — Sports, Clothing, Shoes, Electronics, Home aur aur bhi
- 💰 **Price Range** — Min aur Max price set karke best value products dhundo
- 🃏 **Product Cards** — Image, price, rating, discount badge sab ek jagah
- 🔮 **Find Similar** — Kisi bhi product se similar products dhundo
- 🌙 **Dark / Light Mode** — Beautiful dark UI (light bhi kar sakte ho)
- 📱 **Mobile Friendly** — Mobile aur laptop dono pe kaam karta hai

---

## 🚀 Use Kaise Karein

### Option 1 — Seedha File Open Karo (No Setup)
```
1. ShopAI.html download karo
2. Double-click karo
3. Browser mein khul jaayega ✅
```

### Option 2 — GitHub Pages Live Link
```
https://YOUR-USERNAME.github.io/shopai/ShopAI.html
```

---

## 📁 Project Structure

```
shopai/
├── ShopAI.html        ← Puri app ek file mein (1000 products embedded)
└── README.md          ← Yeh file
```

> **Koi server nahi, koi backend nahi, koi setup nahi!**
> Sirf ek HTML file — sab kuch andar hai.

---

## 🧠 Kaise Kaam Karta Hai

```
User search karta hai
        ↓
JavaScript tokens banata hai (search query se)
        ↓
1000 products mein match dhundta hai
        ↓
Rating + Reviews ke hisaab se sort karta hai
        ↓
Product cards show hoti hain ✅
```

### Recommendation Logic:
- **Search** — Title, Brand, Category mein keyword match karta hai
- **Trending** — Reviews count ke hisaab se sort
- **Category** — Department/Category filter + Rating sort
- **Price Range** — Min-Max filter + Value score (rating × log reviews)
- **Similar Products** — Common tokens se similarity calculate karta hai

---

## 🎨 UI Change Kaise Karein

### Dark → Light Theme:
`ShopAI.html` Notepad mein kholo aur yeh dhundo:

```css
--bg:#0a0a0f; --surface:#13131a; --surface2:#1c1c27;
--border:#2a2a3a; --accent:#6c63ff; --accent2:#ff6584;
--accent3:#43e97b; --text:#f0f0f8; --muted:#7070a0; --card:#16161f;
```

Isse replace karo:

```css
--bg:#f4f6fb; --surface:#ffffff; --surface2:#eef0f7;
--border:#d5d9e8; --accent:#6c63ff; --accent2:#ff6584;
--accent3:#16a34a; --text:#1a1a2e; --muted:#6b7280; --card:#ffffff;
```

---

## 📊 Dataset Info

| Field | Details |
|-------|---------|
| Total Products | 1,000 |
| Source | Amazon.com |
| Categories | Sports, Clothing, Electronics, Home, Toys aur aur bhi |
| Fields | Title, Brand, Price, Rating, Reviews, Image, URL |

---

## 🛠️ Full Backend Version (Flask)

Agar aap full AI backend bhi chahte ho (TF-IDF + Cosine Similarity), toh yeh files use karo:

```
ai-product-recommender/
├── data/products.csv
├── model/recommender.py    ← TF-IDF + Cosine Similarity
├── app/app.py              ← Flask REST API
├── utils/helper.py
└── requirements.txt
```

### Run karo:
```bash
pip install -r requirements.txt
python app/app.py
# Open: http://localhost:5000
```

### API Endpoints:
| Endpoint | Description |
|----------|-------------|
| `/api/search?q=shoes` | Free-text search |
| `/api/category?name=Sports` | Category filter |
| `/api/price?min=10&max=50` | Price range |
| `/api/hybrid?title=...` | AI hybrid recommendations |
| `/api/stats` | Dataset statistics |

---

## 🌐 Deploy Karo (Free)

### Netlify (Sabse Aasaan):
1. [netlify.com](https://netlify.com) pe jao
2. Sign up karo
3. `ShopAI.html` drag & drop karo
4. Link mil jaayega! ✅

### GitHub Pages:
1. Yeh repo fork karo
2. Settings → Pages → main branch select karo
3. Link: `https://username.github.io/shopai/ShopAI.html` ✅

---

## 📱 Screenshots

| Trending | Search | Category |
|---------|--------|----------|
| 🔥 Top products | 🔍 Keyword search | 📦 Filter by dept |

---

## 📝 License

MIT License — Free to use, modify aur share karo! 😊

---

## 🙋 Contact

Koi problem ho toh **Issues** tab mein batao!

⭐ **Agar pasand aaya toh Star zaroor karo!**

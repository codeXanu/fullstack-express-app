# Spiral Sounds 🎵

Spiral Sounds is a full-stack Express.js vinyl record storefront application. It serves a frontend interface for users to browse vinyl albums, filter by genre or search by keywords, and renders content dynamically from a SQLite database.

## 🗂 Project Structure

```
spiral-sounds/
├── controllers/
│   └── productControllers.js        # Business logic for fetching products and genres
├── db/
│   └── db.js                        # SQLite connection helper
├── public/
│   ├── images/                      # Album cover images
│   ├── index.css                    # Stylesheet for frontend
│   ├── index.html                   # Main UI for storefront
│   └── index.js                     # Frontend JavaScript logic
├── routes/
│   └── products.js                  # Express router for product APIs
├── createTable.js                   # Initializes the 'products' table in the DB
├── data.js                          # Seed data of vinyl albums
├── database.db                      # SQLite database file
├── logTable.js                      # Utility to log current database entries
├── seedTable.js                     # Seeds the DB with vinyl album data
├── server.js                        # Main Express server entry
├── package.json
└── package-lock.json
```

## 🚀 Features

- Browse vinyl album listings with images, title, artist, price, and genre.
- Filter albums by genre using a dropdown.
- Search for albums by title, artist, or genre.
- Fully functional REST API using Express.
- SQLite database integration with dynamic querying.
- Responsive and interactive frontend.

## 🧰 Tech Stack

- **Frontend**: HTML, CSS, JavaScript (Vanilla)
- **Backend**: Node.js, Express.js
- **Database**: SQLite
- **Tools**: `sqlite3`, `express`, `nodemon` (optional for dev)

## 🛠 Setup Instructions

1. **Clone the Repository**

```bash
git clone https://github.com/yourusername/spiral-sounds.git
cd spiral-sounds
```

2. **Install Dependencies**

```bash
npm install
```

3. **Create Database Table**

```bash
node createTable.js
```

4. **Seed the Database**

```bash
node seedTable.js
```

5. **Start the Server**

```bash
npm start
```

6. **View the App**

Open your browser and go to:

```
http://localhost:8000
```

## 🔍 API Endpoints

| Method | Endpoint                | Description                        |
|--------|-------------------------|------------------------------------|
| GET    | `/api/products`         | Returns all products               |
| GET    | `/api/products?search=` | Search products by title/artist    |
| GET    | `/api/products?genre=`  | Filter products by genre           |
| GET    | `/api/products/genres`  | Get a list of all product genres   |

## 📦 Sample Product Schema

```json
{
  "id": 1,
  "title": "Selling Dogma",
  "artist": "The Clouds",
  "price": 44.99,
  "image": "vinyl1.png",
  "year": 2003,
  "genre": "rock",
  "stock": 12
}
```

## 🧪 Developer Tools

- **View DB Table**: `node logTable.js`
- **Create Table**: `node createTable.js`
- **Seed Table**: `node seedTable.js`

## 👨‍🎨 Author

Built by [Code-X-Anuj](https://github.com/codeXanu)

## 📄 License

This project is licensed under the ISC License.
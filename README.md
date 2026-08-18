# Book Store API

A full-stack online bookstore where users can browse a catalog of real books (pulled from the Open Library API, complete with covers), sign up/log in, add books to a cart, and check out. A content-based recommendation feature suggests similar books based on genre, author, and description.

## Tech Stack

- **Backend:** FastAPI + PostgreSQL
- **ORM / Migrations:** SQLAlchemy + Alembic
- **Frontend:** React
- **Recommendations:** scikit-learn (TF-IDF + cosine similarity)
- **Book Data:** Open Library API
- **Package Manager:** uv

## Schema Overview

| Table | Purpose |
|---|---|
| `users` | Accounts, auth, admin flag |
| `books` | Catalog — title, author, genre, ISBN, price, cover image URL |
| `cart_items` | User's in-progress cart (book + quantity) |
| `orders` | Placed orders with status (placed/shipped/delivered) |
| `order_items` | Line items per order, with price frozen at purchase time |

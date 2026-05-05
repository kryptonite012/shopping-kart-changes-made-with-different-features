# 🛒 Dukaan — Your Neighbourhood Store

A simple and clean grocery shopping web app built using HTML, CSS, and JavaScript.
It allows users to browse products, filter by categories, add items to cart, and see a live bill update — just like a mini online store.

---

## 📌 About the Project

Dukaan is designed to simulate a small neighbourhood grocery store experience.
The main goal of this project is to practice frontend development concepts like DOM manipulation, event handling, and UI design.

Everything runs on the browser — no backend required.

---

## ✨ Features

* 🛍️ Browse products (Snacks, Drinks, Dairy, etc.)
* 🔎 Filter products by category
* ➕ Add items to cart
* ➖ Increase / decrease quantity
* ❌ Remove items from cart
* 🧮 Automatic price calculation
* 💸 Discount applied on orders above ₹200
* 🚚 Free delivery on orders above ₹499
* 📱 Responsive design (works on mobile)

---

## 🧠 How It Works

* All products are stored in a JavaScript array
* Cart is managed using an object (`id → quantity`)
* UI updates dynamically whenever cart changes
* Total bill is calculated using simple logic:

  * Subtotal = sum of all items
  * Discount = 5% (if applicable)
  * Delivery = ₹30 or FREE
  * Final Total = subtotal - discount + delivery

---

## 🛠️ Tech Stack

* HTML
* CSS
* JavaScript (Vanilla JS)

No frameworks or libraries used — pure frontend.

---

## 📂 Project Structure


---

## 🚀 How to Run

1. Download or clone the project
2. Open the HTML file in your browser

That’s it — no setup needed!

-----------------------------------------------------------------------------------------
## 💡 Future Improvements

* Save cart using LocalStorage
* Add login/signup system
* Integrate real payment gateway (UPI / Razorpay)
* Connect with backend (Node.js + MongoDB)
* Add product images instead of emojis
* Search bar functionality

------------------------------------------------------------------------------------------
## 🙌 Final Note

This project is built for learning and practice purposes.
It helped in understanding how real e-commerce platforms manage carts and pricing logic on the frontend.

--------------------------------------------------------------------------------------------




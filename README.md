# shopping-kart-changes-made-with-different-features
<script>
const items = [
  { id:1, name:"Lays", cat:"Snacks", price:20 },
  { id:2, name:"Kurkure", cat:"Snacks", price:10 },
  { id:3, name:"Milk", cat:"Dairy", price:30 },
  { id:4, name:"Juice", cat:"Drinks", price:50 }
];

let cart = {};
let currentFilter = "all";

// format price
function price(n) {
  return "₹" + n;
}

// add item
function add(id) {
  if (!cart[id]) cart[id] = 0;
  cart[id]++;
  updateUI();
}

// change quantity
function change(id, val) {
  if (!cart[id]) return;

  cart[id] += val;

  if (cart[id] <= 0) delete cart[id];

  updateUI();
}

// render products
function showProducts() {
  let list = items;

  if (currentFilter !== "all") {
    list = items.filter(i => i.cat === currentFilter);
  }

  const box = document.getElementById("prod-list");

  box.innerHTML = list.map(p => `
    <div>
      <h4>${p.name}</h4>
      <p>${price(p.price)}</p>
      <button onclick="add(${p.id})">Add</button>
    </div>
  `).join("");
}

// render cart
function showCart() {
  const ids = Object.keys(cart);
  const box = document.getElementById("cart-body");

  if (ids.length === 0) {
    box.innerHTML = "Cart is empty";
    return;
  }

  let total = 0;

  box.innerHTML = ids.map(id => {
    const item = items.find(x => x.id == id);
    const qty = cart[id];

    total += item.price * qty;

    return `
      <div>
        ${item.name} x ${qty}
        <button onclick="change(${id},-1)">-</button>
        <button onclick="change(${id},1)">+</button>
      </div>
    `;
  }).join("");

  document.getElementById("b-total").innerText = price(total);
}

// update everything
function updateUI() {
  showProducts();
  showCart();
}

// category click
document.getElementById("cats").addEventListener("click", (e) => {
  if (!e.target.dataset.cat) return;

  currentFilter = e.target.dataset.cat;
  updateUI();
});

// initial load
updateUI();
</script>

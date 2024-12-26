# plant-shop-react
<p>Welcome to Plant Shop, your go-to destination for all things green. We provide a variety of houseplants to help you create a peaceful and natural atmosphere in your home.</p>

<h1>Plant Shop</h1>
<button><a href="/products">Get Started</a></button>
const products = [
  { name: "Fiddle Leaf Fig", image: "/images/fiddle-leaf.jpg", price: "$30" },
  { name: "Snake Plant", image: "/images/snake-plant.jpg", price: "$25" },
  { name: "Peace Lily", image: "/images/peace-lily.jpg", price: "$20" },
  { name: "Aloe Vera", image: "/images/aloe-vera.jpg", price: "$15" },
  { name: "Spider Plant", image: "/images/spider-plant.jpg", price: "$18" },
  { name: "Pothos", image: "/images/pothos.jpg", price: "$22" }
];
const [cartCount, setCartCount] = useState(0);

const addToCart = (product) => {
  setCartCount(cartCount + 1);
  // Disable the button or add the product to the Redux store/cart state
};

return (
  <div>
    {products.map((product) => (
      <div key={product.name}>
        <img src={product.image} alt={product.name} />
        <h3>{product.name}</h3>
        <p>{product.price}</p>
        <button onClick={() => addToCart(product)} disabled={/* Check if already in cart */}>Add to Cart</button>
      </div>
    ))}
  </div>
);
<header>
  <nav>
    <a href="/products">Products</a>
    <a href="/cart">Cart</a>
  </nav>
  <div>
    <span>Cart: {cartCount}</span>
  </div>
</header>
<div>
  <h3>Total Plants: {cartItems.length}</h3>
  <h3>Total Cost: ${cartItems.reduce((total, item) => total + item.price * item.quantity, 0)}</h3>
</div>
<button>Coming Soon</button>
<button><a href="/products">Continue Shopping</a></button>
const increaseQuantity = (product) => {
  // Increase the quantity of the product
};

const decreaseQuantity = (product) => {
  // Decrease the quantity of the product
};

return (
  <div>
    {cartItems.map((item) => (
      <div key={item.name}>
        <h4>{item.name}</h4>
        <p>Price: ${item.price}</p>
        <button onClick={() => increaseQuantity(item)}>+</button>
        <button onClick={() => decreaseQuantity(item)}>-</button>
      </div>
    ))}
  </div>
);
const removeFromCart = (product) => {
  // Remove product from cart
};

return (
  <button onClick={() => removeFromCart(item)}>Delete</button>
);

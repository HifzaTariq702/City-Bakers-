# City-Bakers-
<html lang="en">
 <head>
  <meta charset="utf-8"/>
  <meta content="width=device-width, initial-scale=1" name="viewport"/>
  <title>
   City Bakers - Like Tehzeeb Bakers
  </title>
  <script src="https://cdn.tailwindcss.com">
  </script>
  <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css" rel="stylesheet"/>
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&amp;display=swap" rel="stylesheet"/>
  <style>
   body {
      font-family: "Montserrat", sans-serif;
    }
    /* Custom scrollbar for inventory and cart */
    #cart-list::-webkit-scrollbar,
    #inventory-list::-webkit-scrollbar {
      width: 8px;
    }
    #cart-list::-webkit-scrollbar-thumb,
    #inventory-list::-webkit-scrollbar-thumb {
      background-color: #f472b6;
      border-radius: 4px;
    }
  </style>
 </head>
 <body class="bg-white text-gray-800 flex flex-col min-h-screen">
  <!-- Navbar -->
  <header class="bg-white shadow-md sticky top-0 z-50">
   <div class="container mx-auto flex items-center justify-between px-6 py-4">
    <a class="flex items-center space-x-3" href="#">
     <img alt="City Bakers logo, stylized bread loaf with elegant script" class="w-14 h-14 object-contain" height="60" src="https://storage.googleapis.com/a1aa/image/a5de2b98-7b93-4886-7886-0adeaad406ce.jpg" width="60"/>
     <span class="text-3xl font-extrabold text-pink-600 tracking-wide select-none">
      City Bakers
     </span>
    </a>
    <nav class="hidden md:flex space-x-8 font-semibold text-pink-700">
     <a class="hover:text-pink-500 transition" href="#home">
      Home
     </a>
     <a class="hover:text-pink-500 transition" href="#products">
      Products
     </a>
     <a class="hover:text-pink-500 transition" href="#about">
      About
     </a>
     <a class="hover:text-pink-500 transition" href="#contact">
      Contact
     </a>
     <a class="hover:text-pink-500 transition flex items-center space-x-1" href="#cart">
      <i class="fas fa-shopping-cart">
      </i>
      <span class="text-sm font-bold" id="cart-count">
       0
      </span>
     </a>
    </nav>
    <button aria-label="Toggle menu" class="md:hidden text-pink-600 focus:outline-none" id="mobile-menu-button">
     <i class="fas fa-bars fa-lg">
     </i>
    </button>
   </div>
   <nav class="hidden md:hidden bg-pink-50 px-6 py-4 space-y-3 font-semibold text-pink-700" id="mobile-menu">
    <a class="block hover:text-pink-500 transition" href="#home">
     Home
    </a>
    <a class="block hover:text-pink-500 transition" href="#products">
     Products
    </a>
    <a class="block hover:text-pink-500 transition" href="#about">
     About
    </a>
    <a class="block hover:text-pink-500 transition" href="#contact">
     Contact
    </a>
    <a class="block hover:text-pink-500 transition flex items-center space-x-1" href="#cart">
     <i class="fas fa-shopping-cart">
     </i>
     <span class="text-sm font-bold" id="cart-count-mobile">
      0
     </span>
    </a>
   </nav>
  </header>
  <!-- Hero Section -->
  <section class="relative bg-pink-50 overflow-hidden flex items-center justify-center" id="home" style="min-height: 60vh;">
   <img alt="Background image of fresh baked goods on rustic wooden table with warm lighting" class="absolute inset-0 w-full h-full object-cover opacity-30" height="600" src="https://storage.googleapis.com/a1aa/image/22391907-2a1c-48fa-3c6b-c4c3794ccfef.jpg" width="1200"/>
   <div class="relative z-10 text-center px-6 max-w-3xl">
    <h1 class="text-5xl font-extrabold text-pink-700 mb-4 drop-shadow-md">
     Welcome to City Bakers
    </h1>
    <p class="text-xl text-pink-600 mb-8 drop-shadow-sm">
     Freshly baked delights made with love and tradition.
    </p>
    <a class="inline-block bg-pink-600 hover:bg-pink-700 text-white font-semibold py-3 px-8 rounded shadow-lg transition" href="#products">
     Shop Now
    </a>
   </div>
  </section>
  <!-- Products Section -->
  <section class="container mx-auto px-6 py-12 max-w-7xl" id="products">
   <h2 class="text-4xl font-extrabold text-pink-700 mb-10 border-b-4 border-pink-400 inline-block">
    Our Products
   </h2>
   <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-8" id="product-list">
    <!-- Product cards inserted by JS -->
   </div>
  </section>
  <!-- About Section -->
  <section class="bg-pink-50 py-12 px-6 text-center max-w-4xl mx-auto rounded-lg shadow-md mb-16" id="about">
   <h2 class="text-4xl font-extrabold text-pink-700 mb-6">
    About City Bakers
   </h2>
   <p class="text-lg text-pink-700 max-w-3xl mx-auto leading-relaxed">
    At City Bakers, we blend traditional baking techniques with modern
      flavors to bring you the freshest and most delicious baked goods. Our
      passion for quality and customer satisfaction drives everything we do.
      From crusty breads to sweet pastries, every item is crafted with care.
   </p>
  </section>
  <!-- Contact Section -->
  <section class="container mx-auto px-6 py-12 max-w-4xl rounded-lg shadow-md bg-white mb-16" id="contact">
   <h2 class="text-4xl font-extrabold text-pink-700 mb-6 text-center">
    Contact Us
   </h2>
   <form class="max-w-xl mx-auto space-y-6" id="contact-form">
    <div>
     <label class="block text-pink-700 font-semibold mb-2" for="name">
      Name
     </label>
     <input class="w-full border border-pink-300 rounded px-4 py-2 focus:outline-none focus:ring-2 focus:ring-pink-400" id="name" name="name" placeholder="Your full name" required="" type="text"/>
    </div>
    <div>
     <label class="block text-pink-700 font-semibold mb-2" for="email">
      Email
     </label>
     <input class="w-full border border-pink-300 rounded px-4 py-2 focus:outline-none focus:ring-2 focus:ring-pink-400" id="email" name="email" placeholder="you@example.com" required="" type="email"/>
    </div>
    <div>
     <label class="block text-pink-700 font-semibold mb-2" for="message">
      Message
     </label>
     <textarea class="w-full border border-pink-300 rounded px-4 py-2 focus:outline-none focus:ring-2 focus:ring-pink-400" id="message" name="message" placeholder="Write your message here" required="" rows="4"></textarea>
    </div>
    <button class="w-full bg-pink-600 hover:bg-pink-700 text-white font-semibold py-3 rounded transition" type="submit">
     Send Message
    </button>
   </form>
  </section>
  <!-- Cart Sidebar -->
  <aside aria-label="Shopping cart" class="fixed top-0 right-0 h-full w-80 bg-white shadow-lg transform translate-x-full transition-transform z-50 flex flex-col" id="cart">
   <header class="flex items-center justify-between p-4 border-b border-pink-200">
    <h3 class="text-xl font-bold text-pink-700">
     Your Cart
    </h3>
    <button aria-label="Close cart" class="text-pink-600 hover:text-pink-800 focus:outline-none" id="close-cart">
     <i class="fas fa-times fa-lg">
     </i>
    </button>
   </header>
   <ul class="flex-grow overflow-y-auto divide-y divide-pink-200 p-4 text-pink-700" id="cart-items">
    <li class="text-center italic">
     Your cart is empty.
    </li>
   </ul>
   <div class="p-4 border-t border-pink-200">
    <div class="flex justify-between font-bold text-lg text-pink-800 mb-4">
     <span>
      Total:
     </span>
     <span id="cart-total">
      $0.00
     </span>
    </div>
    <button class="w-full bg-pink-600 hover:bg-pink-700 text-white font-semibold py-3 rounded disabled:opacity-50 disabled:cursor-not-allowed transition" disabled="" id="checkout-btn">
     Checkout
    </button>
   </div>
  </aside>
  <div aria-hidden="true" class="fixed inset-0 bg-black bg-opacity-30 hidden z-40" id="cart-overlay">
  </div>
  <footer class="bg-pink-100 text-pink-700 py-6 text-center font-semibold">
   © 2024 City Bakers. All rights reserved.
  </footer>
  <script>
   // Mobile menu toggle
    const mobileMenuButton = document.getElementById("mobile-menu-button");
    const mobileMenu = document.getElementById("mobile-menu");
    mobileMenuButton.addEventListener("click", () => {
      mobileMenu.classList.toggle("hidden");
    });

    // Cart sidebar toggle
    const cartButtonDesktop = document.querySelector('nav a[href="#cart"]');
    const cartButtonMobile = document.getElementById("cart-count-mobile").parentElement;
    const cartSidebar = document.getElementById("cart");
    const cartOverlay = document.getElementById("cart-overlay");
    const closeCartBtn = document.getElementById("close-cart");

    function openCart() {
      cartSidebar.classList.remove("translate-x-full");
      cartOverlay.classList.remove("hidden");
      cartSidebar.focus();
    }
    function closeCart() {
      cartSidebar.classList.add("translate-x-full");
      cartOverlay.classList.add("hidden");
    }

    cartButtonDesktop.addEventListener("click", (e) => {
      e.preventDefault();
      openCart();
    });
    cartButtonMobile.addEventListener("click", (e) => {
      e.preventDefault();
      openCart();
    });
    closeCartBtn.addEventListener("click", closeCart);
    cartOverlay.addEventListener("click", closeCart);

    // Products data
    const products = [
      {
        id: 1,
        name: "Sourdough Bread",
        price: 5.0,
        image:
          "https://placehold.co/400x300/png?text=Sourdough+Bread",
        alt: "Freshly baked sourdough bread loaf on a wooden board with a rustic background",
      },
      {
        id: 2,
        name: "Chocolate Croissant",
        price: 3.5,
        image:
          "https://placehold.co/400x300/png?text=Chocolate+Croissant",
        alt: "Golden flaky chocolate croissant on a white plate with a cup of coffee",
      },
      {
        id: 3,
        name: "Blueberry Muffin",
        price: 2.75,
        image:
          "https://placehold.co/400x300/png?text=Blueberry+Muffin",
        alt: "Fresh blueberry muffin with blueberries on top on a rustic wooden table",
      },
      {
        id: 4,
        name: "Cinnamon Roll",
        price: 3.0,
        image:
          "https://placehold.co/400x300/png?text=Cinnamon+Roll",
        alt: "Sticky cinnamon roll with icing on a white plate with a wooden background",
      },
      {
        id: 5,
        name: "Bagel with Cream Cheese",
        price: 2.5,
        image:
          "https://placehold.co/400x300/png?text=Bagel+with+Cream+Cheese",
        alt: "Toasted bagel with cream cheese spread on a wooden table with a knife",
      },
      {
        id: 6,
        name: "Lemon Tart",
        price: 4.25,
        image:
          "https://placehold.co/400x300/png?text=Lemon+Tart",
        alt: "Fresh lemon tart with powdered sugar and lemon slices on a white plate",
      },
      {
        id: 7,
        name: "Chocolate Chip Cookie",
        price: 1.5,
        image:
          "https://placehold.co/400x300/png?text=Chocolate+Chip+Cookie",
        alt: "Stack of chocolate chip cookies on a rustic wooden table",
      },
      {
        id: 8,
        name: "Vanilla Cupcake",
        price: 3.25,
        image:
          "https://placehold.co/400x300/png?text=Vanilla+Cupcake",
        alt: "Vanilla cupcake with pink frosting and sprinkles on a white plate",
      },
    ];

    // Render products
    const productList = document.getElementById("product-list");
    products.forEach((product) => {
      const card = document.createElement("article");
      card.className =
        "bg-white rounded-lg shadow-md overflow-hidden flex flex-col";
      card.innerHTML = `
        <img
          src="${product.image}"
          alt="${product.alt}"
          class="w-full h-48 object-cover"
          width="400"
          height="300"
          loading="lazy"
        />
        <div class="p-4 flex flex-col flex-grow">
          <h3 class="text-xl font-semibold text-pink-700 mb-2">${product.name}</h3>
          <p class="text-pink-600 font-semibold mb-4">$${product.price.toFixed(
            2
          )}</p>
          <button
            class="mt-auto bg-pink-600 hover:bg-pink-700 text-white font-semibold py-2 rounded transition flex items-center justify-center"
            aria-label="Add ${product.name} to cart"
            data-id="${product.id}"
          >
            <i class="fas fa-cart-plus mr-2"></i> Add to Cart
          </button>
        </div>
      `;
      productList.appendChild(card);
    });

    // Cart data and functions
    let cart = [];

    const cartItemsContainer = document.getElementById("cart-items");
    const cartTotalEl = document.getElementById("cart-total");
    const cartCountDesktop = document.getElementById("cart-count");
    const cartCountMobile = document.getElementById("cart-count-mobile");
    const checkoutBtn = document.getElementById("checkout-btn");

    function formatPrice(price) {
      return "$" + price.toFixed(2);
    }

    function updateCartCount() {
      const totalQuantity = cart.reduce((sum, item) => sum + item.quantity, 0);
      cartCountDesktop.textContent = totalQuantity;
      cartCountMobile.textContent = totalQuantity;
    }

    function renderCart() {
      cartItemsContainer.innerHTML = "";
      if (cart.length === 0) {
        cartItemsContainer.innerHTML =
          '<li class="text-center italic text-pink-600">Your cart is empty.</li>';
        cartTotalEl.textContent = "$0.00";
        checkoutBtn.disabled = true;
        updateCartCount();
        return;
      }
      let total = 0;
      cart.forEach((item, index) => {
        total += item.price * item.quantity;
        const li = document.createElement("li");
        li.className = "flex justify-between items-center py-3";
        li.innerHTML = `
          <div class="flex items-center space-x-3">
            <img src="${item.image}" alt="Image of ${item.name}" class="w-14 h-14 rounded object-cover flex-shrink-0" width="56" height="56" />
            <div>
              <p class="font-semibold text-pink-700">${item.name}</p>
              <p class="text-pink-600 text-sm">$${item.price.toFixed(2)} × ${item.quantity}</p>
            </div>
          </div>
          <div class="flex items-center space-x-2">
            <button aria-label="Decrease quantity of ${item.name}" class="text-pink-600 hover:text-pink-800 focus:outline-none" data-action="decrease" data-index="${index}">
              <i class="fas fa-minus-circle"></i>
            </button>
            <span class="font-semibold">${item.quantity}</span>
            <button aria-label="Increase quantity of ${item.name}" class="text-pink-600 hover:text-pink-800 focus:outline-none" data-action="increase" data-index="${index}">
              <i class="fas fa-plus-circle"></i>
            </button>
            <button aria-label="Remove ${item.name} from cart" class="text-red-600 hover:text-red-800 focus:outline-none" data-action="remove" data-index="${index}">
              <i class="fas fa-trash-alt"></i>
            </button>
          </div>
        `;
        cartItemsContainer.appendChild(li);
      });
      cartTotalEl.textContent = formatPrice(total);
      checkoutBtn.disabled = false;
      updateCartCount();
    }

    // Add to cart event
    productList.addEventListener("click", (e) => {
      const btn = e.target.closest("button");
      if (!btn) return;
      const id = parseInt(btn.getAttribute("data-id"));
      if (!id) return;
      const product = products.find((p) => p.id === id);
      if (!product) return;

      const existing = cart.find((item) => item.id === id);
      if (existing) {
        existing.quantity++;
      } else {
        cart.push({ ...product, quantity: 1 });
      }
      renderCart();
      openCart();
    });

    // Cart buttons (increase, decrease, remove)
    cartItemsContainer.addEventListener("click", (e) => {
      const btn = e.target.closest("button");
      if (!btn) return;
      const action = btn.getAttribute("data-action");
      const index = parseInt(btn.getAttribute("data-index"));
      if (isNaN(index) || !action) return;

      if (action === "increase") {
        cart[index].quantity++;
      } else if (action === "decrease") {
        cart[index].quantity--;
        if (cart[index].quantity <= 0) {
          cart.splice(index, 1);
        }
      } else if (action === "remove") {
        cart.splice(index, 1);
      }
      renderCart();
    });

    // Checkout button
    checkoutBtn.addEventListener("click", () => {
      if (cart.length === 0) return;
      alert(
        `Thank you for your purchase! Your total is ${formatPrice(
          cart.reduce((sum, item) => sum + item.price * item.quantity, 0)
        )}.`
      );
      cart = [];
      renderCart();
      closeCart();
    });

    // Initialize cart
    renderCart();

    // Accessibility: trap focus in cart when open (optional enhancement)
    // For brevity, not implemented here.
  </script>
 </body>
</html>

<script setup>
    const cartItem = ref(0); // liczba produktów w koszyku
    const searchQuerry = ref(' ');
</script>

<template>
  <header class="header">
    <!-- Górna belka -->
    <div class="top-bar">
      <div class="left">
        <span class="icon"><i class="fas fa-map-marker-alt"></i></span>
        <span>Nasze salony</span>
      </div>
      <div class="center has-text-centered">
        <a href="#" class="has-text-white">KOLEKCJA WIOSNA/LATO 2025!<br> 
        POKAŻ PRODUKTY!</a>
      </div>
      <div class="right">
        <span class="icon"><i class="fas fa-user"></i></span>
        <span>Moje konto</span>
        <span class="icon"><i class="fas fa-heart"></i></span>
        <span>Lista życzeń <span class="wishlist-count">0</span></span>
        <button class="cart-btn">
          <span class="icon"><i class="fas fa-shopping-cart"></i></span>
          Koszyk ({{ cartItem }})
        </button>
      </div>
    </div>

    <!-- Logo i Nawigacja -->
    <nav class="navbar">
      <div class="logo">
        <img src="@/assets/logo.svg" alt="Logo">
      </div>
      <ul class="menu">
        <li><a href="#">SALE UP TO -60%!</a></li>
        <li><a href="#">NOWOŚCI</a></li>
        <li><a href="#">MĘSKIE</a></li>
        <li><a href="#">DAMSKIE</a></li>
        <li><a href="#">DZIECIĘCE</a></li>
        <li><a href="#">AKCESORIA</a></li>
        <li><a href="#">PROMOCJE</a></li>
      </ul>
      <div class="right-section">
        <input type="text" placeholder="Szukaj" class="search-input">
        <span class="icon search-icon"><i class="fas fa-search"></i></span>
      </div>
    </nav>
  </header>
</template>

<style scoped>
/* Styl dla górnej belki */
.top-bar {
  display: flex;
  justify-content: center;
  align-items: center;
  background: black;
  color: #7F7F7F;
  padding: 10px 20px;
  font-size: 14px;
}

.top-bar .left, .top-bar .right {
  display: flex;
  align-items: center;
  position: absolute;
  gap: 0.3rem;
}

.top-bar .left {
  left: 20px;
}

.top-bar .right {
  right: 20px;
}

.top-bar .icon {
  color: #7F7F7F;
  margin-right: 5px;
}

.top-bar .wishlist-count {
  background: white;
  color: black;
  border-radius: 50%;
  padding: 2px 6px;
  font-size: 12px;
  margin-left: 4px;
}

/* Nawigacja */
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: white;
  padding: 15px 20px;
  border-bottom: 1px solid #ddd;
}

.navbar .logo img {
  height: 40px;
}

.navbar .menu {
  display: flex;
  list-style: none;
  justify-content: center;
  flex-grow: 1;
}

.navbar .menu li {
  margin: 0 10px;
}

.navbar .menu a {
  text-decoration: none;
  color: black;
  font-weight: bold;
}

.right-section {
  display: flex;
  align-items: center;
}

.search-input {
  padding: 5px 10px;
  border: 1px solid #ddd;
  border-radius: 5px;
}

.search-icon {
  margin-left: -25px;
  cursor: pointer;
}

.cart-btn {
  background: #47b750;
  color: white;
  padding: 8px 15px;
  border: none;
  border-radius: 5px;
  margin-left: 10px;
  font-weight: bold;
  display: flex;
  align-items: center;
}

.cart-btn .icon {
  color: white;
}
</style>

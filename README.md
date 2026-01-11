# Navbar-
<html>
  <head>
    <title>Ma Navbar</title>
    <meta charset="UTF-8">
    <style>
      :root {
  --primary-color: #2c3e50; /* Couleur pro */
  --accent-color: #e67e22;  /* Orange pour l'action (achat) */
  --white: #ffffff;
  --bg-light: #f8f9fa;
}

/* Header global */
.shop-header {
  position: sticky;
  top: 0;
  z-index: 1000;
  box-shadow: 0 2px 10px rgba(0,0,0,0.05);
  background: var(--white);
}

/* Bandeau promo en haut */
.top-bar {
  background: var(--primary-color);
  color: white;
  text-align: center;
  font-size: 0.8rem;
  padding: 5px 0;
  font-weight: 300;
}

.main-nav {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 15px 5%;
  max-width: 1400px;
  margin: 0 auto;
}

/* Logo */
.shop-logo {
  font-size: 1.5rem;
  font-weight: 900;
  text-decoration: none;
  color: var(--primary-color);
}
.shop-logo span { color: var(--accent-color); }

/* Navigation Categories */
.categories-links {
  display: none; /* Mobile first */
  list-style: none;
  gap: 25px;
}

.categories-links a {
  text-decoration: none;
  color: var(--primary-color);
  font-weight: 600;
  font-size: 0.95rem;
}

.sale a { color: #e74c3c; } /* Rouge pour les promos */

/* Actions & Panier */
.shop-actions {
  display: flex;
  align-items: center;
  gap: 20px;
}

.cart-trigger {
  text-decoration: none;
  font-size: 1.4rem;
  position: relative;
}

.cart-count {
  position: absolute;
  top: -8px;
  right: -10px;
  background: var(--accent-color);
  color: white;
  font-size: 0.7rem;
  padding: 2px 7px;
  border-radius: 50%;
  border: 2px solid white;
}

/* Barre de recherche (cachée sur petit mobile, visible en desktop) */
.search-box {
  display: none;
}

@media (min-width: 1024px) {
  .categories-links, .search-box { display: flex; }
  .mobile-menu-btn { display: none; }
  
  .search-box input {
    padding: 8px 15px;
    border: 1px solid #ddd;
    border-radius: 20px 0 0 20px;
    outline: none;
  }
  .search-box button {
    border: 1px solid #ddd;
    border-left: none;
    background: var(--bg-light);
    padding: 0 10px;
    border-radius: 0 20px 20px 0;
    cursor: pointer;
  }
}
    </style>
  </head>
  <body>
<header class="shop-header">
  <div class="top-bar">Livraison gratuite au Togo à partir de 25.000 FCFA 🚚</div>
  
  <nav class="main-nav">
    <button class="mobile-menu-btn">☰</button>

    <a href="#" class="shop-logo">LOME<span>MARKET</span></a>

    <ul class="categories-links">
      <li><a href="#">Électronique</a></li>
      <li><a href="#">Mode</a></li>
      <li><a href="#">Maison</a></li>
      <li class="sale"><a href="#">Promos %</a></li>
    </ul>

    <div class="shop-actions">
      <div class="search-box">
        <input type="text" placeholder="Rechercher...">
        <button>🔍</button>
      </div>
      <a href="#" title="Mon Compte">👤</a>
      <a href="#" class="cart-trigger">
        🛒<span class="cart-count">0</span>
      </a>
    </div>
  </nav>
</header>
</body>
</html>

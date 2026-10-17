<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Veloraa Beauty - Premium Cosmetics & Skincare</title>
    <!-- FontAwesome CDN -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Jost:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Jost', sans-serif;
        }

        body {
            background-color: #fff5f7;
            color: #2c2c2c;
            padding-bottom: 70px;
            overflow-x: hidden;
        }

        .top-bar {
            background-color: #6a1b29;
            color: #fff;
            text-align: center;
            padding: 8px 15px;
            font-size: 12px;
            font-weight: 500;
        }

        .main-header {
            background: #ffffff;
            border-bottom: 1px solid #f2e2e6;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(106, 27, 41, 0.05);
        }

        .header-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 12px 15px;
        }

        .menu-toggle {
            font-size: 18px;
            cursor: pointer;
            color: #6a1b29;
        }

        .logo-area {
            text-align: center;
            cursor: pointer;
        }

        .logo {
            font-size: 22px;
            font-weight: 700;
            letter-spacing: 1px;
            color: #6a1b29;
        }

        .tagline {
            font-size: 7px;
            letter-spacing: 2px;
            color: #8c535d;
            margin-top: -3px;
            font-weight: 500;
        }

        .header-icons {
            display: flex;
            gap: 12px;
            align-items: center;
        }

        .header-icons a {
            color: #6a1b29;
            font-size: 16px;
            position: relative;
            text-decoration: none;
        }

        .cart-badge {
            position: absolute;
            top: -6px;
            right: -8px;
            background: #6a1b29;
            color: #fff;
            font-size: 9px;
            width: 15px;
            height: 15px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .hero-section {
            background: linear-gradient(135deg, #fce4ec 0%, #f8bbd0 100%);
            padding: 30px 15px;
            margin: 12px auto;
            max-width: 1200px;
            border-radius: 14px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            box-shadow: 0 8px 25px rgba(233, 30, 99, 0.08);
            flex-wrap: wrap;
            gap: 15px;
        }

        .hero-content {
            flex: 1;
            min-width: 240px;
        }

        .hero-content .sub-title {
            font-size: 10px;
            letter-spacing: 1.5px;
            color: #880e4f;
            font-weight: 600;
        }

        .hero-content h2 {
            font-size: 28px;
            font-weight: 700;
            color: #4a1525;
            margin: 6px 0;
            line-height: 1.2;
        }

        .hero-content p {
            color: #662e38;
            font-size: 12px;
            margin-bottom: 12px;
        }

        .hero-btn {
            background: #6a1b29;
            color: #fff;
            padding: 9px 20px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 500;
            display: inline-flex;
            align-items: center;
            gap: 6px;
            font-size: 13px;
        }

        .hero-img-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 8px;
        }

        .hero-img-grid img {
            width: 110px;
            height: 95px;
            object-fit: cover;
            border-radius: 8px;
            box-shadow: 0 3px 8px rgba(0,0,0,0.1);
        }

        .categories-container {
            max-width: 1200px;
            margin: 25px auto;
            padding: 0 12px;
        }

        .section-title-main {
            font-size: 18px;
            font-weight: 700;
            color: #4a1525;
            margin-bottom: 12px;
            display: flex;
            align-items: center;
            gap: 6px;
        }

        .cat-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 12px;
        }

        .cat-card {
            background: #fff;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 3px 10px rgba(106, 27, 41, 0.04);
            cursor: pointer;
            transition: transform 0.3s;
            border: 1px solid #f2e2e6;
            text-align: center;
            padding-bottom: 10px;
        }

        .cat-card:hover {
            transform: translateY(-3px);
        }

        .cat-card img {
            width: 100%;
            height: 110px;
            object-fit: cover;
        }

        .cat-card-body {
            padding: 8px;
        }

        .cat-card-body h4 {
            font-size: 13px;
            color: #4a1525;
            font-weight: 600;
            margin-bottom: 4px;
        }

        .sub-cat-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 3px;
            justify-content: center;
            margin-top: 6px;
        }

        .sub-tag {
            font-size: 9px;
            background: #fce4ec;
            color: #6a1b29;
            padding: 2px 5px;
            border-radius: 4px;
            cursor: pointer;
        }

        .sub-tag:hover {
            background: #6a1b29;
            color: #fff;
        }

        .promo-banner {
            max-width: 1200px;
            margin: 30px auto;
            background: linear-gradient(135deg, #f8bbd0 0%, #fce4ec 100%);
            border-radius: 14px;
            padding: 25px 15px;
            text-align: center;
            box-shadow: 0 4px 15px rgba(0,0,0,0.03);
        }

        .promo-text h3 {
            font-size: 10px;
            letter-spacing: 2px;
            color: #880e4f;
            margin-bottom: 4px;
        }

        .promo-text h1 {
            font-size: 26px;
            color: #4a1525;
            font-weight: 700;
            margin-bottom: 6px;
        }

        .promo-text p {
            color: #662e38;
            font-size: 12px;
            margin-bottom: 12px;
        }

        .promo-btn {
            background: #6a1b29;
            color: #fff;
            padding: 9px 20px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 500;
            display: inline-block;
            font-size: 12px;
        }

        .products-section {
            max-width: 1200px;
            margin: 30px auto;
            padding: 0 12px;
        }

        .section-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 15px;
        }

        .section-header h3 {
            font-size: 18px;
            font-weight: 700;
            color: #4a1525;
        }

        .view-all {
            color: #6a1b29;
            text-decoration: none;
            font-weight: 600;
            font-size: 12px;
            cursor: pointer;
        }

        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
            gap: 15px;
        }

        .product-card {
            background: #fff;
            border-radius: 10px;
            overflow: hidden;
            position: relative;
            box-shadow: 0 3px 12px rgba(106, 27, 41, 0.04);
            transition: transform 0.3s;
        }

        .product-card:hover {
            transform: translateY(-3px);
        }

        .product-badge {
            position: absolute;
            top: 8px;
            left: 8px;
            background: #6a1b29;
            color: #fff;
            font-size: 8px;
            padding: 2px 6px;
            border-radius: 20px;
            font-weight: 600;
            z-index: 2;
        }

        .wishlist-icon {
            position: absolute;
            top: 8px;
            right: 8px;
            background: #fff;
            border: none;
            width: 28px;
            height: 28px;
            border-radius: 50%;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            z-index: 2;
            color: #6a1b29;
        }

        .product-img {
            width: 100%;
            height: 160px;
            background: #fdf6f8;
            overflow: hidden;
            cursor: pointer;
        }

        .product-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.4s;
        }

        .product-card:hover .product-img img {
            transform: scale(1.05);
        }

        .product-details {
            padding: 10px;
        }

        .product-details h4 {
            font-size: 13px;
            font-weight: 600;
            color: #333;
            margin-bottom: 4px;
            cursor: pointer;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

        .rating {
            font-size: 10px;
            color: #ffc107;
            margin-bottom: 6px;
        }

        .price-box {
            display: flex;
            align-items: center;
            gap: 6px;
            margin-bottom: 10px;
        }

        .current-price {
            font-size: 14px;
            font-weight: 700;
            color: #6a1b29;
        }

        .old-price {
            font-size: 11px;
            color: #999;
            text-decoration: line-through;
        }

        .product-action-btns {
            display: flex;
            gap: 5px;
        }

        .btn-cart, .btn-order {
            flex: 1;
            padding: 6px;
            border-radius: 5px;
            font-weight: 600;
            font-size: 11px;
            cursor: pointer;
            border: none;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 3px;
        }

        .btn-cart {
            background: #fce4ec;
            color: #6a1b29;
            border: 1px solid #f8bbd0;
        }

        .btn-order {
            background: #6a1b29;
            color: #fff;
        }

        .modal-overlay {
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background: rgba(0,0,0,0.6);
            display: none;
            align-items: center;
            justify-content: center;
            z-index: 2000;
            padding: 12px;
        }

        .modal-box {
            background: #fff;
            padding: 18px;
            width: 100%;
            max-width: 420px;
            border-radius: 12px;
            position: relative;
            max-height: 90vh;
            overflow-y: auto;
        }

        .close-modal {
            position: absolute;
            top: 10px;
            right: 12px;
            font-size: 18px;
            cursor: pointer;
            color: #333;
        }

        .modal-box h3 {
            color: #6a1b29;
            margin-bottom: 10px;
            font-size: 16px;
        }

        .modal-box input, .modal-box select, .modal-box textarea {
            width: 100%;
            padding: 9px;
            border: 1px solid #ddd;
            border-radius: 6px;
            margin-top: 6px;
            font-size: 12px;
        }

        .bottom-nav {
            position: fixed;
            bottom: 0; left: 0; width: 100%;
            background: #fff;
            border-top: 1px solid #eee;
            display: flex;
            justify-content: space-around;
            padding: 7px 0;
            z-index: 1000;
            box-shadow: 0 -2px 10px rgba(0,0,0,0.05);
        }

        .bottom-nav a {
            text-decoration: none;
            color: #777;
            font-size: 10px;
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 2px;
            cursor: pointer;
        }

        .bottom-nav a i {
            font-size: 15px;
        }

        .bottom-nav a.active, .bottom-nav a:hover {
            color: #6a1b29;
        }
    </style>
</head>
<body>

    <div class="top-bar">
        <span>Cash on Delivery Available Across Bangladesh</span>
    </div>

    <header class="main-header">
        <div class="header-container">
            <div class="menu-toggle" onclick="goHome()" title="Home"><i class="fa-solid fa-house"></i></div>
            
            <div class="logo-area" onclick="goHome()">
                <h1 class="logo">Veloraa Beauty</h1>
                <p class="tagline">BEAUTY • SKINCARE • SELFCARE</p>
            </div>

            <div class="header-icons">
                <a href="#" onclick="openSearchModal()" title="Search"><i class="fa-solid fa-magnifying-glass"></i></a>
                <a href="#" onclick="openCartModal()" title="Cart"><i class="fa-solid fa-bag-shopping"></i><span class="cart-badge" id="total-cart-count">0</span></a>
            </div>
        </div>
    </header>

    <section class="hero-section">
        <div class="hero-content">
            <span class="sub-title">PREMIUM BEAUTY COLLECTION</span>
            <h2>Reveal Your Natural Glow</h2>
            <p>Skincare, makeup, haircare & more — all in one place.</p>
            <a href="#shop" class="hero-btn" onclick="loadAllProducts()">Shop Now <i class="fa-solid fa-arrow-right"></i></a>
        </div>
        <div class="hero-img-grid">
            <img src="https://images.unsplash.com/photo-1620916566398-39f1143ab7be?w=300" alt="Skincare">
            <img src="https://images.unsplash.com/photo-1598440947619-2c35fc9aa908?w=300" alt="Makeup">
            <img src="https://images.unsplash.com/photo-1608248597359-97e3a9c7d42d?w=300" alt="Serum">
            <img src="https://images.unsplash.com/photo-1535585209827-a15fcdbc4c2d?w=300" alt="Haircare">
        </div>
    </section>

    <!-- Categories with Sub-Categories -->
    <div class="categories-container">
        <div class="section-title-main"><i class="fa-solid fa-layer-group"></i> Explore Categories</div>
        <div class="cat-grid" id="category-grid"></div>
    </div>

    <section class="promo-banner">
        <div class="promo-text">
            <h3>BEAUTY ESSENTIALS</h3>
            <h1>UP TO 50% OFF</h1>
            <p>Your favourite brands. At your fingertips.</p>
            <a href="#shop" class="promo-btn" onclick="filterCategory('Discount Products')">Shop Sale →</a>
        </div>
    </section>

    <section class="products-section" id="shop">
        <div class="section-header">
            <h3 id="section-title">Featured Products</h3>
            <span class="view-all" onclick="loadAllProducts()">All Products →</span>
        </div>

        <div class="product-grid" id="product-grid"></div>
    </section>

    <!-- Product Details Modal -->
    <div class="modal-overlay" id="product-modal">
        <div class="modal-box" id="product-modal-content"></div>
    </div>

    <!-- Cart Modal -->
    <div class="modal-overlay" id="cart-modal">
        <div class="modal-box">
            <span class="close-modal" onclick="closeCartModal()">&times;</span>
            <h3>Your Shopping Cart</h3>
            <div id="cart-items-container" style="margin-top: 12px; max-height: 220px; overflow-y: auto;"></div>
            <div style="margin-top: 12px; border-top: 1px solid #ddd; padding-top: 8px; display: flex; justify-content: space-between; font-weight: 700; font-size: 14px;">
                <span>Total Amount:</span>
                <span id="cart-total-price">৳ 0</span>
            </div>
            <button onclick="openCheckoutFromCart()" class="btn-order" style="width: 100%; margin-top: 12px; padding: 10px;">Proceed to Checkout</button>
        </div>
    </div>

    <!-- Checkout Modal -->
    <div class="modal-overlay" id="checkout-modal">
        <div class="modal-box">
            <span class="close-modal" onclick="closeCheckout()">&times;</span>
            <h3>Complete Your Order</h3>
            <p id="checkout-item-summary" style="font-size: 11px; color: #666; margin-bottom: 6px; font-weight:600;"></p>
            <form onsubmit="submitOrder(event)">
                <input type="text" id="cust-name" placeholder="Full Name" required>
                <input type="tel" id="cust-phone" placeholder="Mobile Number (e.g., 017XXXXXXXX)" required>
                <input type="text" id="cust-address" placeholder="House / Road / Area Address" required>
                <input type="text" id="cust-city" placeholder="City / District" required>
                
                <label style="font-size: 11px; font-weight: 600; display: block; margin-top: 8px; color: #4a1525;">Select Payment Method:</label>
                <select id="payment-method" required>
                    <option value="Cash on Delivery">Cash on Delivery (COD)</option>
                    <option value="bKash">bKash Payment</option>
                    <option value="Nagad">Nagad Payment</option>
                    <option value="Rocket">Rocket Payment</option>
                </select>

                <button type="submit" class="btn-order" style="width: 100%; margin-top: 12px; padding: 10px;">Confirm Order</button>
            </form>
        </div>
    </div>

    <!-- Search Modal -->
    <div class="modal-overlay" id="search-modal">
        <div class="modal-box">
            <span class="close-modal" onclick="closeSearchModal()">&times;</span>
            <h3>Search Products</h3>
            <input type="text" id="search-input" placeholder="Search skincare, makeup, perfume..." onkeyup="searchProducts()">
        </div>
    </div>

    <nav class="bottom-nav">
        <a onclick="goHome()" class="active"><i class="fa-solid fa-house"></i> Home</a>
        <a onclick="loadAllProducts()"><i class="fa-solid fa-box-open"></i> All Products</a>
        <a onclick="openCartModal()"><i class="fa-solid fa-bag-shopping"></i> Cart</a>
        <a onclick="openSearchModal()"><i class="fa-solid fa-magnifying-glass"></i> Search</a>
    </nav>

    <script>
        const categories = [
            { name: "Skincare", subs: ["Face Wash", "Cleanser", "Serum", "Moisturizer", "Sunscreen", "Toner", "Face Mask", "Acne Care"], img: "https://images.unsplash.com/photo-1620916566398-39f1143ab7be?w=300" },
            { name: "Makeup", subs: ["Foundation", "Concealer", "Lipstick", "Mascara", "Eyeliner", "Blush", "Compact Powder", "Tools"], img: "https://images.unsplash.com/photo-1598440947619-2c35fc9aa908?w=300" },
            { name: "Hair Care", subs: ["Shampoo", "Conditioner", "Hair Oil", "Hair Serum", "Hair Mask", "Growth Care"], img: "https://images.unsplash.com/photo-1535585209827-a15fcdbc4c2d?w=300" },
            { name: "Body Care", subs: ["Body Lotion", "Body Wash", "Body Scrub", "Hand Cream", "Foot Cream", "Deodorant"], img: "https://images.unsplash.com/photo-1556228720-195a672e8a03?w=300" },
            { name: "Fragrance", subs: ["Perfume", "Body Mist", "Attar", "Deodorant Spray"], img: "https://images.unsplash.com/photo-1523293182086-7651a899d37f?w=300" },
            { name: "Lip & Eye Care", subs: ["Lip Balm", "Lip Scrub", "Eye Cream", "Under Eye Serum", "Eye Patches"], img: "https://images.unsplash.com/photo-1586495777744-4413f21062fa?w=300" },
            { name: "Beauty Accessories", subs: ["Makeup Brushes", "Beauty Blender", "Eye Curler", "Hair Clips", "Headbands"], img: "https://images.unsplash.com/photo-1512496015851-a90fb38ba796?w=300" },
            { name: "Gift Sets & Combos", subs: ["Skincare Combo", "Makeup Set", "Perfume Gift Box", "Beauty Gift Hamper"], img: "https://images.unsplash.com/photo-1549465220-1a8b9238cd48?w=300" },
            { name: "Mens Item", subs: ["Face Care", "Body Care", "Perfume Grooming"], img: "https://images.unsplash.com/photo-1622287162716-f311baa1f2b8?w=300" },
            { name: "Daily Use", subs: ["Essentials", "Selfcare"], img: "https://images.unsplash.com/photo-1522337360788-8b13dee7a37e?w=300" },
            { name: "Top Selling", subs: ["Trending", "Best Deals"], img: "https://images.unsplash.com/photo-1571781926291-c477ebfd024b?w=300" },
            { name: "Most Popular", subs: ["Customer Choice"], img: "https://images.unsplash.com/photo-1516975080664-ed2fc6a32937?w=300" },
            { name: "Discount Products", subs: ["Flash Sale", "Special Deals"], img: "https://images.unsplash.com/photo-1607604276583-eef5d076aa5f?w=300" }
        ];

        const products = [
            { id: 1, name: "COSRX Snail Mucin Essence 96%", category: "Skincare", sub: "Serum", price: 1550, oldPrice: 1850, badge: "Best Seller", stock: 15, desc: "Lightweight essence that repairs and rejuvenates dry skin.", works: "Hydration, dark spot fading, skin repair", how: "Apply evenly after cleansing and toning.", img: "https://images.unsplash.com/photo-1620916566398-39f1143ab7be?w=400", rating: 4.9, reviews: [{name: "Ayesha", comment: "Awesome glow result!", rating: 5}] },
            { id: 2, name: "Laneige Lip Sleeping Mask (Berry)", category: "Lip & Eye Care", sub: "Lip Balm", price: 1280, oldPrice: 1600, badge: "Discount Products", stock: 8, desc: "Provides smooth, firm lips by melting dead skin cells during night.", works: "Lip moisturizing, chapped lips healing", how: "Apply generously before sleep.", img: "https://images.unsplash.com/photo-1598440947619-2c35fc9aa908?w=400", rating: 4.8, reviews: [{name: "Tasnia", comment: "Very soft lips.", rating: 5}] },
            { id: 3, name: "The Ordinary Hyaluronic Acid 2%", category: "Skincare", sub: "Serum", price: 1250, badge: "Top Selling", stock: 20, desc: "Hydration support formula with ultra-pure vegan hyaluronic acid.", works: "Deep skin hydration and plumping", how: "Apply a few drops in AM and PM.", img: "https://images.unsplash.com/photo-1608248597359-97e3a9c7d42d?w=400", rating: 4.7, reviews: [] },
            { id: 4, name: "Maybelline Fit Me Foundation", category: "Makeup", sub: "Foundation", price: 1100, oldPrice: 1300, badge: "Discount Products", stock: 12, desc: "Natural fit liquid foundation that syncs with skin texture.", works: "Pore minimizing, medium coverage", how: "Dot and blend with sponge.", img: "https://images.unsplash.com/photo-1631729371254-42c2892f0e6e?w=400", rating: 4.6, reviews: [] },
            { id: 5, name: "Olaplex No. 7 Bonding Oil", category: "Hair Care", sub: "Hair Oil", price: 2450, oldPrice: 2800, badge: "Most Popular", stock: 6, desc: "Highly concentrated weightless reparative styling oil.", works: "Frizz control, shine boost", how: "Apply small amount to hair.", img: "https://images.unsplash.com/photo-1535585209827-a15fcdbc4c2d?w=400", rating: 4.9, reviews: [] },
            { id: 6, name: "Chanel Coco Mademoiselle", category: "Fragrance", sub: "Perfume", price: 4500, badge: "Luxury", stock: 5, desc: "An oriental fragrance with strong personality and freshness.", works: "Long-lasting enchanting aroma", how: "Spray on pulse points.", img: "https://images.unsplash.com/photo-1523293182086-7651a899d37f?w=400", rating: 5.0, reviews: [] }
        ];

        let cart = [];

        function displayCategories() {
            const grid = document.getElementById('category-grid');
            grid.innerHTML = '';
            categories.forEach(c => {
                let subTagsHTML = c.subs.map(s => `<span class="sub-tag" onclick="event.stopPropagation(); filterSubCategory('${s}')">${s}</span>`).join('');
                grid.innerHTML += `
                    <div class="cat-card" onclick="filterCategory('${c.name}')">
                        <img src="${c.img}" alt="${c.name}">
                        <div class="cat-card-body">
                            <h4>${c.name}</h4>
                            <div class="sub-cat-tags">${subTagsHTML}</div>
                        </div>
                    </div>
                `;
            });
        }

        function displayProducts(items) {
            const grid = document.getElementById('product-grid');
            grid.innerHTML = '';
            if(items.length === 0) {
                grid.innerHTML = '<p style="grid-column: 1/-1; text-align:center; padding: 25px; color:#777;">No products found.</p>';
                return;
            }

            items.forEach(p => {
                grid.innerHTML += `
                    <div class="product-card">
                        <span class="product-badge">${p.badge}</span>
                        <button class="wishlist-icon" onclick="toggleWishlist(this)"><i class="fa-regular fa-heart"></i></button>
                        <div class="product-img" onclick="openProductDetails(${p.id})">
                            <img src="${p.img}" alt="${p.name}">
                        </div>
                        <div class="product-details">
                            <h4 onclick="openProductDetails(${p.id})">${p.name}</h4>
                            <div class="rating">
                                <i class="fa-solid fa-star"></i> <span>${p.rating} (${p.reviews.length})</span>
                            </div>
                            <div class="price-box">
                                <span class="current-price">৳ ${p.price}</span>
                                ${p.oldPrice ? `<span class="old-price">৳ ${p.oldPrice}</span>` : ''}
                            </div>
                            <div class="product-action-btns">
                                <button class="btn-cart" onclick="addToCart(${p.id})"><i class="fa-solid fa-cart-plus"></i> Cart</button>
                                <button class="btn-order" onclick="openCheckoutSingle(${p.id})"><i class="fa-solid fa-bolt"></i> Order</button>
                            </div>
                        </div>
                    </div>
                `;
            });
        }

        displayCategories();
        displayProducts(products.slice(0, 4));

        function goHome() {
            document.getElementById('section-title').innerText = "Featured Products";
            displayProducts(products.slice(0, 4));
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        function loadAllProducts() {
            document.getElementById('section-title').innerText = "All Products Collection";
            displayProducts(products);
            document.getElementById('shop').scrollIntoView({ behavior: 'smooth' });
        }

        function filterCategory(catName) {
            document.getElementById('section-title').innerText = `${catName} Products`;
            const filtered = products.filter(p => p.category.toLowerCase().includes(catName.toLowerCase()) || p.badge.toLowerCase().includes(catName.toLowerCase()));
            displayProducts(filtered.length > 0 ? filtered : products);
            document.getElementById('shop').scrollIntoView({ behavior: 'smooth' });
        }

        function filterSubCategory(subName) {
            document.getElementById('section-title').innerText = `${subName} Products`;
            const filtered = products.filter(p => p.sub.toLowerCase().includes(subName.toLowerCase()));
            displayProducts(filtered.length > 0 ? filtered : products);
            document.getElementById('shop').scrollIntoView({ behavior: 'smooth' });
        }

        function openProductDetails(id) {
            const p = products.find(item => item.id === id);
            const modal = document.getElementById('product-modal');
            const content = document.getElementById('product-modal-content');
            
            let reviewsHTML = p.reviews.map(r => `<div style="background:#fdf6f8; padding:7px; border-radius:5px; margin-top:5px; font-size:11px;"><strong>${r.name}:</strong> ⭐${r.rating} - ${r.comment}</div>`).join('');

            content.innerHTML = `
                <span class="close-modal" onclick="closeProductModal()">&times;</span>
                <img src="${p.img}" alt="${p.name}" style="width:100%; height:180px; object-fit:cover; border-radius:8px;">
                <h3 style="margin-top:8px;">${p.name}</h3>
                <p style="font-size:12px; color:#666; margin-top:3px;">${p.desc}</p>
                <div style="margin-top:8px; font-size:12px;">
                    <p><strong>Works for:</strong> ${p.works}</p>
                    <p><strong>How to use:</strong> ${p.how}</p>
                    <p><strong>Stock:</strong> <span style="color:#6a1b29; font-weight:600;">${p.stock} pcs available</span></p>
                </div>
                <div style="margin-top:10px; display:flex; justify-content:space-between; align-items:center;">
                    <span style="font-size:16px; font-weight:700; color:#6a1b29;">৳ ${p.price}</span>
                    <button class="btn-order" onclick="closeProductModal(); openCheckoutSingle(${p.id})" style="padding: 8px 16px;">Order Now</button>
                </div>
                
                <hr style="margin: 12px 0; border:0; border-top:1px solid #eee;">
                <h4>Customer Reviews</h4>
                <div style="max-height:90px; overflow-y:auto;">${reviewsHTML || '<p style="font-size:11px; color:#886;">No reviews yet.</p>'}</div>
                
                <div style="margin-top:8px;">
                    <input type="text" id="rev-name" placeholder="Your Name">
                    <select id="rev-rating">
                        <option value="5">⭐⭐⭐⭐⭐ (5 Star)</option>
                        <option value="4">⭐⭐⭐⭐ (4 Star)</option>
                    </select>
                    <textarea id="rev-comment" placeholder="Write your review..." rows="2" style="width:100%; margin-top:6px; padding:6px; border:1px solid #ddd; border-radius:5px;"></textarea>
                    <button onclick="submitReview(${p.id})" class="btn-cart" style="width:100%; margin-top:6px; padding:7px;">Submit Review</button>
                </div>
            `;
            modal.style.display = 'flex';
        }

        function closeProductModal() {
            document.getElementById('product-modal').style.display = 'none';
        }

        function submitReview(productId) {
            const name = document.getElementById('rev-name').value;
            const rating = parseInt(document.getElementById('rev-rating').value);
            const comment = document.getElementById('rev-comment').value;

            if(!name || !comment) {
                alert('Please enter name and comment!');
                return;
            }

            const p = products.find(item => item.id === productId);
            p.reviews.push({ name, rating, comment });
            alert('Thank you for your review!');
            openProductDetails(productId);
        }

        function addToCart(productId) {
            const p = products.find(item => item.id === productId);
            const cartItem = cart.find(item => item.id === productId);
            if(cartItem) {
                cartItem.qty++;
            } else {
                cart.push({ ...p, qty: 1 });
            }
            updateCartCount();
            alert(`"${p.name}" added to cart!`);
        }

        function updateCartCount() {
            let total = cart.reduce((sum, item) => sum + item.qty, 0);
            document.getElementById('total-cart-count').innerText = total;
        }

        function openCartModal() {
            const container = document.getElementById('cart-items-container');
            const totalPriceEl = document.getElementById('cart-total-price');
            container.innerHTML = '';
            
            if(cart.length === 0) {
                container.innerHTML = '<p style="text-align:center; color:#777; font-size:12px;">Your cart is empty.</p>';
                totalPriceEl.innerText = '৳ 0';
                document.getElementById('cart-modal').style.display = 'flex';
                return;
            }

            let total = 0;
            cart.forEach((item, index) => {
                total += item.price * item.qty;
                container.innerHTML += `
                    <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:8px; border-bottom:1px solid #f2e2e6; padding-bottom:6px;">
                        <img src="${item.img}" style="width:35px; height:35px; object-fit:cover; border-radius:5px;">
                        <div style="flex:1; margin-left:8px;">
                            <h5 style="font-size:11px; color:#333;">${item.name}</h5>
                            <span style="font-size:10px; color:#6a1b29; font-weight:600;">৳ ${item.price} x ${item.qty}</span>
                        </div>
                        <div style="display:flex; gap:4px; align-items:center;">
                            <button onclick="changeQty(${index}, 1)" style="padding:1px 5px; background:#eee; border:none; cursor:pointer;">+</button>
                            <span style="font-size:11px; font-weight:600;">${item.qty}</span>
                            <button onclick="changeQty(${index}, -1)" style="padding:1px 5px; background:#eee; border:none; cursor:pointer;">-</button>
                            <button onclick="removeFromCart(${index})" style="background:none; border:none; color:red; cursor:pointer; margin-left:4px;"><i class="fa-solid fa-trash"></i></button>
                        </div>
                    </div>
                `;
            });
            totalPriceEl.innerText = `৳ ${total}`;
            document.getElementById('cart-modal').style.display = 'flex';
        }

        function closeCartModal() {
            document.getElementById('cart-modal').style.display = 'none';
        }

        function changeQty(index, change) {
            cart[index].qty += change;
            if(cart[index].qty <= 0) {
                cart.splice(index, 1);
            }
            updateCartCount();
            openCartModal();
        }

        function removeFromCart(index) {
            cart.splice(index, 1);
            updateCartCount();
            openCartModal();
        }

        function openCheckoutSingle(productId) {
            const p = products.find(item => item.id === productId);
            document.getElementById('checkout-item-summary').innerText = `Product: ${p.name} (৳ ${p.price})`;
            document.getElementById('checkout-modal').style.display = 'flex';
        }

        function openCheckoutFromCart() {
            if(cart.length === 0) {
                alert('Your cart is empty!');
                return;
            }
            closeCartModal();
            let total = cart.reduce((sum, item) => sum + (item.price * item.qty), 0);
            document.getElementById('checkout-item-summary').innerText = `Total Cart Order Amount: ৳ ${total}`;
            document.getElementById('checkout-modal').style.display = 'flex';
        }

        function closeCheckout() {
            document.getElementById('checkout-modal').style.display = 'none';
        }

        function submitOrder(e) {
            e.preventDefault();
            const name = document.getElementById('cust-name').value;
            const payment = document.getElementById('payment-method').value;

            alert(`ধন্যবাদ ${name}! আপনার অর্ডারটি সফলভাবে গ্রহণ করা হয়েছে।\nপেমেন্ট মাধ্যম: ${payment}\nখুব শীঘ্রই আপনার সাথে যোগাযোগ করা হবে।`);
            closeCheckout();
            cart = [];
            updateCartCount();
            e.target.reset();
        }

        function openSearchModal() { document.getElementById('search-modal').style.display = 'flex'; }
        function closeSearchModal() { document.getElementById('search-modal').style.display = 'none'; }
        function searchProducts() {
            let query = document.getElementById('search-input').value.toLowerCase();
            let matched = products.filter(p => p.name.toLowerCase().includes(query) || p.category.toLowerCase().includes(query));
            document.getElementById('section-title').innerText = "Search Results";
            displayProducts(matched);
            if(query.trim() === '') {
                displayProducts(products.slice(0, 4));
                document.getElementById('section-title').innerText = "Featured Products";
            }
        }

        function toggleWishlist(btn) {
            const icon = btn.querySelector('i');
            icon.classList.toggle('fa-regular');
            icon.classList.toggle('fa-solid');
            icon.style.color = icon.classList.contains('fa-solid') ? '#6a1b29' : '#333';
        }
    </script>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Sri Ananthlaxmi – Wholesome Eats</title>

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">

  <style>
    :root {
      --bg:#0f1115; 
      --card:#171b23; 
      --text:#e9eef6; 
      --muted:#a0adbb;
      --accent:#19a34a; 
      --gold:#f1b02a; 
      --radius:16px;
    }

    * { box-sizing: border-box; }

    body {
      margin: 0;
      font-family: 'Poppins', system-ui, Arial;
      background: var(--bg);
      color: var(--text);
    }

    .container {
      max-width: 1100px;
      margin: 0 auto;
      padding: 20px;
    }

    /* Header */
    header {
      display: flex;
      align-items: center;
      gap: 10px;
      background: #11151c;
      border: 1px solid #232a35;
      padding: 12px 18px;
      border-radius: var(--radius);
    }

    header .logo {
      width: -160px;
      height: 60px;
      border-radius: 10px;
      object-fit: cover;
    }

    header h1 {
      font-size: 20px;
      margin: 0;
      font-weight: 700;
      line-height: 1.2;
    }

    header small {
      display: block;
      color: var(--muted);
      font-weight: 400;
      font-size: 14px;
    }

    header .tagline {
      margin-top: 4px;
      font-size: 13px;
      color: #c4c9d4;
    }

    /* Filter */
    .filter-bar {
      display: flex;
      justify-content: flex-end;
      margin-top: 20px;
    }

    .filter-bar select {
      background: var(--card);
      border: 1px solid #232a35;
      border-radius: 8px;
      padding: 8px 12px;
      color: var(--text);
      font-size: 14px;
      cursor: pointer;
    }

    /* Product Grid */
    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 18px;
      margin-top: 22px;
    }

    .card {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      background: var(--card);
      border: 1px solid #232a35;
      border-radius: var(--radius);
      overflow: hidden;
      transition: transform .2s ease, box-shadow .2s ease;
      min-height: 520px;
    }

    .card:hover {
      transform: translateY(-4px);
      box-shadow: 0 6px 16px #0005;
    }

    .media img {
      width: 100%;
      height: 220px;
      object-fit: cover;
    }

    .content {
      flex: 1;
      display: flex;
      flex-direction: column;
      justify-content: flex-start;
      padding: 16px;
    }

    .title {
      font-weight: 700;
      font-size: 1.1rem;
      margin: 0 0 8px;
      text-align: center;
    }

    .desc {
      flex-grow: 1;
      color: var(--muted);
      text-align: center;
      margin: 8px 0 16px;
      line-height: 1.4;
      min-height: 60px;
    }

    .price {
      font-size: 20px;
      font-weight: 700;
      background: linear-gradient(90deg, #fff, #f7d77a, #f1b02a);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      text-align: center;
      margin-bottom: 10px;
    }

    .actions {
      margin-top: auto;
      display: flex;
      justify-content: center;
    }

    .btn {
      border: none;
      cursor: pointer;
      padding: 10px 14px;
      border-radius: 12px;
      font-weight: 700;
      text-decoration: none;
      display: inline-block;
    }

    .btn.primary {
      background: linear-gradient(90deg,#1fc770,#19a34a);
      color: #04130a;
    }

    footer {
      margin-top: 30px;
      color: var(--muted);
      font-size: .9rem;
      text-align: center;
    }
  </style>
</head>
<body>
  <div class="container">
    <header>
      <img src="SALWE/SRIlogo.jpg" alt="Sri Ananthlaxmi Wholesome Eats logo" class="logo">
      <div>
        <h1>Sri Ananthlaxmi <small>Wholesome Eats</small></h1>
        <small class="tagline">Naturally Nutritious • Authentically Delicious</small>
      </div>
    </header>

    <!-- Filter Dropdown -->
    <div class="filter-bar">
      <select id="priceFilter">
        <option value="default">Sort by Price</option>
        <option value="lowToHigh">Low to High</option>
        <option value="highToLow">High to Low</option>
      </select>
    </div>

    <!-- Product Grid -->
    <div class="grid" id="productGrid">

      <div class="card" data-price="300">
        <div class="media"><img src="SALWE/copperhandled.jpg" alt="Copper Handled Gift"></div>
        <div class="content">
          <h2 class="title">Copper Handled</h2>
          <p class="desc">Elegant handcrafted copper handles. Ideal for festive gifting and hampers.</p>
          <div class="price">₹300</div>
          <div class="actions">
            <a class="btn primary" href="https://wa.me/919440685654?text=Hello!%20I'm%20interested%20in%20the%20product%20'Copper%20Handled'%20from%20Sri%20Ananthlaxmi%20Wholesome%20Eats.">Order on WhatsApp</a>
          </div>
        </div>
      </div>

      <div class="card" data-price="250">
        <div class="media"><img src="SALWE/cowbag.jpg" alt="Green Gift Bag"></div>
        <div class="content">
          <h2 class="title">Green Gift Bag</h2>
          <p class="desc">Eco-friendly green bag with golden handles. Durable and reusable for multiple occasions.</p>
          <div class="price">₹250</div>
          <div class="actions">
            <a class="btn primary" href="https://wa.me/919440685654?text=Hello!%20I'm%20interested%20in%20the%20product%20'Green%20Gift%20Bag'%20from%20Sri%20Ananthlaxmi%20Wholesome%20Eats.">Order on WhatsApp</a>
          </div>
        </div>
      </div>

      <div class="card" data-price="350">
        <div class="media"><img src="SALWE/flowercopperbox4.jpg" alt="Copper Gift Box"></div>
        <div class="content">
          <h2 class="title">Copper Gift Box</h2>
          <p class="desc">A perfect festive combo box with premium handcrafted packaging. Ideal for gifting.</p>
          <div class="price">₹350</div>
          <div class="actions">
            <a class="btn primary" href="https://wa.me/919440685654?text=Hello!%20I'm%20interested%20in%20the%20product%20'Copper%20Gift%20Box'%20from%20Sri%20Ananthlaxmi%20Wholesome%20Eats.">Order on WhatsApp</a>
          </div>
        </div>
      </div>

      <div class="card" data-price="380">
        <div class="media"><img src="SALWE/handbag.jpg" alt="Hand Bag"></div>
        <div class="content">
          <h2 class="title">Hand Bag</h2>
          <p class="desc">Stylish bag for sweets, dry fruits, or return gifts. Sustainable and reusable.</p>
          <div class="price">₹380</div>
          <div class="actions">
            <a class="btn primary" href="https://wa.me/919440685654?text=Hello!%20I'm%20interested%20in%20the%20product%20'Hand%20Bag'%20from%20Sri%20Ananthlaxmi%20Wholesome%20Eats.">Order on WhatsApp</a>
          </div>
        </div>
      </div>

      <div class="card" data-price="350">
        <div class="media"><img src="SALWE/loveshapedcopperhandled.jpg" alt="Love Shaped Copper Handle"></div>
        <div class="content">
          <h2 class="title">Love-Shaped Copper Handle</h2>
          <p class="desc">Beautiful handcrafted bag with a love-shaped copper handle — perfect for special occasions.</p>
          <div class="price">₹350</div>
          <div class="actions">
            <a class="btn primary" href="https://wa.me/919440685654?text=Hello!%20I'm%20interested%20in%20the%20product%20'Love-Shaped%20Copper%20Handle'%20from%20Sri%20Ananthlaxmi%20Wholesome%20Eats.">Order on WhatsApp</a>
          </div>
        </div>
      </div>

      <div class="card" data-price="370">
        <div class="media"><img src="SALWE/Redbag2.jpg" alt="Red Bag"></div>
        <div class="content">
          <h2 class="title">Red Gift Bag</h2>
          <p class="desc">Bright red bag with gold handles. Adds festive charm to your gifts.</p>
          <div class="price">₹370</div>
          <div class="actions">
            <a class="btn primary" href="https://wa.me/919440685654?text=Hello!%20I'm%20interested%20in%20the%20product%20'Red%20Gift%20Bag'%20from%20Sri%20Ananthlaxmi%20Wholesome%20Eats.">Order on WhatsApp</a>
          </div>
        </div>
      </div>

      <div class="card" data-price="450">
        <div class="media"><img src="SALWE/silverhandledcowbox.jpg" alt="Silver Handled Box"></div>
        <div class="content">
          <h2 class="title">Silver Handled Cow Box</h2>
          <p class="desc">Premium silver-handled box with a cultural motif, perfect for festive gifting.</p>
          <div class="price">₹450</div>
          <div class="actions">
            <a class="btn primary" href="https://wa.me/919440685654?text=Hello!%20I'm%20interested%20in%20the%20product%20'Silver%20Handled%20Cow%20Box'%20from%20Sri%20Ananthlaxmi%20Wholesome%20Eats.">Order on WhatsApp</a>
          </div>
        </div>
      </div>

      <div class="card" data-price="300">
        <div class="media"><img src="SALWE/Transparentcover.jpg" alt="Transparent Bag"></div>
        <div class="content">
          <h2 class="title">Transparent Cover Bag</h2>
          <p class="desc">Clear transparent bag ideal for sweets or dry fruits with an elegant finish.</p>
          <div class="price">₹300</div>
          <div class="actions">
            <a class="btn primary" href="https://wa.me/919440685654?text=Hello!%20I'm%20interested%20in%20the%20product%20'Transparent%20Cover%20Bag'%20from%20Sri%20Ananthlaxmi%20Wholesome%20Eats.">Order on WhatsApp</a>
          </div>
        </div>
      </div>

      <div class="card" data-price="600">
        <div class="media"><img src="SALWE/coppercowplatewithceramicbox.jpg" alt="Copper Plate with ceramic box"></div>
        <div class="content">
          <h2 class="title">Copper Cow Plate</h2>
          <p class="desc">Elegant copper plate with ceramic box, perfect for pooja or gifting.</p>
          <div class="price">₹600</div>
          <div class="actions">
            <a class="btn primary" href="https://wa.me/919440685654?text=Hello!%20I'm%20interested%20in%20the%20product%20'Copper%20Cow%20Plate'%20from%20Sri%20Ananthlaxmi%20Wholesome%20Eats.">Order on WhatsApp</a>
          </div>
        </div>
      </div>

      <div class="card" data-price="350">
        <div class="media"><img src="SALWE/bluepouch.jpg" alt="Blue Pouch"></div>
        <div class="content">
          <h2 class="title">Blue Pouch Bag</h2>
          <p class="desc">Elegant blue pouch for sweets, dry fruits, or accessories.</p>
          <div class="price">₹350</div>
          <div class="actions">
            <a class="btn primary" href="https://wa.me/919440685654?text=Hello!%20I'm%20interested%20in%20the%20product%20'Blue%20Pouch%20Bag'%20from%20Sri%20Ananthlaxmi%20Wholesome%20Eats.">Order on WhatsApp</a>
          </div>
        </div>
      </div>

      <div class="card" data-price="400">
        <div class="media"><img src="SALWE/whitejutebag.jpg" alt="White Jute Bag"></div>
        <div class="content">
          <h2 class="title">White Jute Bag</h2>
          <p class="desc">Eco-friendly white jute bag ideal for return gifts and festive occasions.</p>
          <div class="price">₹400</div>
          <div class="actions">
            <a class="btn primary" href="https://wa.me/919440685654?text=Hello!%20I'm%20interested%20in%20the%20product%20'White%20Jute%20Bag'%20from%20Sri%20Ananthlaxmi%20Wholesome%20Eats.">Order on WhatsApp</a>
          </div>
        </div>
      </div>

    </div>

    <footer>© <span id="yr"></span> Sri Ananthlaxmi Wholesome Eats</footer>
  </div>

  <script>
    document.getElementById('yr').textContent = new Date().getFullYear();

    // Price sorting logic
    const filter = document.getElementById('priceFilter');
    const grid = document.getElementById('productGrid');

    filter.addEventListener('change', () => {
      const cards = Array.from(grid.children);
      const value = filter.value;

      if (value === 'lowToHigh') {
        cards.sort((a, b) => a.dataset.price - b.dataset.price);
      } else if (value === 'highToLow') {
        cards.sort((a, b) => b.dataset.price - a.dataset.price);
      } else {
        return;
      }

      cards.forEach(card => grid.appendChild(card));
    });
  </script>
</body>
</html>

## 1. Aim

To create a responsive product listing webpage containing product cards with images, product names, prices, and buttons using HTML and CSS Flexbox.

## 2. Objectives

- Create at least six product cards.
- Add an image, name, price, and button to each card.
- Use `display: flex` and `flex-wrap: wrap` on the product container.
- Use `gap` to add spacing between cards.
- Understand and demonstrate `flex-grow`, `flex-shrink`, and `flex-basis`.
- Make product cards wrap onto the next line on smaller screens.
- Capture desktop and mobile screenshots.

## 3. Project Structure

Create a folder named `Assignment-7.3` with the following files:

```text
Assignment-7.3/
├── index.html
└── style.css
```

## 4. HTML Code — `index.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Assignment 7.3 - Responsive Product Listing</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Website Header -->
    <header class="header">
        <div class="header-container">
            <a href="#home" class="logo">Shop<span>Ease</span></a>

            <nav class="navigation">
                <a href="#home">Home</a>
                <a href="#products">Products</a>
                <a href="#about">About</a>
                <a href="#contact">Contact</a>
            </nav>

            <a href="#products" class="header-button">Shop Now</a>
        </div>
    </header>

    <!-- Hero Section -->
    <main id="home">
        <section class="hero">
            <p class="eyebrow">WELCOME TO SHOPEASE</p>
            <h1>Find Your Favourite Products</h1>
            <p>
                Explore our collection of electronics, accessories,
                and everyday essentials at great prices.
            </p>
            <a href="#products" class="hero-button">Explore Products</a>
        </section>

        <!-- Product Listing Section -->
        <section class="products-section" id="products">

            <div class="section-heading">
                <h2>Our Products</h2>
                <p>Discover something special for yourself.</p>
            </div>

            <!-- Flexbox Product Container -->
            <div class="products-container">

                <!-- Product 1 -->
                <article class="product-card">
                    <div class="product-image">
                        <img
                            src="https://images.unsplash.com/photo-1505740420928-5e560c06d30e?auto=format&fit=crop&w=600&q=80"
                            alt="Black wireless headphones"
                            loading="lazy"
                        >
                    </div>

                    <div class="product-info">
                        <span class="category">Electronics</span>
                        <h3>Wireless Headphones</h3>
                        <p class="product-description">
                            Enjoy music with comfortable headphones.
                        </p>
                        <p class="price">₹1,499</p>
                        <button class="product-button" type="button">
                            Add to Cart
                        </button>
                    </div>
                </article>

                <!-- Product 2 -->
                <article class="product-card">
                    <div class="product-image">
                        <img
                            src="https://images.unsplash.com/photo-1523275335684-37898b6baf30?auto=format&fit=crop&w=600&q=80"
                            alt="Classic wristwatch"
                            loading="lazy"
                        >
                    </div>

                    <div class="product-info">
                        <span class="category">Accessories</span>
                        <h3>Classic Wristwatch</h3>
                        <p class="product-description">
                            A timeless watch for everyday use.
                        </p>
                        <p class="price">₹2,199</p>
                        <button class="product-button" type="button">
                            Add to Cart
                        </button>
                    </div>
                </article>

                <!-- Product 3 -->
                <article class="product-card">
                    <div class="product-image">
                        <img
                            src="https://images.unsplash.com/photo-1526170375885-4d8ecf77b99f?auto=format&fit=crop&w=600&q=80"
                            alt="Compact digital camera"
                            loading="lazy"
                        >
                    </div>

                    <div class="product-info">
                        <span class="category">Photography</span>
                        <h3>Digital Camera</h3>
                        <p class="product-description">
                            Capture and save your favourite moments.
                        </p>
                        <p class="price">₹5,499</p>
                        <button class="product-button" type="button">
                            Add to Cart
                        </button>
                    </div>
                </article>

                <!-- Product 4 -->
                <article class="product-card">
                    <div class="product-image">
                        <img
                            src="https://images.unsplash.com/photo-1542291026-7eec264c27ff?auto=format&fit=crop&w=600&q=80"
                            alt="Red sports shoe"
                            loading="lazy"
                        >
                    </div>

                    <div class="product-info">
                        <span class="category">Footwear</span>
                        <h3>Sports Shoes</h3>
                        <p class="product-description">
                            Comfortable shoes for daily activities.
                        </p>
                        <p class="price">₹1,899</p>
                        <button class="product-button" type="button">
                            Add to Cart
                        </button>
                    </div>
                </article>

                <!-- Product 5 -->
                <article class="product-card">
                    <div class="product-image">
                        <img
                            src="https://images.unsplash.com/photo-1503602642458-232111445657?auto=format&fit=crop&w=600&q=80"
                            alt="Modern chair"
                            loading="lazy"
                        >
                    </div>

                    <div class="product-info">
                        <span class="category">Home</span>
                        <h3>Modern Chair</h3>
                        <p class="product-description">
                            Add comfort and style to your workspace.
                        </p>
                        <p class="price">₹3,299</p>
                        <button class="product-button" type="button">
                            Add to Cart
                        </button>
                    </div>
                </article>

                <!-- Product 6 -->
                <article class="product-card">
                    <div class="product-image">
                        <img
                            src="https://images.unsplash.com/photo-1548036328-c9fa89d128fa?auto=format&fit=crop&w=600&q=80"
                            alt="Stylish handbag"
                            loading="lazy"
                        >
                    </div>

                    <div class="product-info">
                        <span class="category">Fashion</span>
                        <h3>Stylish Handbag</h3>
                        <p class="product-description">
                            A practical accessory for everyday outings.
                        </p>
                        <p class="price">₹1,699</p>
                        <button class="product-button" type="button">
                            Add to Cart
                        </button>
                    </div>
                </article>

                <!-- Product 7 -->
                <article class="product-card">
                    <div class="product-image">
                        <img
                            src="https://images.unsplash.com/photo-1583394838336-acd977736f90?auto=format&fit=crop&w=600&q=80"
                            alt="Over-ear audio headphones"
                            loading="lazy"
                        >
                    </div>

                    <div class="product-info">
                        <span class="category">Electronics</span>
                        <h3>Audio Headset</h3>
                        <p class="product-description">
                            Enjoy clear audio for music and calls.
                        </p>
                        <p class="price">₹1,299</p>
                        <button class="product-button" type="button">
                            Add to Cart
                        </button>
                    </div>
                </article>

                <!-- Product 8 -->
                <article class="product-card">
                    <div class="product-image">
                        <img
                            src="https://images.unsplash.com/photo-1512499617640-c74ae3a79d37?auto=format&fit=crop&w=600&q=80"
                            alt="Everyday personal care products"
                            loading="lazy"
                        >
                    </div>

                    <div class="product-info">
                        <span class="category">Lifestyle</span>
                        <h3>Daily Essentials</h3>
                        <p class="product-description">
                            Useful essentials for your daily routine.
                        </p>
                        <p class="price">₹799</p>
                        <button class="product-button" type="button">
                            Add to Cart
                        </button>
                    </div>
                </article>

            </div>
        </section>

        <!-- About Section -->
        <section class="about-section" id="about">
            <h2>About ShopEase</h2>
            <p>
                ShopEase is a sample online store created to practise
                HTML, CSS, Flexbox, and responsive web design.
            </p>
        </section>

        <!-- Contact Section -->
        <section class="contact-section" id="contact">
            <h2>Contact Us</h2>
            <p>Email: support@example.com</p>
            <p>For this assignment, the contact details are examples.</p>
        </section>
    </main>

    <!-- Footer -->
    <footer class="footer">
        <p>&copy; 2026 ShopEase. Created for Assignment 7.3.</p>
    </footer>

</body>
</html>
```

## 5. CSS Code — `style.css`

```css
/* Reset Default Browser Styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* Smooth Scrolling */
html {
    scroll-behavior: smooth;
}

/* General Page Styling */
body {
    font-family: Arial, Helvetica, sans-serif;
    background-color: #f8fafc;
    color: #1e293b;
    line-height: 1.6;
}

/* Header */
.header {
    background-color: #ffffff;
    box-shadow: 0 3px 12px rgba(15, 23, 42, 0.08);
    position: sticky;
    top: 0;
    z-index: 100;
}

.header-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 24px;
    max-width: 1250px;
    margin: 0 auto;
    padding: 18px 28px;
}

/* Logo */
.logo {
    color: #172554;
    font-size: 27px;
    font-weight: bold;
    text-decoration: none;
    white-space: nowrap;
}

.logo span {
    color: #2563eb;
}

/* Navigation */
.navigation {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 24px;
    flex-wrap: wrap;
}

.navigation a {
    color: #475569;
    font-size: 14px;
    font-weight: 600;
    text-decoration: none;
    transition: color 0.3s ease;
}

.navigation a:hover {
    color: #2563eb;
}

/* Header Button */
.header-button {
    background-color: #2563eb;
    color: #ffffff;
    padding: 10px 18px;
    border-radius: 8px;
    text-decoration: none;
    font-size: 14px;
    font-weight: bold;
    white-space: nowrap;
}

.header-button:hover {
    background-color: #1d4ed8;
}

/* Hero Section */
.hero {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    min-height: 350px;
    padding: 70px 20px;
    text-align: center;
    background: linear-gradient(135deg, #eff6ff, #dbeafe);
}

.eyebrow {
    color: #2563eb;
    font-size: 12px;
    font-weight: bold;
    letter-spacing: 2px;
    margin-bottom: 12px;
}

.hero h1 {
    color: #172554;
    font-size: 40px;
    margin-bottom: 15px;
}

.hero > p:not(.eyebrow) {
    max-width: 600px;
    color: #475569;
    margin-bottom: 24px;
}

.hero-button {
    background-color: #2563eb;
    color: #ffffff;
    padding: 12px 22px;
    border-radius: 8px;
    font-weight: bold;
    text-decoration: none;
}

.hero-button:hover {
    background-color: #1d4ed8;
}

/* Products Section */
.products-section {
    max-width: 1250px;
    margin: 0 auto;
    padding: 65px 28px;
}

.section-heading {
    text-align: center;
    margin-bottom: 38px;
}

.section-heading h2 {
    color: #172554;
    font-size: 32px;
    margin-bottom: 8px;
}

.section-heading p {
    color: #64748b;
}

/* Main Flexbox Product Container */
.products-container {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: center;
    align-items: stretch;
    gap: 28px;
}

/* Product Card */
.product-card {
    display: flex;
    flex-direction: column;

    /*
       flex-grow: 1 allows cards to use available extra space.
       flex-shrink: 1 allows cards to shrink when necessary.
       flex-basis: 240px sets the preferred initial card width.
    */
    flex: 1 1 240px;

    min-width: 0;
    max-width: 280px;
    background-color: #ffffff;
    border: 1px solid #e2e8f0;
    border-radius: 14px;
    overflow: hidden;
    box-shadow: 0 5px 18px rgba(15, 23, 42, 0.06);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

/* Product Card Hover Effect */
.product-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 12px 28px rgba(15, 23, 42, 0.12);
}

/* Product Image */
.product-image {
    width: 100%;
    height: 190px;
    overflow: hidden;
    background-color: #e2e8f0;
}

.product-image img {
    display: block;
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: transform 0.4s ease;
}

.product-card:hover .product-image img {
    transform: scale(1.05);
}

/* Product Details */
.product-info {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    flex-grow: 1;
    padding: 20px;
}

.category {
    color: #2563eb;
    background-color: #eff6ff;
    padding: 4px 9px;
    border-radius: 20px;
    font-size: 11px;
    font-weight: bold;
    margin-bottom: 10px;
}

.product-info h3 {
    color: #172554;
    font-size: 18px;
    margin-bottom: 8px;
}

.product-description {
    color: #64748b;
    font-size: 13px;
    margin-bottom: 16px;
}

/* Product Price */
.price {
    color: #1d4ed8;
    font-size: 22px;
    font-weight: bold;
    margin-top: auto;
    margin-bottom: 16px;
}

/* Product Button */
.product-button {
    width: 100%;
    padding: 11px 12px;
    border: none;
    border-radius: 8px;
    background-color: #2563eb;
    color: #ffffff;
    font-size: 14px;
    font-weight: bold;
    cursor: pointer;
    transition: background-color 0.3s ease;
}

.product-button:hover {
    background-color: #1d4ed8;
}

/* About Section */
.about-section {
    padding: 55px 20px;
    text-align: center;
    background-color: #ffffff;
}

.about-section h2,
.contact-section h2 {
    color: #172554;
    font-size: 28px;
    margin-bottom: 12px;
}

.about-section p {
    max-width: 650px;
    margin: 0 auto;
    color: #64748b;
}

/* Contact Section */
.contact-section {
    padding: 45px 20px;
    text-align: center;
    background-color: #f1f5f9;
}

.contact-section p {
    color: #64748b;
    font-size: 14px;
}

/* Footer */
.footer {
    padding: 22px 15px;
    background-color: #172554;
    color: #ffffff;
    text-align: center;
    font-size: 13px;
}

/* Tablet Screens */
@media (max-width: 900px) {
    .header-container {
        flex-wrap: wrap;
        justify-content: center;
    }

    .navigation {
        gap: 16px;
    }

    .hero h1 {
        font-size: 34px;
    }

    .products-section {
        padding: 50px 22px;
    }

    .products-container {
        gap: 22px;
    }

    .product-card {
        flex: 1 1 220px;
        max-width: 320px;
    }
}

/* Mobile Screens */
@media (max-width: 600px) {
    .header-container {
        flex-direction: column;
        gap: 16px;
        padding: 18px 14px;
    }

    .navigation {
        justify-content: center;
        gap: 12px 18px;
    }

    .header-button {
        align-self: center;
    }

    .hero {
        min-height: 300px;
        padding: 55px 18px;
    }

    .hero h1 {
        font-size: 28px;
    }

    .hero > p:not(.eyebrow) {
        font-size: 14px;
    }

    .products-section {
        padding: 42px 16px;
    }

    .section-heading h2 {
        font-size: 27px;
    }

    .products-container {
        flex-direction: row;
        flex-wrap: wrap;
        justify-content: center;
        gap: 18px;
    }

    .product-card {
        /*
           Each card uses approximately half the available row
           when space allows, then wraps when there is not enough room.
        */
        flex: 1 1 145px;
        max-width: 100%;
    }

    .product-image {
        height: 150px;
    }

    .product-info {
        padding: 14px;
    }

    .product-info h3 {
        font-size: 16px;
    }

    .product-description {
        font-size: 12px;
    }

    .price {
        font-size: 19px;
    }

    .product-button {
        font-size: 13px;
        padding: 10px 8px;
    }
}

/* Very Small Mobile Screens */
@media (max-width: 360px) {
    .products-container {
        flex-direction: column;
        align-items: center;
    }

    .product-card {
        width: 100%;
        max-width: 300px;
        flex: 1 1 auto;
    }

    .product-image {
        height: 190px;
    }
}
```

## 6. Explanation of Important Flexbox Properties

### A. `display: flex`

It makes the product container a Flexbox container. Its direct children become flex items.

```css
.products-container {
    display: flex;
}
```

### B. `flex-wrap: wrap`

It allows cards to move to the next line when there is not enough horizontal space.

```css
.products-container {
    display: flex;
    flex-wrap: wrap;
}
```

Without wrapping, cards may become too narrow or overflow their container.

### C. `gap`

It creates consistent spacing between product cards horizontally and vertically.

```css
.products-container {
    gap: 28px;
}
```

### D. `flex-grow`

`flex-grow` controls how much a card can grow to use extra available space.

```css
.product-card {
    flex-grow: 1;
}
```

A value of `1` allows the card to share extra space with other eligible cards.

### E. `flex-shrink`

`flex-shrink` controls how much a flex item can shrink when there is insufficient space on a line.

```css
.product-card {
    flex-shrink: 1;
}
```

A value of `1` allows the card to shrink when needed, subject to its other sizing constraints.

### F. `flex-basis`

`flex-basis` sets the initial preferred size of a flex item before remaining space is distributed.

```css
.product-card {
    flex-basis: 240px;
}
```

### G. Shorthand Property: `flex`

The following line combines all three properties:

```css
.product-card {
    flex: 1 1 240px;
}
```

It means:

- First `1`: the card can grow.
- Second `1`: the card can shrink.
- `240px`: the initial preferred width.

## 7. How to Run the Project

1. Open Visual Studio Code.
2. Create a folder named `Assignment-7.3`.
3. Create `index.html` and `style.css`.
4. Copy the complete HTML code into `index.html`.
5. Copy the complete CSS code into `style.css`.
6. Save both files using `Ctrl + S`.
7. Open `index.html` in your browser or use the Live Server extension.
8. Ensure you have an internet connection for the externally hosted product images.
9. Resize the browser window to test how the cards wrap.

## 8. Testing and Observation

| Test | Expected Result |
|---|---|
| Desktop width | Several product cards appear in each row, depending on available space. |
| Tablet width | Cards wrap onto additional rows when required. |
| Mobile width | Cards become narrower and wrap to fit the screen. |
| Very small mobile width | Cards stack vertically. |
| Hover over a card | The card moves up slightly and its image zooms in. |
| Hover over a button | The button background changes color. |
| Inspect CSS | `flex-grow`, `flex-shrink`, and `flex-basis` are defined through the `flex` shorthand. |

## 9. Screenshots for Submission

### Screenshot 1 — Desktop View

1. Open the website in the browser.
2. Maximize the browser window.
3. Scroll to the **Our Products** section.
4. Ensure several product cards are visible.
5. Capture a screenshot using `Win + Shift + S`.
6. Save it as `desktop-view.png`.

### Screenshot 2 — Mobile View

1. Open browser Developer Tools using `F12`.
2. Enable the device toolbar using `Ctrl + Shift + M`.
3. Select a mobile device or set the viewport width to approximately 390px.
4. Check that product cards wrap correctly without horizontal page overflow.
5. Capture a screenshot.
6. Save it as `mobile-view.png`.

## 10. Expected Output

The finished webpage displays:

- A ShopEase header and navigation bar.
- A hero section with a heading and Explore Products button.
- Eight product cards with images, names, descriptions, prices, and Add to Cart buttons.
- Responsive product rows using Flexbox.
- Consistent spacing between cards using `gap`.
- Hover effects on cards, images, and buttons.
- About, Contact, and Footer sections.
- A layout that adapts to desktop, tablet, and mobile screens.

**Note:** Product prices and store details are sample content. Product images are loaded from Unsplash, so they require an internet connection. The Add to Cart buttons are for display and do not implement cart functionality.

## 11. Submission Checklist

- [ ] `index.html` created.
- [ ] `style.css` created.
- [ ] At least six product cards included.
- [ ] Every card has an image, name, price, and button.
- [ ] `display: flex` applied to the product container.
- [ ] `flex-wrap: wrap` applied.
- [ ] `gap` used for spacing.
- [ ] `flex-grow`, `flex-shrink`, and `flex-basis` demonstrated.
- [ ] Cards wrap properly on smaller screens.
- [ ] Desktop screenshot saved as `desktop-view.png`.
- [ ] Mobile screenshot saved as `mobile-view.png`.

## 12. Conclusion

In this assignment, I created a responsive product listing webpage using HTML and CSS Flexbox. I added eight product cards containing images, names, prices, and buttons. I practised `display: flex`, `flex-wrap`, `gap`, `flex-grow`, `flex-shrink`, and `flex-basis`. I also used CSS media queries to make the product listing responsive across desktop, tablet, and mobile screens.

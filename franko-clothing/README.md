# FRANKO CLOTHING — Website Documentation

## Folder Structure

```
franko-clothing/
│
├── index.html              ← Home / Landing page (6 sections)
│
├── pages/
│   ├── shop.html           ← Shop page (filter tabs per category)
│   ├── about.html          ← Our Story page
│   └── contact.html        ← Contact page
│
├── css/
│   └── style.css           ← All global styles
│
├── js/
│   └── main.js             ← Cart, scroll reveal, WhatsApp logic
│
└── images/                 ← Replace placeholder images here
    ├── hero/
    │   └── hero-main.jpg
    ├── suits/
    │   ├── category-suits.jpg
    │   ├── suit-001.jpg
    │   ├── suit-002.jpg
    │   ├── suit-003.jpg
    │   └── suit-004.jpg
    ├── shirts/
    │   ├── category-shirts.jpg
    │   ├── shirt-001.jpg
    │   ├── shirt-002.jpg
    │   ├── shirt-003.jpg
    │   └── shirt-004.jpg
    ├── shoes/
    │   ├── category-shoes.jpg
    │   ├── shoes-001.jpg
    │   ├── shoes-002.jpg
    │   ├── shoes-003.jpg
    │   └── shoes-004.jpg
    ├── accessories/
    │   ├── category-accessories.jpg
    │   ├── acc-001.jpg   ← Pocket Square
    │   ├── acc-002.jpg   ← Silk Tie
    │   ├── acc-003.jpg   ← Cufflinks
    │   ├── acc-004.jpg   ← Belt
    │   ├── staff-001.jpg ← Ebony Staff
    │   ├── staff-002.jpg ← Gold Tipped Cane
    │   ├── staff-003.jpg ← Carved Heritage Staff
    │   └── staff-004.jpg ← Walnut Cane
    └── about/
        ├── hero-about.jpg
        ├── intro-image.jpg
        └── founder-franko.jpg
```

## How to Replace Images

Each placeholder shows the exact path it expects. For example:
- A placeholder showing `suits/suit-001.jpg` → add your image at `images/suits/suit-001.jpg`
- Update the `<img src="...">` tags in the HTML to point to the actual images

**Recommended image sizes:**
- Hero: 1200×1600px (portrait)
- Category cards: 600×800px (portrait)
- Product cards: 500×666px (portrait 3:4 ratio)
- About/Founder: 600×750px (portrait)

## Updating the WhatsApp Number

The number is stored in one place in `js/main.js`:
```js
const WHATSAPP_NUMBER = '2347068935733';
```
Replace `2347068935733` with the client's full international number (no + sign, no spaces).

## Updating Product Prices

Each product card uses `addToCart()` and `buyNow()` with the price as the second argument:
```html
onclick="addToCart('Product Name', 480, 'Suits', '')"
onclick="buyNow('Product Name', 480)"
```
Simply change `480` to the correct price. The currency symbol ($) is added automatically.

## Adding New Products

Copy any product card block in `shop.html` and update:
1. `data-category` → suits / shirts / shoes / accessories / sticks
2. `data-price` → numeric price
3. `data-name` → product name
4. The placeholder image path
5. The `addToCart()` and `buyNow()` function arguments

## Pages Summary

| Page       | Sections                                                            |
|------------|---------------------------------------------------------------------|
| index.html | Hero, Marquee Strip, Categories, Featured Products, Story, Testimonials + Footer |
| shop.html  | Header, Filter Tabs + All Products Grid + Footer                    |
| about.html | Hero, Intro, Values, Founder Story, Milestones + Footer             |
| contact.html | Header, Contact Form + Info, WhatsApp CTA, Social Links + Footer  |

## Features Included

- Cart sidebar with localStorage persistence
- Add to Cart + Buy Now buttons on every product
- Cart checkout directs to WhatsApp with full item list
- Buy Now opens WhatsApp with item name and price
- Contact form submits via WhatsApp
- Filter tabs by category on Shop page
- Sort by price / name on Shop page
- Scroll reveal animations on all sections
- Responsive mobile navigation
- Marquee text strip on homepage
- Social media placeholder links (update hrefs)

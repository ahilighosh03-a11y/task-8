Thala 7 - Sneaker Store E-Commerce Interface
A single-page, responsive e-commerce storefront interface built entirely with HTML5 and CSS3. The project utilizes CSS :has() and :target pseudo-classes to handle view switching natively in the browser without requiring JavaScript.

Project Structure
Plaintext
├── index.html   # Main structure containing the four functional views
└── style.css    # Typography, layout grids, components, and the routing engine
Features
No-JavaScript Single Page Architecture: Uses modern CSS :has() and :target selectors to hide and show different sections based on the URL hash.

4 Core Views:

Home (Landing Page): Minimalist hero layout featuring core branding, call-to-actions, and statistics overlays.

Shop (Product Display): Product presentation view featuring an image wrapper, detailed pricing, specific dimensions layout, and a scrollable product gallery.

Cart (Shopping Cart): Overview table managing item information, totals, coupon input structures, and a secure checkout portal layout.

Checkout (Payment Details): Input forms for client details, payment processing options, and card authorization details.

Component-Based CSS Architecture: Isolated global properties, variables, media queries, layouts, and components inside a dedicated stylesheet.

Responsive Layouts: Built with Flexbox and CSS Grid to dynamically adjust across desktop, tablet, and mobile breakpoints.

Setup & Running the Code
Download both index.html and style.css and place them inside the same directory on your computer.

Open index.html in any modern web browser (Chrome, Safari, Firefox, or Edge).

Use the navigation links in the header or button anchors to seamlessly toggle between the view blocks via the URL routing engine.

How the CSS Router Works
The single-page view transitions are managed strictly through standard CSS styles:

CSS
/* Hides all views by default */
.view-section {
    display: none;
}

/* Fallback: Displays the home view if no specific page id is set in the URL hash */
body:not(:has(.view-section:target)) #landing-view {
    display: block;
}

/* Displays the active section when its ID matches the active window hash */
.view-section:target {
    display: block;
}
Core Technologies & Dependencies
HTML5: Semantic architecture (<header>, <main>, <section>, <table>).

CSS3: Flexbox, CSS Grid, Custom Properties (--variables), and :has() relational selectors.

Google Fonts: Poppins (Weights 300, 400, 500, 600, 700).

FontAwesome: Scalable vector icons loaded directly from a public CDN.

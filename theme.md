# Theme Development Guide – Lyteforce Labs

## Theme Overview
- **Theme Base:** Understrap Version 1.2.4 (Bootstrap + Underscores hybrid)
- **Reason for Choice:** Provided a clean starter with Bootstrap integration and minimal styling, allowing us to build the Lyteforce Labs brand design from scratch.

## Features
- Custom homepage template with:
  - Full-width hero banner
  - Sustainability section with image and text overlay
  - Brand history section (visual timeline)
  - Partner logos grid
- Navbar modifications for centred menu and responsive scaling logo
- Full-width footer styling with bullet points removed
- Event listings page styling
- Additional CSS for mobile responsiveness and custom colour palette

---

## File Structure (Understrap v1.2.4)
understrap/

├── assets/

│ ├── css/ # Compiled CSS files

│ ├── js/ # JavaScript files

│ ├── sass/ # SCSS source files (Bootstrap + custom styles)

│ ├── fonts/ # Font files

│

├── inc/ # Theme setup, hooks, template functions

├── js/ # JS scripts for Bootstrap and custom theme functions

├── languages/ # Translation files (.pot, .mo, .po)

├── loop-templates/ # Template parts for post/page loops

├── page-templates/ # Custom page templates

├── woocommerce/ # WooCommerce template overrides (if used)

│
├── 404.php # 404 error template

├── archive.php # Archive page template

├── footer.php # Footer markup

├── front-page.php # Static homepage template

├── functions.php # Theme setup and enqueues

├── header.php # Header markup and navigation

├── index.php # Main blog template

├── page.php # Default page template

├── search.php # Search results template

├── sidebar.php # Sidebar markup

├── single.php # Single post template

├── style.css # Theme information + compiled CSS


---

## Colour Palette
- Primary: `#28a745` (Bootstrap Green – brand highlight)
- Secondary: `#FFFFFF` (White)
- Accent: `#FFCC00` (Gold hover)
- Black text for body content

---

## Typography
- Heading: Montserrat
- Body: Open Sans

---

## Custom CSS Styles

Below are the **additional CSS rules** added in WordPress (Customizer > Additional CSS) for Lyteforce Labs styling.

```css
:root {
    --gap: 2em;
}

/* ===== WordPress Structure Adjustments ===== */
#full-width-page-wrapper {
    padding: 0;
}

/* ===== Branding & Colours ===== */
.bg-primary {
    background-color: #28a745 !important; /* Bootstrap green */
}

.orange { color: orange; }
.blue { color: blue; }
.green { color: green; }

/* ===== Headings & Spacing ===== */
h2, .spacing {
    margin: var(--gap);
}

.entry-title {
    display: none;
}

/* ===== Navbar & Logo ===== */
.navbar-brand img {
    max-width: 100px;
    display: block;
}

.navbar-brand {
    margin-left: -70px;
}

.navbar-nav {
    display: flex;
    width: 100%;
}

.navbar-nav .nav-link {
    font-size: 20px;
    font-weight: bold;
    color: #ffff;
}

.navbar-nav .nav-link:hover {
    color: #ffcc00;
}

/* Menu text (overriding default) */
.nav-link {
    font-size: 1.1rem; 
    font-weight: bold;
}

/* ===== Product List Styling ===== */
.product-list .item {
    border: 1px #ddd solid;
    margin: 1em;
    text-decoration: none;
    color: #000;
}

.product-list .item .product-name {
    text-transform: uppercase;
    font-weight: bold;
}

.product-list .item .brand {
    font-size: 1em;
}

.product-list .item .category {
    font-size: 2em;
}

/* ===== Footer Styling ===== */
#wrapper-footer {
    background-color: #28a745;
    width: 100%;
}

.site-footer .site-info {
    text-align: center;
    color: #ffffff;
    font-size: 16px;
    font-weight: bold;
    padding: 20px 0;
}

.footer-menu {
    list-style: none;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
    gap: 20px;
}

.footer-menu li a {
    color: #ffffff;
    text-decoration: none;
    font-weight: bold;
    font-size: 16px;
    transition: color 0.3s ease;
}

.footer-menu li a:hover {
    color: #ffcc00; /* gold hover */
}

.page_item {
    list-style: none;
}

/* ===== Block & Image Styling ===== */
.wp-block-column {
    text-align: center;
}

.wp-block-column img {
    display: inline-block; /* Prevents full-width stretch */
}

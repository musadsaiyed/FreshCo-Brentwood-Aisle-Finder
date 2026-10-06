<div align="center">

# 🛒 Brentwood Aisle Finder

### Find products faster. Help shoppers with confidence.

**A responsive, searchable product-to-aisle directory for the FreshCo Brentwood store layout in Calgary, Alberta.**

[![GitHub Pages](https://img.shields.io/badge/Hosting-GitHub%20Pages-222?logo=github)](https://pages.github.com/)
![HTML5](https://img.shields.io/badge/HTML5-Frontend-E34F26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-Vanilla-F7DF1E?logo=javascript&logoColor=black)
![Responsive](https://img.shields.io/badge/Design-Mobile--Friendly-087F5B)
![Status](https://img.shields.io/badge/Status-Prototype-64748B)

**[Launch the live app](https://musadsaiyed.github.io/FreshCo-Brentwood-Aisle-Finder/)** · **[Report an issue](../../issues)**

<sub>Independent educational/portfolio project. Not affiliated with, sponsored by, or endorsed by FreshCo, Sobeys, or its affiliates. The live-app link assumes this repository is published under the GitHub account and repository name shown; update it if yours differs.</sub>

</div>

---

## Overview

**Brentwood Aisle Finder** helps store workers locate products without memorizing every shelf or searching through long product lists. Enter a product name, brand, or UPC and immediately see matching products and their **suggested aisle or store section**.

The project currently includes **1,742 verified-snapshot product records** from a collected product-listing snapshot. The database is **not a live inventory feed**, and the classifications are intended to be checked against the physical store layout.

## Features

| Feature | Description |
| --- | --- |
| 🔎 **Smart global search** | Searches all sections as soon as you type, even if another aisle was selected previously. |
| 🧭 **Aisle discovery** | Displays the assigned aisle or section on each matching product card. |
| 📱 **Mobile-first usability** | Responsive interface for Android, iPhone, tablets, and desktops. |
| 🧺 **Section filters** | Browse Aisles 1–9, Dairy, Produce, Meat, and Other. |
| 🏷️ **Product details** | View product name, brand, category, image (when available), and product link. |
| ✏️ **Aisle corrections** | Product locations are maintained centrally in the published data files. |
| 🚀 **Static deployment** | Runs on GitHub Pages without a backend, database, or paid hosting. |

### How search behaves

1. Type a query such as `rice`, `CRAVE`, or a UPC into **Find a product**.
2. The app automatically searches **all products** and displays matching results with location labels.
3. Optionally select a matching aisle/section filter to narrow the results.
4. Press **Enter** to scroll down to the matching product cards.
5. Clear the query to return to the full catalog.

> **Note:** Search shows the product's aisle/section; it does not physically navigate you through the store or open a map.

## Store layout

The location rules reflect a **user-supplied layout**, not an official planogram.

| Location | Main product groups |
| --- | --- |
| **Aisle 1** | International foods, rice, European, Middle Eastern, South Asian and Asian groceries |
| **Aisle 2** | Pasta and sauces, side dishes, Mexican/Latin American items, selected Asian foods, dumplings, samosas, specialty frozen items, **frozen fish and squid/seafood** |
| **Aisle 3** | **Frozen dinners and entrées**, CRAVE meals, lasagna, prepared pasta meals, pizza, desserts, frozen vegetables (with exceptions), fries and perogies |
| **Aisle 4** | Frozen fruit, ice cream, juices, yogurt and lassi |
| **Aisle 5** | Peanut butter, jams, honey, tea, coffee, hot cereal, gluten-free and selected packaged drinks |
| **Aisle 6** | Flour, baking supplies, soups, canned milk, sugar, spices, crackers and organic foods |
| **Aisle 7** | Food wraps, foil, facial tissues, disposable dishes, baby products and pet supplies |
| **Aisle 8** | Laundry, cleaning, dish detergent, hair care, soaps, body wash and skincare |
| **Aisle 9** | Chocolate, chips, bars, soft drinks, candy and ready-to-eat popcorn |
| **Dairy** | Milk, eggs, butter, cheese, sour cream, cream cheese, creamers and selected dairy alternatives |
| **Produce** | Fresh fruit and vegetables, packaged salads, prepared produce and selected tofu |
| **Meat** | Fresh meat, poultry, seafood, halal products and plant-based meat alternatives |
| **Other** | Products outside the named aisles and sections |

**Important exceptions:** CRAVE-brand prepared meals and comparable frozen dinners are assigned to **Aisle 3**; frozen fish, squid, calamari, shrimp and similar frozen seafood are assigned to **Aisle 2**. Fresh seafood belongs to **Meat**. Yogurt and lassi remain in **Aisle 4**. Product-specific placement may still need verification.

## Getting started

### Option A — Publish to GitHub Pages (recommended)

1. Create a **public** repository named `FreshCo-Brentwood-Aisle-Finder` on GitHub.
2. Upload the four files in this project directly to the repository's **root directory** (not inside an extra folder).
3. Commit your changes to the `main` branch.
4. Open **Settings → Pages → Build and deployment**.
5. Set **Source** to `Deploy from a branch`, **Branch** to `main`, and folder to `/ (root)`; click **Save**.
6. Wait for the Pages deployment to finish, then open the URL displayed in the Pages settings.

For the account `musadsaiyed` and the repository name above, the expected URL is:

```text
https://musadsaiyed.github.io/FreshCo-Brentwood-Aisle-Finder/
```

> The URL only works after GitHub Pages is successfully enabled. Replace the account or repository portion if your setup is different.

### Option B — Run locally

From the folder containing `index.html` and `products.json`, run:

```bash
python -m http.server 8000
```

Then open **http://localhost:8000** in your browser. You can also use the VS Code **Live Server** extension.

**Do not open `index.html` directly with `file://`**: browsers may block the JavaScript request to `products.json`.

## Project structure

```text
FreshCo-Brentwood-Aisle-Finder/
├── index.html             # Responsive UI, search, and section filters
├── products.json          # Product snapshot and default location assignments
├── aisle_assignments.csv  # Reference table for aisle classifications
└── README.md              # Project documentation
```

### Technology

- **HTML5 / CSS3** — layout and responsive styling
- **Vanilla JavaScript** — live search, aisle filtering, client-side rendering
- **JSON / CSV** — product records and aisle assignments
- **Static JSON data** — centrally maintained product assignments
- **GitHub Pages** — static website hosting

No framework, build step, server-side code, or API key is required to run the supplied website.

## Correcting product locations

1. Find the product using search or an aisle filter.
3. The updated location is saved **only in that browser**.

**Updating locations:** Modify the product's aisle in `products.json` and `aisle_assignments.csv`, then commit the updated files to GitHub. All users will see the revised data after deployment and refresh.

## Maintaining the catalog

The source data is a **point-in-time snapshot** and may not cover every product sold at the store. To update the website, replace the classified product data with a reviewed newer dataset, preserve the expected JSON fields, and commit the changes. Avoid publishing internal, confidential, or personal data.

## Known limitations

- **Not real-time:** No live stock, prices, or current product availability are displayed.
- **Not authoritative:** Locations are suggested and may differ from current shelf placement.
- **Internet required:** The current site is not a service-worker-enabled offline PWA. Hosting the data file alongside the app does **not** make it available offline.
- **External images:** Product images/links depend on third-party resources that may change or become unavailable.
- **Store specificity:** This layout is tailored to the described Brentwood location; it should not be assumed accurate for other FreshCo stores.

## Roadmap

- [ ] Validate product placements aisle by aisle against the physical store
- [ ] Add an administrator-reviewed shared corrections workflow
- [ ] Add automated validation for catalog updates and duplicate product IDs
- [ ] Improve category-specific matching and ambiguous-item review
- [ ] Explore an installable offline-capable Progressive Web App (PWA)

## Contributing

Suggestions, bug reports, and corrections are welcome through [GitHub Issues](../../issues). For a location correction, include the **product name**, **current displayed location**, **proposed location**, and an explanation where possible. Do not share confidential store information or customer data.

## Disclaimer

This is an **independent, unofficial portfolio/learning project**. FreshCo and related trademarks belong to their respective owners. Product information and imagery may be subject to third-party terms; confirm you have the appropriate rights or permissions before distributing the site publicly. Always verify shelf placement before directing a customer.

---

<div align="center">

**Built to make product lookup quicker, clearer, and more accessible on the shop floor.**

</div>

### Oreo product placement

All **19** Oreo-related products in the current snapshot are assigned to **Aisle 9**, including Oreo sandwich cookies, seasonal flavours, Oreo snack cakes and Oreo-branded protein bars. This version clears stale locally saved Oreo aisle overrides once on first load so earlier incorrect placements do not persist. Subsequent employee edits remain available.


## Store-specific updates

This version intentionally has **no Verify section, correction dropdowns, or correction-export button**. Product locations are maintained in `products.json` and `aisle_assignments.csv` and are updated through repository changes. Product locations reflect the **Brentwood, Calgary** layout only.

## Branding and independence

The website displays a FreshCo logo sourced from [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:FreshCo_logo.svg) for store identification. **This is an unofficial independent project, not affiliated with, sponsored by, or endorsed by FreshCo or Sobeys.** FreshCo is a trademark of its respective owner. The logo loads from Wikimedia Commons, so internet access is required for it to display.


## Aisle 2 international frozen product-family guides

The website includes **12 manually added product-family guides** for Deep frozen parathas, naan and roti, frozen vegetable burger patties, Ashoka frozen foods, frozen rasmalai, kaju katli, and similar sweets. These are **location guides, not verified FreshCo product SKUs**. No UPC, size, price, image, product URL, or inventory status is invented. The original 1,742 catalog records are preserved. When verified catalog records become available, replace these guides with individual product records and deduplicate.

### Brentwood bakery and naan placement

- **Bakery:** roti, sandwich bread, burger/hot dog buns, rolls, tortillas, pita, bagels, baguettes and other bread products, including the Deep Roti product-family guide.
- **Aisle 2:** naan, including the Deep Frozen Naan product-family guide.
- These are store-specific placements; generic product-family guides are not verified individual SKUs.

### Expanded bakery classification

Bread, buns, bakery rolls, tortillas, pita, bagels and related bread products in the existing catalog are mapped to **Bakery**. Naan and paratha remain in **Aisle 2**. Tortilla chips, breaded meats, spring rolls and egg rolls are excluded from the bakery rule.

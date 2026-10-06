<div align="center">

# FreshCo Brentwood · Aisle Finder

**Find the right product. Know the right section.**

An independent, mobile-friendly product-location directory designed around the **Brentwood, Calgary** store layout.

![Project status](https://img.shields.io/badge/Status-Active%20prototype-087F5B) ![Mobile](https://img.shields.io/badge/Interface-Mobile%20friendly-2563EB) ![JavaScript](https://img.shields.io/badge/JavaScript-Vanilla-F7DF1E?logo=javascript&logoColor=black) ![Hosting](https://img.shields.io/badge/Hosting-GitHub%20Pages-181717?logo=github)

**[View the website](https://musadsaiyed.github.io/FreshCo-Brentwood-Aisle-Finder/)** · **[View location changes](drinks_section_changes.csv)**

<sub>**UNOFFICIAL.** Independent project; not affiliated with, endorsed by, or operated by FreshCo, Sobeys, or their affiliates. The website link assumes the repository is published at the address above.</sub>

</div>

---

## At a glance

| | |
|---|---|
| **Store** | FreshCo Brentwood · Calgary, Alberta |
| **Catalog** | 1,774 searchable entries, including location-only guides |
| **Experience** | Mobile-friendly search with instant location labels and section filters |
| **Data model** | Static JSON snapshot; no real-time stock or pricing |

## The problem

Product locations vary between grocery stores. Even familiar brands can be difficult to find when similar items are split between frozen, international, bakery, beverage, and other departments. This project turns a store-specific location map into a quick-search reference for staff.

## What it does

- **Searches globally:** A product search is not restricted by the section selected earlier.
- **Shows a clear destination:** Each result displays its aisle or named store section.
- **Works on phones:** Responsive product cards and touch-friendly navigation for Android and iPhone.
- **Supports location exceptions:** For example, frozen seafood is in Aisle 2; frozen waffles are in Aisle 3; frozen berries are in Aisle 4.
- **Keeps updates auditable:** Assignment changes are maintained in the project data rather than edited by staff in the live website.
- **Runs as a static website:** HTML, CSS, JavaScript, and JSON; no account or server required for visitors.

## Brentwood store directory

| Location | Product groups |
|---|---|
| **Aisle 0** | Cooking oils, cooking sprays, vinegar, salad dressings, mayonnaise, mustard, ketchup, pickles, olives, relish, canned vegetables |
| **Aisle 1** | Rice, international groceries, European, Middle Eastern, South Asian and Asian foods |
| **Aisle 2** | Pasta, noodles, Mexican/Latin American foods, frozen fish and squid, dumplings, samosas, Deep/Ashoka frozen foods, naan and parathas |
| **Aisle 3** | Frozen dinners and entrées, CRAVE, pizza, frozen waffles, frozen vegetables, fries, perogies and frozen prepared meals |
| **Aisle 4** | Frozen berries and other frozen fruit, ice cream, yogurt, lassi and selected juices |
| **Aisle 5** | Peanut butter, jams, honey, tea, coffee, hot cereal, gluten-free foods and selected carton drinks |
| **Aisle 6** | Flour, baking ingredients, canned milk, soup, sugar, spices, crackers and organic foods |
| **Aisle 7** | Foil, food wraps, tissues, disposable dishes, baby supplies and pet products |
| **Aisle 8** | Laundry products, household cleaners, dish detergent, hair care, soap and skincare |
| **Aisle 9** | Chips, cookies including Oreo, chocolates, candy, snack bars and ready-to-eat popcorn |
| **🥤 Drinks** | Pop, soda, bottled and sparkling water, sports and energy drinks |
| **🥛 Dairy** | Milk, eggs, butter, cheese, sour cream, cream cheese and related products |
| **🥬 Produce** | Fresh vegetables, fruit, packaged salads, tofu and prepared produce |
| **🥩 Meat** | Meat, poultry, fresh seafood, halal and plant-based meat alternatives |
| **🍞 Bakery** | Bread, buns, roti, tortillas, pita and related bakery items |
| **Other** | Entries not confidently matched to a named store section |

### Important location distinctions

**Drinks** is separate from Aisle 9. Bottled water, pop, soda, sports drinks and energy drinks belong in Drinks; chips, candy and cookies remain in Aisle 9. **Juices, lassi, and other specialty drinks** keep their previously specified aisle locations rather than being indiscriminately moved to Drinks. **Ice cubes** are in the freezer by the tills near the exit, not in Aisle 3 or 4.

## Data and maintenance

The catalog was assembled from a limited product-listing snapshot and augmented with store-worker location rules and clearly identified product-family guides. Product entries do **not** establish current stock, shelf availability, prices, or the completeness of FreshCo's online catalog.

- `index.html` — responsive app, search, section navigation and product cards.
- `products.json` — searchable product records and store-specific location assignments.
- `aisle_assignments.csv` — tabular reference of current assignments.
- `sorting_changes.csv` — earlier full-catalog sorting audit.
- `README.md` — project overview and store layout reference.

**Location accuracy:** The named layout reflects information supplied for the Brentwood store. Some other assignments were inferred from category names; they are not an official planogram. Photo-reference and product-family guide entries are not verified individual SKUs.

## Technical design

```text
Search input → global product filtering → section labels → responsive product cards
                          ↑
                    products.json
```

The site uses plain HTML/CSS/JavaScript with no framework dependency. It is designed for static hosting through GitHub Pages. The application reads the JSON dataset on page load; product images and links may depend on external websites.

## Project scope and future improvements

Potential improvements include a shared, reviewed location-update workflow, catalog refreshes, offline support, and better coverage of products not included in the current snapshot. Changes should be validated against the actual Brentwood store layout before publication.

---

<div align="center"><sub>FreshCo Brentwood Aisle Finder · Independent, unofficial project · Product locations subject to change.</sub></div>

## Latest data quality update

- **Drinks** is a dedicated, populated section for bottled water, soda/pop, sparkling water, and energy/sports drinks.
- Removed the **Exit Freezer** navigation and its non-catalogued ice guide.
- Rechecked high-confidence Brentwood rules for frozen waffles, frozen berries, naan, roti, Oreo, CRAVE, condiments and frozen seafood.
- `final_corrections.csv` records changes made in this release.
- This is a store-specific, unofficial reference based on a partial product snapshot; exact placement of remaining items should be checked in store.

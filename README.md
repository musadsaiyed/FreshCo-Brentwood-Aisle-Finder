# FreshCo Brentwood — Aisle Finder

An **independent, unofficial** mobile-friendly product lookup built from a snapshot of FreshCo product listings and user-provided aisle descriptions. Not affiliated with or endorsed by FreshCo.

## Features
- Search by product, brand, category, UPC or product ID
- Browse aisles 1–9, plus **Other sections** and **Needs verification**
- Product pictures and FreshCo product links
- Local aisle corrections (stored only in your browser) and export corrections as CSV
- Offline-friendly data file committed with the site; no backend needed

## Publish using GitHub Pages
1. Create a new public GitHub repository (e.g. `freshco-brentwood-aisle-finder`).
2. Upload `index.html`, `products.json`, `aisle_assignments.csv`, and this `README.md` to the **root** of the repository.
3. Open repository **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch**, `main`, `/ (root)`, then **Save**.
4. Wait for GitHub Pages deployment. Visit the URL displayed in Settings → Pages.

## Run locally
Use VS Code Live Server or run `python -m http.server 8000` in this directory and visit `http://localhost:8000`. Directly opening `index.html` with `file://` may block fetching `products.json`.

## Important data limitations
- This is a **snapshot**, not live store inventory or verified prices/stock. Prices and stock status are deliberately not shown.
- Aisle assignments are **heuristics**, not verified store shelf locations. Check them against actual store signage.
- `Needs verification` products are not assigned by guess. `Other sections` means outside the supplied aisles 1–9.
- Local corrections are only saved on that browser; download CSV and incorporate into your master data to share corrections with all employees.
- Use the site for internal assistance only as permitted by your workplace; verify permission before public deployment of store-specific information or product imagery.

## Update data
Replace `products.json` with a newly classified dataset and commit. Existing local corrections are keyed by product ID.

## Phone compatibility

The website uses a responsive layout for iPhone and Android browsers. Search, aisle filters, product cards and aisle corrections are touch-friendly. Upload all files to the root of the GitHub repository and open the GitHub Pages URL on a phone. Changes made to aisle assignments are stored locally in each device/browser, not synchronized between employees.


## Dairy section (separate from aisles 1–9)
The **Dairy** filter includes milk, eggs, butter, margarine, block/shredded/sliced/cream cheese, sour cream, refrigerated creamers and related dairy alternatives according to the product category. Yogurt and lassi remain in Aisle 4 as specified. This is a suggested classification: some cheese, dips, plant-based products, and shelf-stable creamers may be merchandised elsewhere; verify in store. Existing corrections stored on a device take priority over new default assignments; clear or update those corrections to see the new defaults.

## Additional store sections

- **Produce:** fresh fruit and vegetables, packaged salads, cut produce, and refrigerated tofu where identifiable.
- **Meat:** meat, poultry, seafood, halal meats, and plant-based meat alternatives.
- Specialty frozen fish and sausages already assigned to **Aisle 2** remain there where applicable; frozen meals and samosas retain their designated aisle.
- Product placement is heuristic; confirm actual shelf locations in-store. Corrections are device-local and can be exported.

## Confirmed frozen seafood placement
Frozen fish, squid, calamari, shrimp, prawns, mussels, clams, scallops, crab, lobster and related frozen seafood are assigned to **Aisle 2**, even when the online department is Seafood. Fresh (not frozen) seafood remains in Meat & Seafood. Products incorrectly tagged under Frozen Seafood are not moved solely based on that category.

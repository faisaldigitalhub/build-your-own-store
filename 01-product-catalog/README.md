# Step 01 — Product Catalog

**One concept:** data vs. design. A store page is a *template*. The products are *data*. Change the data, and the whole shop changes — without touching the design.

## What you build

A shop page that shows 8 demo products in three categories (Bakery, Boutique, Beauty) with buttons to filter by category.

## How to run it

1. Open `index.html` in your browser (double-click it).
2. Click a category button — Bakery, Boutique, or Beauty — and watch the list change.
3. To change the products, edit `products.js` and reload the page. The shop changes without touching the design.

## How it works

- `products.js` holds the products: each one has an `id`, `name`, `category`, `price`, and `description`. It is loaded with a plain `<script>` tag, so it works when you double-click the file and when you serve the folder.
- `index.html` reads that list and builds one card per product with JavaScript. No product is written by hand in the HTML.
- The filter buttons only change which products are shown — the data never changes.
- Products you add in Step 05 (Admin) are read from the browser and shown here too.

## Try it yourself

- Add a 9th product to `products.js` (copy one line, change the values) and reload.
- Add a new category, for example `"Electronics"`, and give two products that category. A new filter button appears by itself — why?

## Challenge

Change all 8 products to products from *your* shop (or a shop you know). Keep the same format: name, category, price, description. If your shop only has one category, use one category — the filter still works.

> All prices here are demo prices in PKR, for learning only.

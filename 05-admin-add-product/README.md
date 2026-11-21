# Step 05 — Admin: Add a Product

**One concept:** create, read, and delete. A shop owner needs to add products without editing code. This page does the "create" and "delete" part; Steps 01, 02, and 04 do the "read" part. Together they are the whole admin job.

## What you build

A small admin page: a form (name, category, price, description) that adds a product, a list of the products you added, and a delete button for each one.

## How to run it

1. Open `index.html` in your browser.
2. Add a product — for example, Mango Jam, Bakery, 600, "Homemade mango jam, 250 g."
3. Now open Step 01 (Product Catalog). Your product is there. Open Step 04 and search for it. Open Step 02 and add it to the cart.

## How it works

- Added products are saved in `localStorage` under the key `byos-custom-products`, as a list of product objects — the same shape as the products in Step 01.
- Steps 01, 02, and 04 each read that list and add it to their own products before showing the shop. That is why one admin page feeds three shop pages.
- Each added product gets `id: Date.now()` — the current time in milliseconds — so every product has a unique id without a server.
- Delete removes the product from the saved list and re-draws the page.

## The honest limit

This admin page saves products only in *your* browser. Another visitor on another device will not see them. A real shop saves products on a server or a database so every visitor sees the same shop. That is the next level — but the form, the validation, and the list you just built are exactly the same shape a server version uses.

## Try it yourself

- Add a product, close the browser completely, reopen it, and come back here. Is your product still listed? (That is localStorage doing its job.)
- Delete a product, then check Step 01. Is it gone there too?

## Challenge

Add an "Edit price" button next to each product: clicking it asks for a new price (with `prompt()`), saves it, and re-draws the list. That is the last missing admin job — update.

> All prices here are demo prices in PKR, for learning only.

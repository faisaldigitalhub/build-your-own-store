# Step 04 — Search and Sort

**One concept:** filter, then sort. Finding a product in a list is two small jobs: first keep only the products that match, then put them in order. Do them in that order, every time.

## What you build

A shop page with a live search box and a sort menu (name A–Z / Z–A, price low–high / high–low). The list updates as you type.

## How to run it

1. Open `index.html` in your browser.
2. Type `cake` in the search box — the list shrinks as you type.
3. Clear it, then change the sort to "Price: high to low". The most expensive product comes first.

## How it works

- **Filter** uses `.filter()` and `.includes()`: a product stays in the list only if its name or category contains the search text (compared in lowercase, so "Cake" and "cake" both match).
- **Sort** uses `.sort()` with a small compare function: for prices, `a.price - b.price` sorts low to high; for names, `localeCompare` sorts A to Z.
- The code copies the list (`[...shown]`) before sorting, so the original product list is never reordered by accident.
- Products added in Step 05 (Admin) are searchable and sortable here too.

## Try it yourself

- Search for `beauty`. How many products match, and why?
- Sort by price low to high. Which product is first? Is that what you expected?

## Challenge

Add a category dropdown next to the search box (like the filter buttons in Step 01), so a visitor can search *and* filter by category at the same time. Which runs first in your code — the search or the category filter — and does the order matter?

> All prices here are demo prices in PKR, for learning only.

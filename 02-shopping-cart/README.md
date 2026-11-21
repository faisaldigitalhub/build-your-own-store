# Step 02 — Shopping Cart

**One concept:** state. A cart is not a page — it is a small list the browser remembers: *which product, how many*. Everything on the screen is drawn from that list.

## What you build

A shop with an "Add to Cart" button on every product, a cart panel that shows each item, + / − buttons to change quantity, a remove button, and a running total.

## How to run it

1. Open `index.html` in your browser.
2. Add a few products. Change quantities with + and −. Remove one with ✕.
3. **Reload the page.** The cart is still there — that is the point of this step.

## How it works

- The cart is one JavaScript object: `{ productId: quantity }`. For example `{ "1": 2, "5": 1 }` means 2 × Chocolate Cake and 1 × Face Wash.
- The cart is saved in `localStorage` under the key `byos-cart`. `localStorage` is storage built into the browser — it survives a reload and is only on the visitor's own device.
- Every button re-draws the cart from that object, so the screen and the saved cart can never disagree.
- Products added in Step 05 (Admin) appear here too, because this page reads them from `localStorage`.

## Try it yourself

- Open the browser console and type `localStorage.getItem("byos-cart")`. You will see the cart as text.
- Add the same product twice. What happens to the quantity instead of adding a second line? Why is that better?

## Challenge

Add a delivery fee of Rs. 200 (demo) that only appears when the cart is not empty, and show it as its own line above the total. Where in the code does the total get calculated?

> All prices here are demo prices in PKR, for learning only.

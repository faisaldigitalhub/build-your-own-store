# Step 03 — Checkout via WhatsApp Order

**One concept:** no backend needed. A small shop does not need a payment gateway to take its first orders. The order can travel as a *message* — the customer fills a form, and the shop gets a ready-made WhatsApp message.

## What you build

A checkout page that reads the cart from Step 02, asks for name, address, and city, and builds a WhatsApp order message with a "Send Order on WhatsApp" button.

## How to run it

1. First go to Step 02 and add some products to the cart (this page reads the same saved cart).
2. Open `index.html` in this folder.
3. Fill in the delivery details and the shop's WhatsApp number, then click **Build WhatsApp Order**.
4. Read the preview, then click **Send Order on WhatsApp** — it opens WhatsApp with the message ready to send.

## How it works

- The cart is shared with Step 02 through `localStorage` (key `byos-cart`). Two different pages, one saved cart.
- The message is built as plain text: one line per item, then the total, then the customer details.
- `encodeURIComponent()` turns that text into a safe web link: `https://wa.me/<number>?text=<message>`. WhatsApp opens with the message already typed.
- Nothing is sent, saved, or charged by this page. The order only exists once the customer presses send in WhatsApp, and the shop confirms it in chat.

## Try it yourself

- Leave the name empty and click the button. What happens? (Good forms check their inputs before building the message.)
- Order 3 × Chocolate Cake and check the total in the preview. Does it match Step 02?

## Challenge

Add a "Payment method" choice to the form — Cash on Delivery or Bank Transfer — and include the choice in the WhatsApp message. Cash on Delivery is how most Pakistani online orders are paid.

> All prices here are demo prices in PKR, for learning only. No real payment is taken.

# Side Quest Planner

Tell it the trip like you'd text a friend ("It's my 30th, 4 of us, New York in May, active stuff, partying, good food, around $300 each") and it plans the days around live LivingSocial deals: it reads the fine print, puts each stop on a day it's valid, routes each day on a map and fills one cart.

Live: https://antonellamasini.github.io/side-quest-planner/

Built for the LivingSocial Side Quest (Build It track) by Antonella Masini Ortiz.

## How it works

- One static page, no backend, no API key. The browser calls the public LivingSocial agent API (`https://api-core.livingsocial.com/ls_agent_api`): `offers/search` (including `near` searches for swaps) and `offers/{id}`.
- Every offer, price, place and rule comes from the API. Nothing is invented.
- "Add to cart" uses each option's buy link with the group quantity; the links add to one LivingSocial cart and the person pays on Groupon's checkout.
- Fine-print rules it schedules around: weekday-only, single-day-only, weekend-only, 21+, dated events, and voucher validity (it shows the earliest day to buy each voucher for the trip).
- Globe: d3 + world-atlas / us-atlas (Natural Earth). Street map: Leaflet + OpenStreetMap tiles.

Buying a voucher doesn't reserve a date or time; book with the merchant after you buy.

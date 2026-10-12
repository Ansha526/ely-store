# ELY Atelier storefront

A complete static fragrance-store demonstration inspired by elyscents.pk. This is an independent concept, not an exact reproduction or an official Elyscents store. All catalog names, prices and illustrations are sample content. The project uses HTML, CSS and vanilla JavaScript, not React or Vite. It needs no Railway, backend service, database, API key or third-party package.

## Included

- Responsive home page and mobile navigation
- 12 sample products with original local SVG illustrations
- Collection pages, category filtering, search and price/name sorting
- Individual product pages with quantity selection and related products
- Cart with add/remove/update quantities and browser-local persistence
- Explicitly labeled demo checkout and order-summary preview
- Story, FAQ, contact setup, privacy and delivery/returns pages
- Keyboard focus styles, semantic navigation and native modal dialogs
- Vercel configuration and dependency-free build

## GitHub se Vercel par deploy karein

1. ZIP extract karein. `ely-store` folder kholein.
2. GitHub par new repository banayein, phir **Add file → Upload files**.
3. `ely-store` ke **andar ki files** repository root mein upload karein. `package.json` root par nazar aana chahiye.
4. Commit changes karein. No secrets are included. GitHub web upload may omit `.gitignore`; create it manually if needed.
5. Vercel → **Add New → Project** → repository import karein.
6. Framework Preset: **Other** (this project is not Vite).
7. Root Directory: **./**. Agar aapne outer `ely-store` folder upload kiya hai, Root Directory **ely-store** set karein.
8. Build Command: **npm run build**. Output Directory: **dist**.
9. Environment Variables: **none**. Railway connect na karein.
10. **Deploy** dabayein. Vercel successful deployment ke baad live `.vercel.app` URL dega.

`vercel.json` already sets build/output configuration. Hash routes (such as `/#product/amber-noir`) work on refresh without SPA rewrite rules.

## Run locally

Install Node.js 20 or later, open the extracted project folder in a terminal:

```bash
npm run dev
```

Open http://localhost:3000. No `npm install` is necessary because there are no dependencies.

```bash
npm run build
```

The build creates `dist/` with the complete deployable site. Alternatively deploy `dist/` as static output.

## Customize

- `app.js`: sample `products` array, product names, prices, descriptions, categories and informational pages
- `styles.css`: colors, typography and responsive layout
- `index.html`: logo, navigation, footer and page metadata
- `assets/`: replace original illustrations with licensed product images. Update `image()` in `app.js` if changing file extensions.
- The name/logo ELY Atelier is placeholder branding. Replace it with a brand you are authorized to publish.
- No external font or image network requests are used.

## Demo boundaries / real ecommerce

Cart contents (only product IDs and quantities) persist in localStorage, when browser storage is allowed. No real order, email, delivery, payment, account, inventory, customer database or admin system exists. Checkout is explicitly a preview and does not send or persist entered personal details. Use fictional details.

To accept real orders, connect a secure checkout/order service or Vercel server functions with durable storage. Never trust browser prices for payment totals; validate product IDs, quantities and pricing on the server. Never put secret payment/API keys in frontend source. Add verified contact, shipping and return policies before commercial use.

## Verification

The source JavaScript syntax, build and packaged asset references were checked. Browser rendering and your Vercel deployment should be reviewed after upload. This ZIP is not already deployed; you create the live URL through Vercel.

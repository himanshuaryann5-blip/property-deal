# Property Deal — Real Estate Website

A responsive React + Vite + TypeScript website for Property Deal, Faridabad. Includes a centered responsive wordmark, property search/filtering, sample property cards and detail/gallery modal, visit-request WhatsApp handoff, seller lead form, EMI calculator, FAQ accordion, contact CTAs, and responsive layouts.

## Important before launch

- The property inventory in `src/data/properties.ts` is **illustrative demo content only**. Prices, localities, specs and availability are not verified. Replace it with owner-confirmed listings before publishing.
- Customer testimonials are deliberately not fabricated. Replace the preview with authentic, permission-approved reviews.
- Google Maps link is a directions/search link based on the supplied location reference; confirm the exact address/pin before publishing.
- Form submissions open WhatsApp with a prefilled message for the visitor to review and send. This static frontend does not save leads to a database or CRM. A backend/CRM integration is needed for automatic lead storage.
- Images use remote Unsplash image URLs. Replace with appropriately licensed owner-provided or licensed images for production and consider downloading/optimizing assets locally.
- Confirm the supplied phone, email, address, Google rating and experience claims before publishing.

## Requirements

Node.js 20+ recommended.

## Run locally

```bash
npm install
npm run dev
```

Open the local URL shown by Vite.

## Production build

```bash
npm run build
npm run preview
```

The generated site is in `dist/`.

## Push to GitHub

Create an empty repository on GitHub, then run these commands from this folder:

```bash
git init
git add .
git commit -m "Build Property Deal website"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
git push -u origin main
```

Replace the remote URL with your repository URL. Do not commit credentials or private customer information.

## Deploy to Vercel

1. Push the repository to GitHub.
2. In Vercel, choose **Add New → Project** and import the repository.
3. Framework preset: **Vite**. Build command: `npm run build`; output directory: `dist`.
4. Deploy. `vercel.json` provides an SPA rewrite for deep links.
5. Replace `YOUR-DOMAIN.example` in `public/robots.txt` and `public/sitemap.xml` with the real domain. Set a canonical URL and production Open Graph metadata when the domain is known.

No environment variables are required for the current static implementation.

## Update sample property data

Edit `src/data/properties.ts`. Each property includes an ID, slug, title, purpose, type, city, locality, price, optional bedrooms/bathrooms/area, description, image gallery, featured flag, and a `sample` marker. Keep `purpose` as `Buy` or `Rent`. Replace sample images and all illustrative fields with confirmed property information. For a live inventory/CMS, replace this local array with a typed API data layer and add secure server-side lead handling.

## Features / limitations

- Property filters are functional against local demo data; location, type, budget, bedrooms and text search update visible results.
- Property detail modal has next/previous gallery navigation.
- EMI calculator uses the standard reducing-balance formula and supports zero interest.
- Seller and visit forms validate basic required details and hand off to WhatsApp. The site does not claim that a visit is booked or a lead is stored.
- Favourites are local UI state only and are not persisted.
- No real-time inventory, CMS, CRM, booking calendar or Google reviews integration is connected.

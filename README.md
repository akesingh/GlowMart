# GlowMart

Premium beauty & cosmetics e-commerce marketplace built with **Next.js**, **TypeScript**, and **Tailwind CSS**.

GlowMart is an original brand experience inspired by leading beauty shopping flows — elegant rose/blush accents, generous whitespace, and fully interactive browsing, search, cart, wishlist, and checkout.

## Features

- Responsive homepage with hero, categories, trending / bestsellers / new arrivals, deals, brands, blog, trust strip, and newsletter
- Product listing with filters (category, brand, price, rating) and sorting
- Product detail pages with gallery, shades/sizes, reviews, and related products
- Search with autocomplete suggestions
- Shopping bag and wishlist (persisted in local storage)
- Multi-step checkout (bag → address → payment → review)
- Mobile header, mega-menu, and bottom navigation
- Skeleton loaders, empty states, toast notifications, SEO metadata

## Getting started

```bash
npm install
npm run dev -- --port 3456
```

Open [http://localhost:3456](http://localhost:3456).

## Scripts

| Command | Description |
|---------|-------------|
| `npm run dev` | Start development server |
| `npm run build` | Production build |
| `npm start` | Start production server |
| `npm run lint` | Run ESLint |

## Architecture

- `src/data` — mock catalogs (products, brands, categories, blogs, reviews)
- `src/services` — API-ready service layer over mock data
- `src/store` — Zustand cart & wishlist state
- `src/components` — reusable UI, layout, product, cart, checkout modules
- `src/app` — Next.js App Router pages

Mock data is separated from UI so services can later point at real APIs without rewriting components.

## Stack

- Next.js 16 (App Router)
- React 19
- TypeScript
- Tailwind CSS 4
- shadcn/ui
- Zustand + Sonner

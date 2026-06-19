# Aboki Frontend

The official marketing and product website for **Aboki** — an API-first platform powering fast, secure stablecoin-to-fiat infrastructure for businesses across Nigeria, Kenya, and beyond. This repository contains the public-facing Next.js site: landing page, use cases, and developer-facing sections that introduce partners to the Aboki platform.

🔗 **Live site**: https://aboki.xyz
🚀 **Frontend (this repo) deployment**: https://aboki-frontend.vercel.app/
📚 **API Docs**: https://docs.aboki.xyz

## About Aboki

Aboki gives remittance companies, e-commerce platforms, fintech startups, and enterprises a single, developer-friendly API to move value between stablecoins (USDC, USDT) and local fiat currencies (NGN, KES, and more) — without building offramp infrastructure themselves. The goal is integration in a day, not months.

Aboki is built **multi-chain from the ground up**, with native support for both **EVM networks** and **Stellar**. This lets partners settle stablecoin transactions on whichever chain best fits their users — low-cost, fast-finality rails on Stellar, or broad ecosystem compatibility across EVM chains — through one unified API rather than juggling separate integrations per chain.

This frontend is where prospective partners and developers first encounter the product: what it does, which chains it supports, who it's for, and how to get started.

## Key Sections / Features

- **Hero** — Primary value proposition and call-to-action for new visitors.
- **Trusted By** — Social proof showcasing partners and businesses using Aboki.
- **Use Cases** — Real-world applications of the platform (remittances, treasury management, payouts, e-commerce settlement), with a dedicated `/use-cases` page for deeper detail.
- **Developer-Centric Section** — Highlights the API-first, multi-chain approach, built for engineering teams evaluating integration.
- **Header / Footer** — Global navigation, links to docs, and company information.

## Supported Networks

Aboki's infrastructure spans two ecosystems so partners aren't locked into a single chain:

| Network | Role |
|---|---|
| **EVM Chains** | Stablecoin (USDC/USDT) liquidity and settlement across EVM-compatible networks (e.g. Ethereum, Polygon, and other supported chains). |
| **Stellar** | Native Stellar DEX and payment-rail integration for fast, low-cost stablecoin settlement, including anchor-based on/off-ramping. |

The frontend's developer-facing copy and use-case examples are written to reflect this dual-chain capability — partners can pick the network that best matches their users' needs, accessed through Aboki's single unified API rather than separate per-chain integrations.

> Update the table above with the exact EVM chains currently live in production if you'd like the README to list them by name (e.g. Ethereum, Base, Polygon).

## Tech Stack

- **Framework**: [Next.js](https://nextjs.org) (Pages Router)
- **Library**: React
- **Language**: JavaScript / JSX
- **Styling**: CSS (`styles/globals.css`)
- **Fonts**: [`next/font`](https://nextjs.org/docs/pages/building-your-application/optimizing/fonts) with [Geist](https://vercel.com/font)
- **Deployment**: [Vercel](https://vercel.com)

> If your project also uses a CSS framework (e.g. Tailwind), a component library, or analytics tooling, add those here — they weren't visible in the file tree I worked from.

## Project Structure

```
aboki-frontend/
├── components/
│   ├── DeveloperCentricSection.js   # API/developer value proposition
│   ├── Footer.js                    # Site footer
│   ├── Header.js                    # Site navigation
│   ├── Hero.js                      # Landing page hero section
│   ├── TrustedBySection.js          # Partner/social proof logos
│   ├── UseCase.js                   # Single use-case card/component
│   └── UseCasesSection.js           # Use cases overview section
├── pages/
│   ├── api/                         # Next.js API routes
│   ├── _app.js                      # Custom App component
│   ├── _document.js                 # Custom Document component
│   ├── index.js                     # Home page
│   └── use-cases.jsx                # Dedicated use cases page
├── public/
│   ├── dashboard.svg                # Product dashboard preview asset
│   ├── logo.svg                     # Aboki logo
│   ├── usdc.svg / usdt.svg          # Supported stablecoin icons
│   ├── ngn.svg / us.png / ke.png    # Supported currency/region icons
│   └── ...                          # Other static assets (favicon, vercel, next, etc.)
└── styles/
    └── globals.css                  # Global styles
```

## Getting Started

### Prerequisites

- Node.js 18+
- npm, yarn, pnpm, or bun

### Installation

```bash
# Clone the repository
git clone https://github.com/BernardOnuh/aboki-frontend.git
cd aboki-frontend

# Install dependencies
npm install
# or
yarn install
# or
pnpm install
# or
bun install
```

### Run the development server

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `pages/index.js`. The page auto-updates as you edit the file.

[API routes](https://nextjs.org/docs/pages/building-your-application/routing/api-routes) can be accessed on [http://localhost:3000/api](http://localhost:3000/api). These live in `pages/api/` and are mapped to `/api/*` instead of being treated as React pages.

## Environment Variables

Create a `.env.local` file in the project root for any local configuration (e.g. analytics keys, API base URLs used by the developer-centric section). Example:

```env
NEXT_PUBLIC_API_BASE_URL=https://docs.aboki.xyz
NEXT_PUBLIC_SITE_URL=https://aboki.xyz
```

⚠️ Never commit `.env.local` — use `.env.example` for templates only.

## Available Scripts

```bash
npm run dev      # Start development server with hot reload
npm run build    # Build for production
npm run start    # Run the production build
npm run lint     # Run ESLint
```

## Design Assets

The `public/` directory includes brand and currency iconography used throughout the site, including support indicators for **USDC**, **USDT**, **NGN**, **KES**, and **USD** — reflecting the markets and stablecoins Aboki currently supports.

## Contributing

1. Fork the repository
2. Create your feature branch: `git checkout -b feature/your-feature-name`
3. Make your changes and test locally with `npm run dev`
4. Commit with a clear message describing the change
5. Push to your fork and open a Pull Request

### Reporting Issues

Found a bug or broken section on the site? Open an issue with:
- A clear description of the problem
- Steps to reproduce
- Expected vs. actual behavior
- Browser/device details if relevant

## Deploy on Vercel

This frontend is deployed on Vercel at **https://aboki-frontend.vercel.app/**.

The easiest way to deploy your own instance is via the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme).

Check out the [Next.js deployment documentation](https://nextjs.org/docs/pages/building-your-application/deploying) for more details.

## Learn More

- [Next.js Documentation](https://nextjs.org/docs) — learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn-pages-router) — an interactive Next.js tutorial.
- [Aboki API Docs](https://docs.aboki.xyz) — integrate with the Aboki platform.

## License

[Add your license here — e.g. Proprietary, MIT]

## Contact

- 💼 Business inquiries: [add email]
- 🛠️ Developer support: [add email]

---

**Maintainer**: [@BernardOnuh](https://github.com/BernardOnuh)
# Novarift — Project Context for Claude Code

## What is this
Novarift is a tech agency website based in Canada.
One single HTML file (index.html) — no framework, no build step.
Deploy on Vercel. Domain: novarift.ca

## Stack
- HTML + CSS + JavaScript vanilla (everything inline in one file)
- Google Fonts only (Cormorant Garamond + Syne + DM Mono)
- No npm, no webpack, no React, no dependencies
- Hosted on Vercel (static)

## Design system
Background:  #080A0F
Gold accent: #C8A96E
Gold light:  #E2C99A
Gold dark:   #8B6F3E
White:       #F0EDE8
White muted: rgba(240,237,232,0.6)
Border:      rgba(200,169,110,0.15)

Fonts:
- Headings: Cormorant Garamond (serif, elegant)
- UI/Nav/Labels: Syne (sans-serif, modern)
- Code/Tags/Mono: DM Mono (monospace)

## Architecture rules
1. Everything in ONE file — index.html
2. CSS in <style> tag at the top
3. JS in <script> tag at the bottom
4. No inline styles except rare dynamic values
5. Portfolio projects stored as JSON array in JS — never hardcoded in HTML

## Sections (in order)
1. Nav — logo + links + CTA button
2. Hero — full viewport, big title, description, 2 CTA buttons
3. Marquee — animated service names strip
4. Services — 6 cards in 3x2 grid
5. Numbers — 4 stats
6. Work/Portfolio — cards from JSON array
7. Process — 4 steps + sticky visual
8. Pricing — 3 tiers
9. CTA section — contact
10. Footer

## Content rules
- Language: English (site), French OK in comments
- Location: "Canada" only — never "Montreal" or any city
- Tagline: "Based in Canada · Est. 2025"
- Email: hello@novarift.ca
- No fake phone number

## Portfolio JSON format (ALWAYS use this structure)
```js
const projects = [
  {
    id: "001",
    name: "MamaShop",
    category: "SaaS · Africa",
    year: "2026",
    desc: "Complete digital management system for wholesale traders in West Africa.",
    stack: ["Supabase", "Claude API", "n8n", "WhatsApp API"],
    featured: true
  }
]
```
To add a project: add one object to the array. Never touch the HTML.

## Animations
- Custom gold cursor (dot + lagging ring)
- Reveal on scroll (IntersectionObserver)
- Nav fills on scroll (backdrop-filter + border)
- Marquee infinite scroll
- Service cards: bottom border slides in on hover
- Work cards: subtle gold gradient on hover

## What must work
- All anchor links (#services, #work, #process, #pricing, #contact)
- mailto: on CTA email button
- Lighthouse score > 90 mobile
- Responsive at 360px and 1440px

## What to NEVER do
- No lorem ipsum
- No placeholder images (use CSS gradients or geometric shapes)
- No "Montreal to the world" or city names
- No inline event handlers (onclick="") — use addEventListener in JS
- No framework suggestions
- Never break the one-file rule

# HANDOFF PROMPT — J&J Real Estate Group Website

> Give this entire document to any AI assistant (Claude, ChatGPT, etc.) or human developer, together with `index.html` and the `assets/` folder, and they will have everything needed to maintain, improve, or rebuild this website.

---

## The Prompt

You are working on the official website of **J&J Real Estate Group**, a luxury real estate team at **Capstone Realty** serving **Huntsville and North Alabama**. The team is **Chrystal Justice** (256-503-1924, Chrystal@choosecapstone.com — strategic, analytical, negotiation-focused) and **Patsy Jenkins** (270-881-7622, Patsy@choosecapstone.com — patient, detailed, education-focused). Combined experience: 15+ years.

**Brand:** black-and-gold luxury. Tagline: "Exceptional Properties. Extraordinary Results." The brand voice is emotional and persuasive — clients buy feelings first (certainty, calm, exclusivity, leverage) and justify with logic after. Copy should always sell confidence, privacy, strategy, and results. Money and outcomes matter more than features. Never make it feel cheap, loud, or generic — it must read like a private wealth firm, not a discount brokerage.

**Design system (all in `index.html`, single file, no build step):**
- Colors: background near-black `#0a0a0a`, panels `#161618`, gold `#c6a35d`, light gold `#e3c98a`, cream text `#f5f1e8`
- Fonts: Cormorant Garamond (headings, Google Fonts) + Inter (body)
- Reference inspiration: Sotheby's Realty, JamesEdition, Forbes Global Properties, Cotino/Storyliving by Disney

**Signature features already built (preserve them all):**
1. Cinematic preloader — gold J&J mark + growing line, fades after load
2. Hero flashlight — the dark hero image is revealed by a spotlight that follows the mouse 1:1 with zero lag (`.hero-light`, radial CSS mask, `--fx/--fy/--fr` variables, disabled on touch devices)
3. Headline line-reveal animation (`.hl` spans)
4. Gold scroll progress bar (`#prog`)
5. Custom gold cursor: dot + expanding ring on hover, desktop only
6. Parallax hero background tied to scroll
7. Animated stat counters (15+ years, 2 advisors, 7-step journey)
8. "The J&J Difference" comparison table (J&J vs typical agent)
9. 3D tilt on the two advisor cards
10. Property gallery with full-screen lightbox (arrows + keyboard)
11. Communities marquee: Huntsville · Madison · Athens · Decatur · Owens Cross Roads · Meridianville · Hazel Green · Harvest
12. Film-grain overlay, scroll-reveal animations (`.rv` + IntersectionObserver)
13. Contact form → opens email to Chrystal, cc Patsy (mailto)
14. Fully responsive; heavy effects disabled on touch/mobile

**Page order:** Hero → Stats → Positioning → Advisors → J&J Difference → Sellers (+3-step pricing) → Gallery → Buyers → New Construction/Investor/Relocation → Client Journey (7 steps) → Testimonial (Bri Bolling, verified Google review) → Communities marquee → Community involvement (Free 2 Teach backpack drive, Manna House, Food Bank of North Alabama) → Communication Promise → Contact → Footer (Capstone Realty, REALTOR®, Equal Housing logos).

**Owner preferences (important):**
- No bilingual/EN-ES messaging anywhere
- The site must feel: locked-in, fancy, modern, intelligent, futuristic — always better than competitor sites
- Emotional persuasion in copy is desired; frame everything around client money, leverage, and results
- Dark hero image stays dark; the flashlight reveals it

**Deployment:** GitHub Pages, deploy from `main` branch root. No build step — pushing `index.html` + `assets/` is the release.

**Top requested future upgrades (in priority order):**
1. Featured Properties / live listings section (MLS/IDX via Capstone Realty when available)
2. Contact form wired to a real backend (e.g., Formspree/Netlify Forms) instead of mailto
3. SEO: JSON-LD RealEstateAgent schema, Open Graph tags, sitemap; target "Huntsville luxury real estate"
4. Custom domain
5. More verified testimonials as they come in

---

## File Map

| File | Purpose |
|---|---|
| `index.html` | Entire site — CSS in `<style>`, JS in `<script>` at bottom |
| `assets/chrystal.jpg` | Chrystal Justice headshot (dark hair) |
| `assets/patsy.jpg` | Patsy Jenkins headshot (blonde) |
| `assets/logo.jpg` | J&J gold-on-black team logo |
| `assets/capstone-logo.jpg`, `realtor.png`, `eho.png` | Footer compliance logos |
| `assets/living-dusk.jpg` | Hero image (also flashlight layer) |
| other `assets/*.jpg` | Gallery / section / community images |

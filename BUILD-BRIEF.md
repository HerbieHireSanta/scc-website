# SCC Website Build Brief

## Project
Build out all HTML pages for SantaClausandCompany.com redesign.

## Design System
- Homepage: `/Users/openclaw/.openclaw/workspace/scc-website/index.html`
- Interior template: `/Users/openclaw/.openclaw/workspace/scc-website/_interior-template.html`
- All pages must use the EXACT same nav, footer, CSS variables, and font imports as those files.

## CSS Variables (copy exactly into every page)
```
--green: #1c3a28
--green-mid: #244d34
--green-deep: #152d1f
--red: #8b2020
--red-bright: #a52828
--gold: #c9a050
--gold-light: #e2c07a
--parchment: #f7f1e6
--parchment2: #efe8d8
--cream: #fdfaf5
--text: #1a1a1a
--muted: #5a5a5a
```
Google Fonts: `Playfair Display` (serif headings) + `Cormorant Garamond` (italic quotes) + `Inter` (body)

## Brand Voice
- NOT AI-sounding. Write like a confident, experienced human operator.
- No filler phrases: "we are dedicated to", "we pride ourselves", "look no further"
- Short punchy paragraphs. Varied sentence length.
- Confident, warm, slightly authoritative — like a luxury service brand that's been around 50 years.
- Nationwide focus (not just Arizona). SCC serves clients across the US.
- Always mention "since 1972" and "oldest Santa staffing agency" where natural.
- No duplicate content between pages — every page earns its own unique content.

## Real Photos to Use (reference these URLs in img tags / background-image)
- Hero/about: `https://www.hiresanta.com/wp-content/uploads/2018/11/edited-santa.jpg`
- Santa close-up: `https://www.hiresanta.com/wp-content/uploads/2019/01/hire-santa-claus-2.jpg`
- Family events: `https://www.hiresanta.com/wp-content/uploads/2022/10/family-events.jpg`
- Corporate events: `https://www.hiresanta.com/wp-content/uploads/2022/10/corporate-events.jpg`
- Mall/retail: `https://www.hiresanta.com/wp-content/uploads/2022/10/mall-retail.jpg`
- Talent/parade: `https://www.hiresanta.com/wp-content/uploads/2022/10/talent-agency.jpg`
- Santa portrait 1: `https://santaclausandcompany.com/wp-content/uploads/2022/10/Cards-Joe-Aiello-Low-Res-274x300.jpg`
- Santa portrait 2: `https://santaclausandcompany.com/wp-content/uploads/2022/10/Cards-Mark-DeMonbrun-2.jpg`
- Real Santa: `https://santaclausandcompany.com/wp-content/uploads/2022/10/HireSanta-Real-Santa-Claus-small.jpg`

## Gravity Forms Placeholder
Everywhere a booking/contact form appears, use this comment instead of a real form:
`<!-- [gravityforms id="1"] -->`
Then show a styled "Loading form..." placeholder div below it.

## Schema (include in every page <head>)
Each page needs LocalBusiness JSON-LD. City pages get areaServed adjusted. Service pages get a Service schema added.

## NAV (copy exactly)
```html
<nav>
  <a href="/index.html" class="logo-wrap">
    <span class="logo-est">Est. 1972</span>
    <span class="logo-name">Santa Claus &amp; Company</span>
    <span class="logo-rule">Nationwide</span>
  </a>
  <ul class="nav-links">
    <li><a href="/services/">Services</a></li>
    <li><a href="/about.html">About</a></li>
    <li><a href="/rates.html">Rates</a></li>
    <li><a href="/locations/">Locations</a></li>
    <li><a href="/hire-santa.html" class="nav-cta">Book Santa</a></li>
  </ul>
</nav>
```

## FOOTER (copy exactly from index.html — keep EST. 1972 block)

---

## PAGES TO BUILD

### Core Pages
1. `about.html` — Company history since 1972, the team, vetting process, mission. Feature the "oldest" credential heavily. Include photo of real Santa.
2. `rates.html` — Pricing page. Don't list specific prices (they vary). Instead: explain the factors (duration, location, event type, travel), show a pricing tier table (Budget / Standard / Premium experience levels), strong CTA to get a custom quote. No fake prices.
3. `faq.html` — Comprehensive FAQ, 20+ questions. Cover: booking process, pricing, what to expect, safety/background checks, how far in advance, cancellation, what Santa wears/brings, nationwide availability, corporate vs. private. Use FAQPage JSON-LD schema for ALL questions.
4. `hire-santa.html` — Dedicated booking/contact page. Full-width form (Gravity Forms placeholder). Left side: reassurance copy, what happens after you submit, response time promise (24hrs). Trust elements alongside.
5. `employment.html` — Santa talent application page. Recruiting Santas nationwide. Requirements: real beard preferred, background check required, professional demeanor, experience helpful. Application form placeholder.
6. `privacy-policy.html` — Standard privacy policy. Keep it real but brief.
7. `thank-you.html` — Post-form-submission page. Warm, on-brand. "We received your request. Expect to hear from us within 24 hours."

### Service Pages (all go in /services/)
8. `services/index.html` — Services overview page. Grid of all services with photos and links. Nationwide intro.
9. `services/home-visits.html` — Personal Santa home visits. Nationwide. What to expect, how long, what Santa brings, tips for parents. 2 city-agnostic FAQs.
10. `services/corporate-events.html` — Corporate holiday parties, client events. Enterprise angle. Mentions Fortune 500 caliber experience. 2 FAQs.
11. `services/business-parties.html` — Smaller business/office parties. Slightly different angle than corporate — more intimate, budget-conscious framing.
12. `services/breakfast-with-santa.html` — Breakfast/brunch events with Santa. Restaurants, HOAs, community groups. How it works, what's included.
13. `services/house-parties.html` — Christmas house/block parties. Neighborhoods, HOA events, family gatherings.
14. `services/school-daycare.html` — School and daycare visits. Safety emphasis. Age-appropriate experiences. Pre-K through elementary.
15. `services/parades.html` — Parade appearances, tree lighting ceremonies, grand entrances. Large-scale public events.
16. `services/mall-retail.html` — Mall Santas, retail locations, pop-up experiences. Driving foot traffic angle.
17. `services/charity-events.html` — Charity and nonprofit events. Community-focused copy. Mentions discounted rates for qualifying nonprofits.
18. `services/weddings.html` — Christmas/winter wedding appearances. Unique angle, fun and whimsical copy.

### Location Pages (all go in /locations/)
19. `locations/index.html` — Locations overview. US map concept (text-based). Intro: "We send Santas nationwide." Grid of all city links. CTA.

#### Arizona Cities (existing market)
20. `locations/phoenix-arizona.html` ← use the built interior template, already done as reference
21. `locations/scottsdale-arizona.html`
22. `locations/mesa-arizona.html`
23. `locations/tempe-arizona.html`
24. `locations/chandler-arizona.html`
25. `locations/gilbert-arizona.html`
26. `locations/glendale-arizona.html`
27. `locations/peoria-arizona.html`
28. `locations/avondale-arizona.html`
29. `locations/goodyear-arizona.html`
30. `locations/cave-creek-arizona.html`
31. `locations/queen-creek-arizona.html`

#### National Cities (new — nationwide expansion)
32. `locations/los-angeles-california.html`
33. `locations/new-york-new-york.html`
34. `locations/chicago-illinois.html`
35. `locations/dallas-texas.html`
36. `locations/houston-texas.html`
37. `locations/miami-florida.html`
38. `locations/denver-colorado.html`
39. `locations/las-vegas-nevada.html`
40. `locations/seattle-washington.html`
41. `locations/atlanta-georgia.html`
42. `locations/boston-massachusetts.html`
43. `locations/nashville-tennessee.html`

---

## CONTENT RULES (enforce strictly)
- Every city page: unique intro paragraph mentioning the city, unique FAQ questions specific to that market, nearby cities tag cloud linking to sibling pages.
- Every service page: real-world scenario in first paragraph (paint a picture), clear what's-included section, 2 unique FAQs only.
- No page should repeat the same opening sentence structure as another.
- Nationwide framing: "Whether you're in Phoenix or Portland, New York or Nashville..."
- Phone: (602) 954-8697 | Email: santa@santaclausandcompany.com
- Footer HireSanta link: https://www.hiresanta.com
- All internal links must use relative paths.

## OUTPUT
Write each file completely. Save to the correct path under `/Users/openclaw/.openclaw/workspace/scc-website/`.
Start with core pages, then services, then locations.
After all files are written, output a DONE signal with a file count.

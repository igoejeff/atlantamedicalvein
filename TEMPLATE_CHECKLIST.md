# 🔧 SPARKPAGE TEMPLATE — CLIENT ONBOARDING CHECKLIST
> Use this document for every new client. Work top-to-bottom. Check off each item.
> Most swaps require only Ctrl+F on the `<!-- TEMPLATE:` comment in sparkpage.html.

---

## ⚡ QUICK-START: 5 CSS Variables (Rebrand in 2 Minutes)

Open `sparkpage.html`, find `:root {` and replace these 5 values:

```css
--navy:       #0d2145;   /* Client's primary dark color (nav, hero, footer) */
--blue:       #1B75BB;   /* Client's action/accent color (buttons, links) */
--blue-mid:   #1561a0;   /* Hover state — darken --blue by ~10% */
--blue-light: #e8f4ff;   /* Light tint of --blue (card backgrounds) */
--gold:       #c8973a;   /* Optional secondary accent (badges) */
```

**Tools:** https://coolors.co · https://color.adobe.com · https://contrast-ratio.com (aim for 4.5:1 minimum)

---

## ✅ SECTION-BY-SECTION SWAP CHECKLIST

### 1. `<head>` — SEO Meta (Lines ~10–65)
- [ ] `<title>` — "Condition + Location | Clinic Name"
- [ ] `<meta name="description">` — 150–160 chars, include phone
- [ ] `<meta name="keywords">` — 8–12 core keyword phrases
- [ ] `<link rel="canonical">` — final production URL (no trailing slash)
- [ ] `geo.region` — e.g. `US-GA`
- [ ] `geo.placename` — e.g. `Atlanta, Georgia`
- [ ] `geo.position` & `ICBM` — decimal lat;lon for clinic address
- [ ] `og:title`, `og:description`, `og:url` — match meta above
- [ ] `og:image` — 1200×630px hero image URL
- [ ] `twitter:site` — client Twitter/X handle
- [ ] `twitter:label1/data1` / `label2/data2` — key differentiators
- [ ] Favicon `<link rel="icon">` — client logo URL
- [ ] `<link rel="preload">` hero + logo image URLs
- [ ] Theme color `<meta name="theme-color">` — match --navy

---

### 2. JSON-LD Structured Data

#### MedicalClinic / LocalBusiness
- [ ] `"name"` — exact legal clinic name
- [ ] `"alternateName"` — DBA or common name variant
- [ ] `"description"` — 2–3 sentence clinic description
- [ ] `"url"` — production domain root
- [ ] `"telephone"` — E.164 format: +1XXXXXXXXXX
- [ ] `"email"` — clinic contact email
- [ ] `"logo"` — logo image URL
- [ ] `"image"` — hero/clinic photo URL
- [ ] `"priceRange"` — $ / $$ / $$$
- [ ] `"medicalSpecialty"` — specialty type
- [ ] `"address"` — streetAddress, locality, region, postalCode
- [ ] `"geo"` — exact latitude / longitude
- [ ] `"areaServed"` — list all cities served
- [ ] `"openingHoursSpecification"` — days + opens/closes times
- [ ] `"aggregateRating"` ratingValue + reviewCount — use real numbers
- [ ] `"review"` array — 3+ real patient reviews with dates
- [ ] `"contactPoint"` — phone + availableLanguage + hoursAvailable
- [ ] `"sameAs"` array — add ALL citation/directory URLs

#### Person (Team Members)
- [ ] Name, jobTitle, honorificSuffix for each provider
- [ ] `"image"` — real headshot URL for each
- [ ] `"description"` — bio sentence per provider
- [ ] `"medicalSpecialty"` — per physician

#### MedicalProcedure (Services)
- [ ] `"name"` — exact procedure name
- [ ] `"description"` — clinical description
- [ ] `"bodyLocation"` — anatomical area
- [ ] `"followup"` + `"preparation"` + `"howPerformed"`
- [ ] `"legalStatus"` — "FDA-approved" if applicable

#### MedicalCondition (Conditions Treated)
- [ ] Name, description, signOrSymptom array
- [ ] `"possibleTreatment"` — link to procedure @id

#### VideoObject (when video is available)
- [ ] `"name"` — descriptive video title
- [ ] `"description"` — what the video covers
- [ ] `"thumbnailUrl"` — thumbnail image URL
- [ ] `"uploadDate"` — YYYY-MM-DD
- [ ] `"contentUrl"` — YouTube/Vimeo direct URL
- [ ] `"embedUrl"` — embed URL for YouTube/Vimeo

#### FAQPage
- [ ] All Q&As match client's actual services and policies
- [ ] Include: procedure time, insurance, hours, location, cost, team, candidacy, pain, recovery, referral, sessions

---

### 3. TOP BAR (Search: `<!-- TOP BAR`)
- [ ] Phone number (href AND display text)
- [ ] Days open (e.g. "Mon – Thu")
- [ ] Street address (itemprop streetAddress/locality/region/postalCode)

---

### 4. HEADER (Search: `<!-- HEADER`)
- [ ] Logo `src` and `alt` text
- [ ] Nav link labels and `href` targets (keep `#id` anchors matching section IDs)
- [ ] Phone number `href` and display text in .btn-phone

---

### 5. HERO (Search: `<!-- HERO`)
- [ ] Hero star badge: **Replace `ChIJ_REPLACE_WITH_REAL_PLACE_ID`** with real Google Place ID
  - Find Place ID: https://developers.google.com/maps/documentation/javascript/examples/places-placeid-finder
  - Direct write-review URL: `https://search.google.com/local/writereview?placeid=YOUR_PLACE_ID`
- [ ] Star rating (4.7) and review count (300+) — use real numbers
- [ ] H1 headline — condition + city
- [ ] Sub-text paragraph — clinic name, address, USP
- [ ] Trust items (3 bullets under hero buttons)
- [ ] Hero card stats (providers, procedure time, downtime, insurance, hours)

---

### 6. ABOUT (Search: `<!-- ABOUT`)
- [ ] About image `src` and `alt` text
- [ ] Section headline
- [ ] 3–4 paragraph description of the clinic
- [ ] 4 about-points with icons, titles, and descriptions
- [ ] Address, nearby landmark, highway references

---

### 7. CONDITIONS / EDUCATION
- [ ] Condition names (Varicose Veins, Spider Veins, Reticular Veins)
- [ ] Clinical descriptions matching what the client treats
- [ ] Symptom list items per condition
- [ ] Risk factor grid items (6 items)

---

### 8. TEAM (Search: `<!-- TEAM`)
- [ ] Number of team cards (add/remove articles as needed)
- [ ] Each card: photo `src` + `alt`, name, credential suffix, job title
- [ ] Fallback initials in `onerror` handler
- [ ] EEAT credential bar items match actual credentials on staff

---

### 9. INSURANCE (Search: `<!-- INSURANCE`)
- [ ] Accepted insurance carrier names and notes (update all 8 ins-cards)
- [ ] Prior auth notice text
- [ ] Cost transparency note
- [ ] Phone number in links

---

### 10. TREATMENTS (Search: `<!-- TREATMENTS`)
- [ ] Number of treatment cards (3 is standard)
- [ ] Procedure number labels (01, 02, 03)
- [ ] Procedure names, icons, descriptions
- [ ] Detail bullets (4 per procedure)
- [ ] Tags (e.g. "For Larger Varicose Veins")
- [ ] "Learn More" links → correct service page URLs

---

### 11. GEO PROXIMITY (Search: `<!-- GEO PROXIMITY`)
- [ ] City name in headline
- [ ] Exact address in paragraph
- [ ] Nearby landmarks and highway references
- [ ] Service area tags (12 city tags — update all)

---

### 12. WHAT TO EXPECT
- [ ] 4 step titles and descriptions
- [ ] Insurance/prior-auth note text and phone number

---

### 13. FAQ (Search: `<!-- FAQ`)
- [ ] All Q&As updated to match client services, policies, team names
- [ ] Include 18 total FAQs recommended (the template ships with 18)
- [ ] Location FAQ has correct address and nearby cities
- [ ] FAQ schema in JSON-LD matches HTML FAQ content

---

### 14. REVIEWS (Search: `<!-- REVIEWS`)
- [ ] Review star rating (big number + reviewCount)
- [ ] **Google Leave-a-Review link** — Replace `ChIJ_REPLACE_WITH_REAL_PLACE_ID` in 3 places:
  1. Hero star badge
  2. Reviews section CTA block
  3. CTA banner "Leave Us a Review" button
  4. Footer trust badge
- [ ] Yelp URL — real Yelp listing URL
- [ ] Healthgrades URL — real Healthgrades listing
- [ ] 3 review card texts, author names, dates, initials
- [ ] "Read All Google Reviews" link → real Google Maps listing

---

### 15. BEFORE/AFTER (Search: `<!-- BEFORE/AFTER`)
- [ ] Real patient photos in ba-img-wrap (with signed HIPAA consent)
- [ ] Treatment labels and outcome notes per card
- [ ] Update HIPAA consent note text if needed

---

### 16. VIDEO (Search: `<!-- VIDEO`)
- [ ] Replace placeholder with real YouTube/Vimeo embed
  - YouTube: `<iframe src="https://www.youtube.com/embed/VIDEO_ID" title="..." allowfullscreen></iframe>`
  - Remove `video-placeholder` div when real video is added
- [ ] Update VideoObject JSON-LD with real contentUrl, embedUrl, uploadDate

---

### 17. COMPARISON TABLE
- [ ] Column headers (procedure names)
- [ ] Row data for each feature/procedure combination
- [ ] Adjust rows to match client's actual offering

---

### 18. CONTACT FORM (Search: `<!-- CONTACT FORM`)
- [ ] Connect form to a real handler (3 options in the JS comments):
  - **Option A — Formspree:** https://formspree.io (free tier: 50 submissions/mo)
  - **Option B — EmailJS:** https://emailjs.com (free tier: 200/mo)
  - **Option C — Netlify Forms:** Add `netlify` attribute (requires Netlify hosting)
- [ ] Update `preferred_day` select options to match client open days
- [ ] Update insurance dropdown to match client accepted plans
- [ ] Privacy Policy and Terms links
- [ ] Form phone number in trust sidebar
- [ ] Success message phone number

---

### 19. HOURS & CONTACT (Search: `<!-- HOURS & CONTACT`)
- [ ] Hours table rows (open/closed per day)
- [ ] Open badge text ("Open Mon – Thu")
- [ ] **Google Maps embed URL** — replace with real embed URL from Google Maps:
  1. Search address on maps.google.com
  2. Click Share → Embed a map → Copy iframe src URL
- [ ] Address display (all 4 contact-info-list items)
- [ ] Phone, email, directions link

---

### 20. CTA BANNER
- [ ] Headline text
- [ ] Sub-text (open days + address)
- [ ] Phone number button
- [ ] "Leave Us a Review" link (replace Place ID)

---

### 21. FOOTER (Search: `<!-- FOOTER`)
- [ ] Logo `src` and `alt`
- [ ] Footer description paragraph
- [ ] Trust badges (HIPAA, Board-Certified, Secure)
- [ ] Google review link (replace Place ID)
- [ ] Social links: Facebook, Instagram, Google
- [ ] Treatments column — all 5 service page links
- [ ] Quick Links column — all anchor IDs match section IDs
- [ ] Contact column — address, phone, email, hours
- [ ] Copyright year and clinic name
- [ ] Privacy Policy, Terms of Use, Accessibility, Sitemap links

---

### 22. STICKY CALL BAR (mobile)
- [ ] Phone number href and "Call Now" label
- [ ] Schedule link target

---

## 📂 ADDITIONAL FILES TO UPDATE

| File | What to Update |
|------|----------------|
| `sitemap.xml` | All `<loc>` URLs → production domain; `<lastmod>` dates |
| `robots.txt` | Sitemap URL → production domain |
| `services/varicose-vein-treatment.html` | Full rebrand if included |
| `services/spider-vein-treatment.html` | Full rebrand if included |
| `services/venclose-rfa.html` | Full rebrand if included |
| `services/varithena.html` | Full rebrand if included |
| `services/sclerotherapy.html` | Full rebrand if included |
| `blog.html` | Rebrand header/footer |
| `team-page.html` | Update all team cards |

---

## 🔑 POST-LAUNCH OFF-PAGE CHECKLIST

### Google Business Profile (GBP) — HIGHEST PRIORITY
- [ ] Claim/verify GBP at https://business.google.com
- [ ] Upload 10+ photos (interior, exterior, staff, equipment, logo)
- [ ] Add all services with descriptions
- [ ] Set hours matching the website
- [ ] Add Q&A (seed with your own FAQs)
- [ ] Get first 5 reviews before launch

### Find Real Google Place ID
1. Go to https://developers.google.com/maps/documentation/javascript/examples/places-placeid-finder
2. Type clinic name + city in the search box
3. Copy the Place ID (starts with "ChIJ...")
4. Replace ALL instances of `ChIJ_REPLACE_WITH_REAL_PLACE_ID` in sparkpage.html

### Citation Building (NAP Consistency)
- [ ] Google Business Profile
- [ ] Yelp for Business: yelp.com/biz/add
- [ ] Healthgrades: healthgrades.com/provider-registration
- [ ] Vitals: vitals.com
- [ ] WebMD Physician Directory: webmd.com
- [ ] ZocDoc: zocdoc.com
- [ ] Doximity (for physicians): doximity.com
- [ ] NPI Registry: nppes.cms.hhs.gov
- [ ] Better Business Bureau: bbb.org
- [ ] Local Chamber of Commerce

### Search Console & Analytics
- [ ] Google Search Console: search.google.com/search-console
  - Verify domain ownership → Submit sitemap.xml
- [ ] Google Analytics 4: analytics.google.com
- [ ] Bing Webmaster Tools: bing.com/webmasters
- [ ] Install GA4 tracking snippet in `<head>` before `</head>`

### Technical
- [ ] Submit sitemap.xml to Google Search Console
- [ ] Check Core Web Vitals (PageSpeed Insights: pagespeed.web.dev)
- [ ] Test all pages on mobile (Google Mobile-Friendly Test)
- [ ] Validate structured data (Google Rich Results Test: search.google.com/test/rich-results)
- [ ] Check for broken links (W3C Link Checker)
- [ ] Compress images (TinyPNG / Squoosh)
- [ ] Enable HTTPS / SSL certificate

---

## 🎯 GOOGLE REVIEW LINK — STEP BY STEP
This is the #1 most impactful quick win. Do this first.

1. **Find Your Place ID:**
   - Go to: https://developers.google.com/maps/documentation/javascript/examples/places-placeid-finder
   - Search the clinic name and city
   - Copy the Place ID (e.g. `ChIJrTLr-GyuEmsRBfy61i59si4`)

2. **Build the Write-Review URL:**
   ```
   https://search.google.com/local/writereview?placeid=YOUR_PLACE_ID
   ```

3. **Replace in sparkpage.html** — Search for `ChIJ_REPLACE_WITH_REAL_PLACE_ID` — there are **4 occurrences**:
   - Hero star badge link
   - Reviews section "Leave a Google Review" button
   - CTA banner "Leave Us a Review" button
   - Footer trust badge

4. **Also update `sameAs` in JSON-LD:**
   Add your verified GBP URL (e.g. `https://g.co/kgs/YOUR_HANDLE`)

---

## 📱 FORM INTEGRATION — QUICK SETUP

### Formspree (Recommended — Free, No Backend)
1. Create account at formspree.io
2. Create a new form → copy the form ID (e.g. `xvojbgkn`)
3. In sparkpage.html JS, uncomment Option A and replace `YOUR_FORM_ID`
4. Add `action="https://formspree.io/f/YOUR_FORM_ID"` to `<form>` tag as backup

### EmailJS (Alternative)
1. Create account at emailjs.com
2. Add email service + template → copy Service ID + Template ID
3. Add EmailJS CDN to `<head>`: `<script src="https://cdn.jsdelivr.net/npm/@emailjs/browser@4/dist/email.min.js"></script>`
4. Uncomment Option B in the JS form handler

---

## 🏆 COMPETITIVE SCORING (Target for Each Client)

| Signal | Target Score | How to Hit It |
|--------|-------------|---------------|
| Core SEO | A+ | Title, meta, canonical, schema, robots |
| Structured Data | A+ | MedicalClinic, FAQPage, HowTo, VideoObject, Persons |
| FAQ Coverage | A+ | 18 Q&As covering all patient intent |
| GEO/Near-Me | A+ | Address in H1, geo meta, GEO block, 12+ city tags |
| E-E-A-T | A+ | Named providers, credentials, reviews, schema |
| Mobile UX | A | Sticky bar, 44px targets, shrink header, 1-col layout |
| Local SEO | A | GBP verified, citations, NAP consistency |
| Social/OG | A | og:image, twitter:card, social links in footer |
| Page Speed | A | Preload hero, defer FontAwesome, lazy-load images |
| Form/Lead Gen | A | Real form handler connected, clear CTA |

---

*Template version: 2026-03-12 | Built by [Your Agency Name] | Confidential — Client Use Only*

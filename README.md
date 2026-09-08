# HopNTrip — Sabah Tourism Agency Website

HopNTrip is a static, multi-page website for a fictional/practice travel agency specialising in Sabah, Malaysia tourism. It showcases a full customer-facing booking experience — flights, hotels, tours, and travel insurance — alongside company info, a portfolio, and account login/registration, all built with plain HTML, CSS, and JavaScript (no frameworks, no backend).

## 📄 Pages

| File | Description |
|---|---|
| `index.html` | Homepage — hero banner, highlights, and entry points into the rest of the site |
| `about-us.html` | Company story, mission, team profiles, and certifications |
| `services.html` | Overview of services offered by HopNTrip |
| `tours.html` | Browsable tour packages around Sabah |
| `flighbooking.html` | Flight search & booking UI (from/to, dates, travelers, class, airline/price/duration filters) |
| `hotels.html` | Hotel search & booking UI (destination, check-in/out dates, guests, price/rating/amenity filters) |
| `insurance.html` | Travel insurance plan selector and application form (traveler details, passport, trip dates, plan choice) |
| `contact-us.html` | Contact form (name, email, subject, travel interest, message) plus embedded Google Map and location details |
| `login.html` | Combined login / registration UI with tab switching, show/forgot password flows |
| `portfolio.html` | Showcase of past trips/projects or client work |

All pages share a common navigation bar, footer, and design language, and link to one another via relative `.html` paths (e.g. `href="about-us.html"`).

## ✨ Key Features

- **Responsive navigation** — collapsible/sidebar menu with language dropdown, shared identically across all pages
- **Flight & hotel search forms** — interactive filters (checkboxes for airline, price range, duration, star rating, amenities)
- **Insurance application form** — full traveler intake form with required-field validation (`required` attributes) and a plan field that's populated from the selected plan
- **Contact form** — validated inputs with an embedded Google Maps location and a WhatsApp click-to-chat link
- **Login / Register** — client-side JS handlers (`handleLogin`, `handleRegister`, `handleForgotPassword`) with password visibility toggle and a forgot-password modal
- **Floating chat widget** — a "Type your message..." live-chat style box present on most inner pages
- **Social & partner links** — Facebook, Instagram, TikTok, YouTube, TripAdvisor icons, plus MSTA / IATA / UNESCO / Eco certification badges
- **Smooth scrolling & scroll-to-top** — UX polish via CSS `scroll-behavior` and JS scroll listeners

## 🛠️ Tech Stack

- **HTML5** — semantic markup, one self-contained file per page
- **CSS3** — embedded `<style>` blocks per page (CSS custom properties for theming, e.g. `--primary`, `--accent`)
- **Vanilla JavaScript** — embedded `<script>` blocks handling menus, modals, forms, and the chat widget (no external JS frameworks)
- **Font Awesome 6.5.0** — icon library, loaded via CDN (`cdnjs.cloudflare.com`)
- **Pexels** — stock photography, loaded via hotlinked URLs
- **Google Maps Embed** — used on the Contact Us page

## 📁 Expected Folder Structure

The pages reference local assets under an `image/` directory that isn't included in this upload. To run the site as intended, create the following structure:

```
project-root/
├── index.html
├── about-us.html
├── contact-us.html
├── flighbooking.html
├── hotels.html
├── insurance.html
├── login.html
├── portfolio.html
├── services.html
├── tours.html
└── image/
    ├── logo1.png
    ├── HopNTrip logo variants...
    ├── hero images...
    ├── hotel1.jpg, hotel2.jpg, hotel3.jpg, hotel_bg.jpg
    ├── flight_bg.jpg, sabah_bg.jpg, mountain3.jpg
    ├── team photos (tiff.jpg, enyi.jpg, weiting.jpg, wenxi.jpg, yixuan.jpg)
    ├── certification badges (iata.png, msta.png)
    └── social icons (facebook, instagram, tiktok, youtube, tripadvisor, whatsapp)
```

Without this `image/` folder populated, pages will load and function but images will appear broken.

## 🚀 Getting Started

Since this is a static site with no build step or backend:

1. Download/clone all `.html` files into a single folder.
2. Add an `image/` folder alongside them containing the required assets (see structure above).
3. Open `index.html` directly in a browser, **or** serve the folder locally for the best experience (recommended, since some browsers restrict local file behavior):
   ```bash
   # Using Python
   python -m http.server 8000

   # Then visit
   http://localhost:8000/index.html
   ```
4. Navigate the site using the top navigation bar — all internal links are relative, so no server-side routing is required.

## ⚠️ Known Limitations

- **No backend / persistence** — login, registration, booking, and contact forms are front-end only; submissions are not sent anywhere or stored (no database, no API calls).
- **Hardcoded sample data** — flight/hotel search fields have pre-filled placeholder values (e.g. dates from 2023) rather than live data.
- **Duplicated CSS/JS** — shared components (nav, footer, chat widget) are copy-pasted into every page rather than extracted into shared files.
- **External image hotlinking** — some images are pulled live from Pexels URLs, which requires an internet connection and depends on those URLs staying valid.
- **No accessibility/SEO audit performed** — while some `aria-label`s exist (e.g. on the login form), a full accessibility pass hasn't been done.

## 🔮 Possible Next Steps

- Extract shared nav/footer/chat-widget markup into includes or a JS templating approach to reduce duplication
- Move inline `<style>`/`<script>` blocks into shared external `styles.css` / `script.js` files
- Wire up forms to a real backend (e.g. Node/Express + database) for actual bookings, accounts, and contact submissions
- Replace hardcoded sample dates/values with dynamic data
- Store local images instead of relying on hotlinked stock photos

## 👥 Team

This is a group project. Team members (as credited on the About Us page):

| Name | Student ID |
|---|---|
| Tiffany Fam (Leader) | 23052301 |
| Tan Wei Ting | 23094709 |
| Teoh En Yi | 2305110 |
| Tan Wen Xi | 23093495 |
| Sian Yi Xuan | 23099609 |

# App.css

**Project:** Paradise Nursery — landing page styles

Stylesheet for the Paradise Nursery landing page, including the
background image for the hero (landing) section.

## Background image

The `.landing-page` hero section uses a real plant nursery photograph
as its background:

- Primary: `https://www.karurrosenursery.com/images/contact/contact-hero-karur-rose-nursery.png`
  (a wide view of a plant nursery with rows of potted greenery)
- Fallback: `https://palmlandnursery.com/wp-content/uploads/2025/10/Diverse_Plant_Nursery_Garden.webp`
  (shown only if the primary image fails to load)

It is layered under a dark gradient so the heading and text stay
readable, and styled with:

```css
background-size: cover;
background-position: center;
background-repeat: no-repeat;
background-attachment: fixed;
```

`background-attachment` switches to `scroll` on screens under 768px,
where fixed backgrounds stutter on mobile.

## What else is in the file

- Navbar, hero heading, text and call-to-action button styles
- Plant cards grid for the catalogue section
- Footer styles
- Responsive rules for mobile screens

## Usage

Import it in your React app:

```jsx
import './App.css';

function App() {
  return (
    <div className="landing-page">
      <h1>Welcome to Paradise Nursery</h1>
      <p>Find the perfect plants for your home and garden.</p>
      <a className="cta-button" href="#plants">Shop Plants</a>
    </div>
  );
}

export default App;
```

To use a different background image, replace the two image URLs in
the `.landing-page` rule.

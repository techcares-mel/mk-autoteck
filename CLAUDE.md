# MK Autoteck Centre – Website Design Rules

## Business Info
- **Name**: MK Autoteck Centre
- **Type**: Auto mechanic service, car repair
- **Address**: 109-113 McIntyre Rd, Sunshine North VIC 3020
- **Phone**: (03) 9310 2776
- **Logo**: `Logo.png`

## Reference Style
Inspired by cowboy.com – a premium, dark, full-bleed design with cinematic scroll animations.

## Design System

### Color Palette
| Token | Value | Usage |
|---|---|---|
| `--bg-primary` | `#0a0a0a` | Page background |
| `--bg-secondary` | `#111111` | Section alternates |
| `--bg-card` | `#1a1a1a` | Cards, panels |
| `--text-primary` | `#ffffff` | Headings, main text |
| `--text-secondary` | `#a0a0a0` | Subtext, captions |
| `--accent` | `#2196F3` | Blue accent (matches logo) |
| `--accent-hover` | `#1565C0` | Hover state |
| `--border` | `rgba(255,255,255,0.08)` | Dividers, card borders |

### Typography
- **Font stack**: `'Inter', 'SF Pro Display', -apple-system, sans-serif`
- **Hero heading**: 72–96px, weight 700–900, tight letter-spacing (-0.03em)
- **Section heading**: 48–64px, weight 700
- **Sub-heading**: 24–32px, weight 600
- **Body**: 16–18px, weight 400, line-height 1.7
- **Caption/Label**: 12–14px, weight 500, uppercase, letter-spacing 0.1em
- All text renders white on dark backgrounds

### Layout
- Full-width sections, 100vw
- Max content width: 1280px, centered
- Section padding: `120px 0` on desktop, `80px 0` on mobile
- Horizontal padding: `clamp(24px, 5vw, 80px)`
- Grid: 12-column with `gap: 24px`

### Navigation
- Fixed/sticky, transparent → blurred dark on scroll
- Logo left, nav links right
- `backdrop-filter: blur(20px)` when scrolled
- Height: 72px
- Mobile: hamburger menu with slide-down overlay

### Hero Section
- 100vh full-screen
- Background: team photo with dark overlay (`rgba(0,0,0,0.55)`)
- Large headline centered, white
- Subtext in accent blue
- CTA button with border + hover fill
- Scroll-down indicator (animated chevron)

### Service Cards
- Dark card `#1a1a1a`, `border: 1px solid var(--border)`
- `border-radius: 8px`
- Icon top, title, description
- Hover: lift with `translateY(-8px)`, border glows blue
- Transition: `all 0.3s cubic-bezier(0.4, 0, 0.2, 1)`

### Buttons
- Primary: `background: var(--accent)`, `color: white`, `padding: 14px 32px`, `border-radius: 4px`
- Outline: `border: 1px solid rgba(255,255,255,0.3)`, transparent bg → filled on hover
- Hover transitions: 0.25s ease

### Scroll Animations
- Elements fade up: `opacity: 0; transform: translateY(40px)` → visible
- Staggered children with `animation-delay: 0.1s` increments
- Use `IntersectionObserver` API
- Trigger at 80% visibility threshold
- Duration: 0.6s ease-out

### Sections Order
1. **Nav** – sticky, minimal
2. **Hero** – full screen, team photo background
3. **Services** – 3-column card grid
4. **About** – split layout (text left, image right)
5. **Work Gallery** – full-bleed image strip (engine + car photos)
6. **Why Choose Us** – stats/features row
7. **Contact** – map + details side by side
8. **Footer** – minimal, logo + links

### Back to Top Button
- Fixed bottom-right, `border-radius: 50%`
- Appears after scrolling 400px
- Smooth scroll to top on click
- Accent blue, arrow icon

### Mobile (< 768px)
- Single column layout
- Hero text scales down: `clamp(40px, 8vw, 72px)`
- Hamburger nav
- Cards stack vertically
- Images full width

### Image Treatment
- All images: `object-fit: cover`, `object-position: center`
- Hero overlay: `linear-gradient(to bottom, rgba(0,0,0,0.3) 0%, rgba(0,0,0,0.65) 100%)`
- Gallery: hover zoom `transform: scale(1.05)` with `overflow: hidden`

### Micro-interactions
- Nav links: underline slide-in from left on hover
- Service icons: rotate/scale on card hover
- Stats numbers: count-up animation when in view
- Scroll progress bar at top of page

## File Structure
```
/
├── index.html
├── styles.css
├── script.js
├── Logo.png
├── team.jpg
├── engine.jpg
├── car.jpg
└── CLAUDE.md
```

## Services Offered
1. Log Book Servicing
2. Preventative Maintenance
3. Brakes & Clutch Repairs
4. Air Conditioning Service
5. Tyres & Wheels
6. Transmission Servicing & Repairs
7. Engine Repairs & Rebuilds
8. Electrical Diagnostics

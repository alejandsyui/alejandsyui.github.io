# Site Architecture & Components

This document outlines the structure and components of the Microsoft homepage clone.

## HTML Structure

### Main Layout
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- Meta tags, title, stylesheets -->
</head>
<body>
    <!-- Navigation -->
    <nav class="main-nav">...</nav>

    <!-- Main content sections -->
    <header class="showcase">...</header>
    <section class="home-cards">...</section>
    <section class="xbox">...</section>
    <section class="carbon">...</section>
    <section class="follow">...</section>

    <!-- JavaScript -->
    <script>...</script>
</body>
</html>
```

## CSS Architecture

### Design System
- **Colors**: Microsoft brand colors (#0067b8, #262626, #ffffff)
- **Typography**: Segoe UI system font stack
- **Spacing**: Consistent padding/margin system
- **Breakpoints**: Mobile-first responsive design

### CSS Organization
- **Reset**: Box-sizing and margin/padding reset
- **Components**: Individual component styles
- **Utilities**: Reusable classes (.btn, .container)
- **Responsive**: Media queries for different screen sizes

## JavaScript Functionality

### Interactive Elements
- **Mobile Menu**: Toggle navigation on mobile devices
- **Hover Effects**: CSS-based transitions
- **Responsive Behavior**: Dynamic layout adjustments

### Event Listeners
```javascript
document.querySelector('.menu-btn').addEventListener('click', () => {
    document.querySelector('.main-menu').classList.toggle('show');
});
```

## Component Breakdown

### Navigation (.main-nav)
- Microsoft logo
- Main menu items (Office, Windows, Surface, Xbox, Deals, Support)
- Search and cart icons
- Mobile hamburger menu

### Showcase (.showcase)
- Hero section with Surface deals
- Call-to-action button
- Background image

### Product Cards (.home-cards)
- Grid layout (4 columns on desktop)
- Product images and descriptions
- "Learn More" links

### Xbox Section (.xbox)
- Game Pass Ultimate promotion
- Background image overlay
- Call-to-action button

### Carbon Section (.carbon)
- Environmental commitment messaging
- Dark theme variant

### Social Links (.follow)
- Facebook, Twitter, YouTube links
- Microsoft branding

## Responsive Design

### Breakpoints
- **Desktop**: > 700px (4-column grid)
- **Tablet**: 500px - 700px (2-column grid)
- **Mobile**: < 500px (1-column grid)

### Mobile Optimizations
- Hamburger menu for navigation
- Stacked card layout
- Adjusted spacing and typography

## External Dependencies

### Fonts & Icons
- **Font Awesome**: Icon library (CDN)
- **Google Fonts**: Segoe UI (system fallback)

### Images
- **External Hosting**: Images hosted on imgbb.co
- **Alt Text**: Accessibility compliance
- **Optimization**: Web-optimized formats

## Performance Considerations

### Loading Optimization
- CSS in `<head>` for render blocking
- JavaScript at end of `<body>`
- External resources from CDNs
- Minimal HTTP requests

### Accessibility
- Semantic HTML structure
- Alt text for images
- Keyboard navigation support
- Color contrast compliance

## Maintenance Notes

### Content Updates
- Update product information in HTML
- Replace images with current assets
- Modify CSS variables for theming

### Code Quality
- Valid HTML5 markup
- CSS follows BEM-like naming
- Minimal JavaScript footprint
- Cross-browser compatibility

# H&A Security Solutions - AI Coding Agent Instructions

## Project Overview
H&A Security Solutions is a cybersecurity company website built as a **static HTML site**. The architecture follows a simple static web approach with external contact form integration.

## Core Architecture

### Contact System
- **External Contact Form**: All contact requests redirect to `https://tellaro.io/contact/`
- **Business Relationship**: H&A operates as a "Doing Business As" (DBA) entity of Tellaro
- **No PHP Dependencies**: Contact forms have been removed - site is purely static HTML

### Asset Organization
- **CSS**: `assets/css/` - modular with external imports (TypeKit fonts, FontAwesome)
- **JavaScript**: `assets/js/main.js` - jQuery-based with animations and UI interactions
- **Images**: `assets/img/` organized by purpose (`hero/`, `tab/`, `logo/`, `about/`, etc.)
- **No Server Dependencies**: Pure static HTML site, no PHP processing required

### Page Structure Pattern
All pages follow consistent structure:
```html
<!DOCTYPE html>
<!-- IE8 compatibility comments -->
<head>
    <!-- Google Analytics (G-NM6M7MMYLD) -->
    <!-- CSS: reset.css + style.css -->
</head>
<body>
    <!-- Preloader with custom loader animation -->
    <div class="wrapper [page-class]">
        <header class="header [header-transparent|header-white]">
            <!-- Logo + Navigation + Social links -->
        </header>
        <!-- Page content -->
    </div>
    <!-- jQuery + validation + WOW.js animations -->
</body>
```

## Development Patterns

### CSS Architecture
- **Base**: `reset.css` for normalization
- **Main**: `style.css` with external imports at top
- **Animations**: WOW.js integration with CSS classes
- **Responsive**: Bootstrap-like container system (768px/992px/1200px breakpoints)

### JavaScript Patterns
- **jQuery-based**: All interactions use jQuery
- **External Contact**: Contact requests redirect to `https://tellaro.io/contact/`
- **Animation**: WOW.js for scroll-triggered animations with data attributes
- **Mobile**: Slide toggle navigation for mobile menu

```javascript
// Standard animation and UI patterns
$('.mobile-button').toggleClass('active');
$('.lists-wrap').slideToggle();
```

## File Naming Conventions
- **Pages**: `.html` for all pages (static site)
- **Assets**: Lowercase with hyphens (`logo-white.svg`, `edr-icon.png`)
- **Directories**: Lowercase, descriptive (`our-team/`, `section/`)

## Deployment Context
- **Server**: Any web server (no special requirements)
- **No Build Process**: Direct file serving - no compilation step
- **External Dependencies**: 
  - Google Fonts (TypeKit)
  - FontAwesome
  - Google Analytics
  - jQuery CDN

## Key Integration Points
- **Contact Routing**: All contact links → `https://tellaro.io/contact/` (external)
- **Analytics**: Google Tag Manager integration on all pages
- **Social Media**: Twitter, YouTube, LinkedIn links in header
- **Mobile Responsiveness**: CSS breakpoints + jQuery mobile menu

## Development Workflow
1. **Local Development**: Any web server or file:// protocol for testing
2. **No Dependencies**: Static HTML - no server-side processing
3. **Assets**: Direct file modification - no build step
4. **Deployment**: Upload files to any web server

## Common Gotchas
- **External Links**: Contact forms redirect to Tellaro.io - ensure `target="_blank"` is used
- **Mobile Menu**: Relies on jQuery slideToggle - ensure jQuery loads first
- **Icon Updates**: Use `fa-external-link` for external contact links

## File Priority for Changes
1. **Content**: `index.html`, `about.html`, `services.html`, `contact.html`
2. **Styling**: `assets/css/style.css`
3. **Functionality**: `assets/js/main.js`
4. **Assets**: `assets/img/` for visual updates
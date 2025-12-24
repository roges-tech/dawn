# New Gallery Layout: Thumbnail Slider with Main Slider

## Overview
A new gallery layout option has been added to the Dawn theme that combines:
- **Main image slider** with corner navigation controls
- **Thumbnail slider** below for quick navigation

## What's New?

### Layout Name: `thumbnail_slider_main`

This new layout extends the existing `thumbnail_slider` layout by adding slider functionality to the main/large product images.

### Key Features:

1. **Desktop (≥750px):**
   - Large product images slide left/right using corner buttons
   - Corner navigation buttons appear on hover with:
     - Circular design
     - Semi-transparent background
     - Smooth hover effects
     - Positioned at 50% height on left and right edges
   - Only one main image visible at a time
   - Thumbnail slider below with horizontal scrolling
   - Thumbnails sync with main image

2. **Mobile (<750px):**
   - Standard mobile slider with bottom navigation
   - Swipe gestures supported
   - Thumbnail slider available

## Files Modified:

### 1. `sections/main-product.liquid`
- Added new gallery layout option in schema
- Conditionally loads the new CSS file

### 2. `snippets/product-media-gallery.liquid`
- Updated slider buttons visibility for the new layout
- Modified thumbnail list classes to support the new layout

### 3. `assets/component-product-gallery-slider.css` (NEW)
- Custom styles for the main slider controls
- Corner button positioning and styling
- Media transition animations
- Responsive behavior

## How to Use:

1. **Via Theme Customizer:**
   - Go to: Shopify Admin > Online Store > Themes > Customize
   - Navigate to a Product page
   - Click on "Product information" section
   - Find "Gallery layout" setting
   - Select: **"Thumbnail slider with main slider"**

2. **Via Code:**
   Set the gallery_layout setting to `thumbnail_slider_main`:
   ```json
   {
     "gallery_layout": "thumbnail_slider_main"
   }
   ```

## Visual Behavior:

```
┌─────────────────────────────────┐
│  ◀                             ▶ │  ← Corner controls
│                                  │
│     [  MAIN IMAGE SLIDER  ]      │
│                                  │
│                                  │
└─────────────────────────────────┘
        ↓
◀ [thumb1] [thumb2] [thumb3] [thumb4] ▶
```

## Best For:
- Products with 5+ high-quality images
- Showcasing product details from multiple angles
- Enhanced user experience with dual navigation
- E-commerce stores wanting maximum image visibility

## Technical Details:

### CSS Classes:
- `.product--thumbnail_slider_main` - Applied to product container
- `.slider-button--prev` - Left corner button
- `.slider-button--next` - Right corner button
- `.thumbnail-list.slider--tablet-up` - Thumbnail slider

### Z-index Layers:
- Corner buttons: `z-index: 10`
- Sticky info: `z-index: 2`

### Animations:
- Button hover: 0.2s ease
- Media transitions: 0.3s ease

## Browser Support:
- Modern browsers (Chrome, Firefox, Safari, Edge)
- Mobile browsers (iOS Safari, Chrome Mobile)
- Progressive enhancement for older browsers

## Future Enhancements:
- [ ] Keyboard navigation (arrow keys)
- [ ] Touch/swipe gestures on desktop
- [ ] Auto-play option
- [ ] Customizable button styles in theme settings
- [ ] Transition effects (fade, slide, etc.)

---

**Created:** December 23, 2025  
**Version:** 1.0.0  
**Compatible with:** Dawn theme (latest)

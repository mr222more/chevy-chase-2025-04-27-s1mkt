# Custom Shower Glass Landing Page - Maintenance Guide

This guide will help you maintain and customize the Custom Shower Glass landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold tracking-tighter text-white hover:text-purple-400">
    Chevy Chase  <!-- Replace this text -->
</a>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <!-- Update these link texts -->
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
The main banner section contains the primary heading and subheading:

```html
<h1 class="text-4xl md:text-5xl lg:text-7xl font-bold leading-tight tracking-tighter mb-8">
    Custom shower glass for luxury bathroom  <!-- Update main heading -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12 leading-relaxed">
    Transform your bathroom into a modern sanctuary  <!-- Update subheading -->
</p>
```

### Tailwind CSS Class Guide
Common classes used in this template:

- Text sizes: `text-sm`, `text-base`, `text-lg`, `text-xl`, `text-2xl`
- Colors: `text-white`, `text-gray-300`, `text-purple-400`
- Spacing: `p-8` (padding), `m-4` (margin), `space-x-8` (horizontal spacing)
- Responsive: `md:text-xl` (applies at medium screens)

Example of updating a button's color:
```html
<!-- Original -->
<a href="#" class="bg-purple-600 hover:bg-purple-700">

<!-- To change to blue -->
<a href="#" class="bg-blue-600 hover:bg-blue-700">
```

## Fixing Broken Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Contact</a>
```

2. External Website Link:
```html
<!-- Update this URL to your actual website -->
<a href="http://www.customeuroglass.com">Explore Our Collection</a>
```

3. Email Link:
```html
<!-- Update with your actual email -->
<a href="mailto:info@customeuroglass.com">info@customeuroglass.com</a>
```

### How to Update Links
1. For internal section links (starting with #):
   - Ensure the href matches the id of the target section
   - Example: `href="#features"` should match `id="features"`

2. For external links:
   - Replace the placeholder URLs with actual websites
   - Always include `http://` or `https://`
   ```html
   <a href="https://your-actual-website.com">Visit Our Website</a>
   ```

## Linking Privacy and Terms Pages

### Adding Privacy and Terms Links
1. Locate the footer section:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <!-- Update these href attributes -->
        <li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

2. Create matching HTML files:
   - Create `privacy.html` in the same folder as `index.html`
   - Create `terms.html` in the same folder as `index.html`
   - Use the same styling classes for consistency

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links:**
   - Check that section IDs match exactly with href attributes
   - IDs are case-sensitive: `href="#Features"` won't link to `id="features"`

2. **Responsive Design Issues:**
   - Keep the responsive classes (`md:`, `lg:`) when updating
   - Test on different screen sizes after making changes

3. **Color Changes:**
   - Always update both regular and hover states
   - Example: `text-purple-400 hover:text-purple-300`

4. **Missing Styles:**
   - Verify the Tailwind CSS CDN link is working
   - Check for typos in class names

### Need Help?
- Reference the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate your HTML at [W3C Validator](https://validator.w3.org/)
- Test all links after making changes
- Keep a backup of the original code before making modifications

Remember to test all changes across different devices and browsers to ensure consistency in appearance and functionality.
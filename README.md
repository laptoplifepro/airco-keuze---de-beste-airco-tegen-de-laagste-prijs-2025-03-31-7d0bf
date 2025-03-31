# Airco Keuze Landing Page - Maintenance Guide

This guide will help you maintain and customize the Airco Keuze landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Logo Text:**
```html
<a href="/" class="text-2xl font-bold text-blue-600">Airco Keuze</a>
```
- Replace "Airco Keuze" with your desired text
- Adjust size using `text-2xl` (options: text-sm, text-base, text-lg, text-2xl, text-3xl)

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600">Voordelen</a>
    <!-- Other menu items -->
</div>
```
- Update text between `<a>` tags
- Maintain the class structure for consistent styling
- `hidden md:flex` means hidden on mobile, visible on medium screens

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    Snel De Juiste Airco Voor De Laagste Prijs
</h1>
```
- Update heading text while keeping the classes
- Size classes explain: `text-4xl` (mobile), `md:text-5xl` (medium screens), `lg:text-6xl` (large screens)

### Feature Cards
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold mb-4">Ruime Keuze</h3>
    <p class="text-gray-600">Ontdek ons uitgebreide assortiment...</p>
</div>
```
- Update heading in `<h3>` tags
- Modify description in `<p>` tags
- Keep the class structure for consistent styling

## Managing Links

### Navigation Links
Current navigation structure:
```html
<a href="#features">Voordelen</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. Internal links (same page):
   - Use `#section-id` format
   - Ensure section IDs match exactly
2. External links:
   - Replace `#` with full URL
   - Example: `href="https://www.example.com"`

### Call-to-Action Buttons
Current structure:
```html
<a href="https://amzn.to/4iRgNla" class="inline-block px-8 py-4 bg-blue-600 text-white">
    Bekijk Aanbod
</a>
```
To update:
1. Replace `href` value with your target URL
2. Update button text
3. Maintain classes for consistent styling

## Adding Privacy and Terms Pages

### Footer Links Setup
Current placeholder links:
```html
<ul class="space-y-2 text-gray-400">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Algemene Voorwaarden</a></li>
</ul>
```

To link to new pages:
1. Create new HTML files:
   - `privacy.html`
   - `terms.html`
2. Update href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Algemene Voorwaarden</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links:**
   - Check that section IDs match href values exactly
   - Example: `href="#features"` must match `id="features"`
   - IDs are case-sensitive

2. **Responsive Design Issues:**
   - Check screen-size classes:
     - `md:` (medium screens, 768px+)
     - `lg:` (large screens, 1024px+)
   - Don't remove `hidden md:flex` from navigation - it controls mobile menu visibility

3. **Styling Problems:**
   - Keep Tailwind class order consistent
   - Don't remove utility classes without understanding their purpose
   - Example: `transition-colors duration-300` controls hover animations

### Need Help?
- Check Tailwind CSS documentation for class references
- Use browser inspector to identify specific elements
- Test all changes across different screen sizes
- Maintain backup copies before making significant changes

Remember to test all changes thoroughly before pushing to production, especially links and responsive design elements.
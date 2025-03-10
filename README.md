# EagleiO Landing Page Maintenance Guide

This guide will help you maintain and customize the EagleiO landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text:**
```html
<a href="/" class="text-2xl font-bold text-white tracking-tight">
    Eagle<span class="text-blue-500">iO</span>
</a>
```
- Change "Eagle" and "iO" text directly
- The blue highlight is controlled by `text-blue-500`

2. **Navigation Links:**
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
    <!-- Other navigation items -->
</div>
```
- Edit text between `<a>` tags
- Maintain the class structure for consistent styling
- `hidden md:flex` ensures mobile responsiveness

### Hero Section
Located at the top of the page:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-blue-400 to-purple-500 bg-clip-text text-transparent">
    Soar Above Service Hassles with EagleiO
</h1>
```
- Update heading text directly
- Keep the gradient classes (`bg-gradient-to-r`, etc.) for the colorful effect
- Size classes explain the responsive behavior:
  - `text-4xl`: Default size
  - `md:text-5xl`: Medium screens
  - `lg:text-6xl`: Large screens

### Features and Benefits
Each feature card follows this structure:
```html
<div class="bg-gray-900 rounded-2xl p-8 hover:transform hover:scale-105 transition-all duration-300">
    <h3 class="text-xl font-semibold mb-4">Feature Title</h3>
    <p class="text-gray-400">Feature description text here.</p>
</div>
```
- Maintain the hover effects (`hover:transform`, `hover:scale-105`)
- Keep padding (`p-8`) and margin (`mb-4`) classes for consistent spacing

## Managing Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="https://www.eagle360.app">Get Started</a>
```

2. Call-to-Action Links:
```html
<a href="https://www.eagle360.app" class="px-8 py-4 bg-blue-600 rounded-full">
    Start Your Journey
</a>
```

### Updating Links
1. For internal section links:
- Keep the `#` prefix
- Ensure the ID matches your section:
```html
<!-- Navigation link -->
<a href="#features">Features</a>

<!-- Corresponding section -->
<section id="features" class="py-24 bg-gray-800">
```

2. For external links:
- Replace `https://www.eagle360.app` with your desired URL
- Always include `https://` or `http://`
- Test links after updating

## Adding Privacy and Terms Pages

### Footer Link Setup
Locate the legal section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link privacy and terms pages:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Responsive Design**
- If elements look wrong on mobile:
  - Check for `md:` prefixed classes
  - Ensure the `hidden md:flex` class is on the navigation menu
  - Verify viewport meta tag exists in header

2. **Missing Styles**
- If Tailwind styles aren't working:
  - Confirm the Tailwind CSS link is present:
```html
<link href="https://unpkg.com/tailwindcss@^2/dist/tailwind.min.css" rel="stylesheet">
```

3. **Links Not Working**
- For section links (#features, etc.):
  - Verify section IDs match exactly
  - Check for proper scroll-smooth class on html tag
- For external links:
  - Ensure full URLs with http:// or https://
  - Test in incognito mode

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test responsive design using browser developer tools

Remember to always backup your files before making changes and test on multiple devices and browsers after updates.
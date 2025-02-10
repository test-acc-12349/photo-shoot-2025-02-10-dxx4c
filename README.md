# Photo-Shoot Landing Page Maintenance Guide

This guide will help you maintain and customize the Photo-Shoot landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your brand name and navigation menu:

```html
<header class="sticky top-0 z-50 bg-white shadow-md">
    <nav class="container mx-auto px-4 py-4 flex items-center justify-between">
        <div class="flex items-center space-x-10">
            <a href="#" class="text-2xl font-bold text-gray-800">Photo-Shoot</a>
```

To modify:
1. Change brand name: Replace "Photo-Shoot" with your desired text
2. Adjust font size: Modify `text-2xl` to `text-3xl` for larger text or `text-xl` for smaller
3. Change color: Replace `text-gray-800` with colors like `text-blue-600` or `text-black`

### Hero Section
The main banner section contains your primary headline:

```html
<div class="text-center max-w-4xl">
    <h1 class="text-4xl md:text-6xl font-bold text-white mb-6">Photo-Shoot</h1>
    <p class="text-xl md:text-2xl text-gray-200 mb-8">Get the ultimate product photography lightbox</p>
```

To modify:
1. Update headline: Replace both instances of text within the `<h1>` tags
2. Change subheading: Modify the text within the `<p>` tags
3. Adjust spacing: Modify `mb-6` and `mb-8` (margin-bottom) values

### Features Section
Each feature card follows this structure:

```html
<div class="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-12 h-12 bg-blue-100 rounded-full flex items-center justify-center mb-6">
        <i class="fas fa-bolt text-blue-600 text-xl"></i>
    </div>
    <h3 class="text-xl font-semibold mb-4">USB Powered</h3>
    <p class="text-gray-600">Connect to any USB port for consistent, reliable power supply</p>
</div>
```

To modify:
1. Change icon: Replace `fa-bolt` with any [Font Awesome](https://fontawesome.com/icons) icon name
2. Update feature title: Modify text within `<h3>` tags
3. Update description: Change text within `<p>` tags
4. Adjust card appearance: Modify `p-8` padding or `rounded-xl` border radius

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-6">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900 transition-colors">FAQ</a>
</div>
```

To update:
1. Internal links: Keep `#` followed by section ID (e.g., `#features`)
2. External links: Replace `#` with full URL (e.g., `https://example.com`)
3. Verify links work by clicking them after updating

### Buy Now Button
The current purchase link appears multiple times:

```html
<a href="https://buy.stripe.com/14k5mM58ObjBbRK000" class="bg-blue-600 text-white px-6 py-2 rounded-full hover:bg-blue-700 transition-colors duration-300">Buy Now</a>
```

To update:
1. Search for all instances of `https://buy.stripe.com/14k5mM58ObjBbRK000`
2. Replace with your actual purchase URL
3. Test each button to ensure proper redirection

## Linking Privacy and Terms Pages

### Footer Policy Links
Current policy links structure:

```html
<div>
    <h4 class="text-white text-lg font-semibold mb-4">Policies</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors">Terms of Service</a></li>
        <li><a href="#" class="hover:text-white transition-colors">Shipping Policy</a></li>
    </ul>
</div>
```

To link policy pages:
1. Create your policy pages (e.g., `privacy.html`, `terms.html`)
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors">Terms of Service</a></li>
```
3. Ensure policy pages are in the same directory as `index.html`

## Troubleshooting

Common issues and solutions:

1. **Broken Layout**
   - Check for missing closing tags
   - Verify Tailwind CSS classes are spelled correctly
   - Ensure responsive classes (e.g., `md:`) are properly formatted

2. **Missing Icons**
   - Verify Font Awesome CDN link is present in `<head>`
   - Check icon class names against Font Awesome documentation
   - Ensure proper icon style prefix (fas, fab, far)

3. **Non-working Links**
   - Verify file paths are correct
   - Check for typos in URLs
   - Ensure linked pages exist in the specified location

Remember to:
- Test all changes in multiple browsers
- Verify responsive design on different screen sizes
- Keep backups before making significant changes
- Validate HTML using [W3C Validator](https://validator.w3.org/)
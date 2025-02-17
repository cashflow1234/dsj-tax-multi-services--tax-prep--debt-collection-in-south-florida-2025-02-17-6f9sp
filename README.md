# DSJ Tax Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the DSJ Tax landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company logo and navigation menu. To update:

```html
<!-- Logo Text -->
<div class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    DSJ Tax  <!-- Edit this text to change the logo -->
</div>

<!-- Navigation Menu Items -->
<div class="hidden md:flex space-x-8">
    <a href="#services">Services</a>  <!-- Edit these text labels -->
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
</div>
```

### Hero Section
To modify the main headline and subheading:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">
    DSJ Tax Multi-Services<br>  <!-- Edit main headline -->
    Tax Prep & Debt Collection in South Florida  <!-- Edit subheading -->
</h1>
```

### Tailwind CSS Tips
- Font sizes use this pattern: `text-[size]` (e.g., `text-xl`, `text-2xl`)
- Colors use this pattern: `[type]-[color]-[shade]` (e.g., `bg-purple-400`, `text-gray-900`)
- Spacing uses this pattern: `[property]-[amount]` (e.g., `mb-8` for margin-bottom, `py-4` for padding-y)

## Managing Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<div class="hidden md:flex space-x-8">
    <a href="#services">Services</a>
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
</div>
```

To update these links:
1. Identify the section ID you want to link to
2. Update the `href` attribute with `#` followed by the section ID
3. Example: `<a href="#new-section">New Section</a>`

### Call-to-Action Links
The main CTA form link appears multiple times:
```html
<a href="https://form.jotform.com/250476421727054" class="...">
```

To update:
1. Replace the JotForm URL with your new form URL
2. Update all instances of this link throughout the page
3. Locations to check:
   - Header "Get Started" button
   - Hero section "Start Your Tax Journey" button
   - Bottom CTA "Contact Us Now" button

## Adding Privacy and Terms Pages

### Footer Link Updates
Locate the Quick Links section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Quick Links</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-purple-400 transition-colors duration-300">Services</a></li>
        <li><a href="#" class="hover:text-purple-400 transition-colors duration-300">About Us</a></li>
        <li><a href="#" class="hover:text-purple-400 transition-colors duration-300">Privacy Policy</a></li>
    </ul>
</div>
```

To add privacy and terms pages:
1. Create new files: `privacy.html` and `terms.html`
2. Add these links to the footer:
```html
<li><a href="privacy.html" class="hover:text-purple-400 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-purple-400 transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match href attributes exactly
   - Check for typos in IDs
   - Verify that sections have the correct ID attribute

2. **Responsive Design Issues**
   - Check mobile classes (e.g., `md:`, `lg:` prefixes)
   - Test on different screen sizes
   - Verify that the viewport meta tag is present:
   ```html
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   ```

3. **Style Changes Not Applying**
   - Verify Tailwind CSS CDN link is working
   - Check class name spelling
   - Ensure classes are in the correct order for specificity

### Need Help?
If you encounter issues:
1. Use browser developer tools (F12) to inspect elements
2. Check the console for any error messages
3. Verify all changes against this original template
4. Test all links and interactions after making changes

Remember to always make a backup of your files before making significant changes.
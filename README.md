# Landing Page Maintenance Guide

This guide will help you maintain and customize your landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your main navigation and logo. To update:

1. **Logo Text**: Find this line and replace "HK Websites":
```html
<a href="/" class="text-2xl font-bold text-gray-800">HK Websites</a>
```

2. **Navigation Items**: Located in the header's `div` with class `md:flex space-x-8`:
```html
<a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
```
- Change text between `>` and `</a>`
- Keep the `href` attributes matching your section IDs

### Hero Section
Located right after the header, customize:

1. **Main Heading**:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-8">Best Websites In Hong Kong</h1>
```
- Change text while keeping the classes intact
- The classes control size (`text-4xl`), responsiveness (`md:text-5xl`), and spacing (`mb-8`)

2. **Subheading**:
```html
<p class="text-xl md:text-2xl text-gray-600 mb-12 leading-relaxed">Custom Websites For Your Business</p>
```

### Tailwind CSS Tips
- `text-{size}`: Controls text size (xl, 2xl, etc.)
- `mb-{number}`: Adds margin bottom (4, 8, 12, etc.)
- `md:`: Applies styles on medium screens and up
- `hover:`: Applies styles on mouse hover

## Managing Links

### Navigation Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. Locate the section ID you want to link to
2. Update the `href` attribute with `#` followed by the section ID
3. Example: `<a href="#new-section">New Section</a>`

### External Links
The main call-to-action buttons currently point to:
```html
<a href="https://sigmaseo.io" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg">
```

To update:
1. Replace `https://sigmaseo.io` with your desired URL
2. Test the link before deploying
3. Consider adding `target="_blank"` for external links

### Social Media Links
Located in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">
        <i class="fab fa-twitter"></i>
    </a>
    <!-- Similar for Facebook and LinkedIn -->
</div>
```

Replace `#` with your social media profile URLs.

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Add these lines to the footer's link section:
```html
<div>
    <h3 class="text-xl font-bold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Step 2: Create New Pages
1. Create `privacy.html` and `terms.html` in your root directory
2. Copy the header and footer from `index.html`
3. Add your policy content between them

## Troubleshooting

### Common Issues

1. **Broken Links**
- Check if section IDs match href attributes
- Ensure external URLs include `https://`
- Verify file names match exactly (case-sensitive)

2. **Styling Problems**
- Don't remove Tailwind CSS classes unless you're sure
- Keep responsive classes (`md:`, `lg:`) to maintain mobile compatibility
- Test on different screen sizes after changes

3. **Layout Issues**
- Maintain the container structure:
```html
<div class="container mx-auto px-6">
    <!-- Your content here -->
</div>
```
- Keep the grid system intact in features/benefits sections

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate your HTML at [W3C Validator](https://validator.w3.org/)
- Test responsiveness using browser developer tools

Remember to always backup your files before making changes and test thoroughly before deploying to production.
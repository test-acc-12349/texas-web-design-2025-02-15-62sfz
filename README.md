# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. It's written for beginners and provides step-by-step instructions for common updates.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To update:

1. Change the logo text:
```html
<!-- Find this line in the header -->
<div class="text-2xl font-bold text-blue-600">TWD</div>
```
Simply replace "TWD" with your desired text.

### Hero Section
To update the main headline and subheading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
    Texas Web Design  <!-- Replace this text -->
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-8">
    Best Websites In Texas  <!-- Replace this text -->
</p>
```

### Tailwind CSS Classes Explained
Common classes used in this template:
- `text-[size]`: Controls text size (xl, 2xl, 3xl, etc.)
- `mb-[size]`: Adds margin bottom (4, 6, 8, etc.)
- `py-[size]`: Adds padding top and bottom
- `bg-[color]`: Sets background color
- `text-[color]`: Sets text color

Example of modifying a button:
```html
<!-- Original button -->
<a href="https://twd.com" class="inline-block px-8 py-4 bg-blue-600 text-white rounded-full">

<!-- To make it green instead of blue -->
<a href="https://twd.com" class="inline-block px-8 py-4 bg-green-600 text-white rounded-full">
```

## Managing Links

### Navigation Menu Links
Current navigation links are located in the header:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update a link:
1. Locate the `<a>` tag
2. Modify the `href` attribute
3. Update the link text

Example:
```html
<!-- Change this -->
<a href="#features">Features</a>

<!-- To this -->
<a href="#services">Services</a>
```

### Call-to-Action Links
The main CTA buttons need updating in three locations:
1. Header button
2. Hero section button
3. Bottom CTA section

Find and replace all instances of:
```html
<a href="https://twd.com" class="...">
```
Replace `https://twd.com` with your actual website URL.

## Adding Privacy and Terms Pages

### Step 1: Locate the Footer Links
Find this section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Step 2: Update the Links
Replace the `#` placeholder with actual page links:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

### Step 3: Create the New Pages
1. Create `privacy.html` and `terms.html` in the same directory
2. Copy the header and footer from `index.html` to maintain consistent styling
3. Add your policy content between the header and footer

## Troubleshooting

### Common Issues

1. **Broken Links**
   - Check that all `href` attributes have correct paths
   - Ensure internal links start with `#` for section IDs
   - Verify external links include `https://`

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - Keep the viewport meta tag in the head section
   - Test on multiple screen sizes

3. **Animation Problems**
   - Verify AOS script is loaded at the bottom of the page
   - Check `data-aos` attributes are spelled correctly
   - Ensure AOS initialization script is present:
```html
<script>
    AOS.init({
        duration: 800,
        offset: 100,
        once: true
    });
</script>
```

For additional help, refer to:
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [AOS Documentation](https://michalsnik.github.io/aos/)

Remember to always test your changes across different devices and browsers before publishing updates.
# Elwood Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Elwood Accounting Services landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To modify:

1. **Company Name:**
```html
<div class="text-2xl font-bold bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent">
    Elwood <!-- Change company name here -->
</div>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Services</a> <!-- Update menu text here -->
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent">
    Beyond compliance: strategic accounting that drives growth
    <!-- Update main headline here -->
</h1>
```

**Styling Tip:** The text sizes (`text-4xl`, `md:text-5xl`, `lg:text-6xl`) create responsive typography. Don't remove these classes unless you're replacing them with similar responsive sizes.

### Features Section
To modify service cards:

1. Locate the `features` section:
```html
<div class="grid grid-cols-1 md:grid-cols-3 gap-12">
    <div class="bg-white rounded-2xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
        <!-- Each card follows this structure -->
        <h3 class="text-xl font-semibold mb-4">CFO Advisory</h3>
        <p class="text-gray-600 leading-relaxed">Strategic financial guidance...</p>
    </div>
</div>
```

2. To add or modify features:
   - Copy an existing card div
   - Update the heading and description
   - Maintain the class structure for consistent styling

## Managing Links

### Navigation Links
Current internal links use anchor tags (#):
```html
<a href="#features">Services</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. For internal sections: Keep the `#` prefix with the section's ID
2. For external pages: Replace with full URL
   ```html
   <a href="https://your-website.com/services">Services</a>
   ```

### Call-to-Action Links
Located in multiple sections, currently pointing to placeholder URL:
```html
<a href="https://theaccountants.com" class="px-8 py-4 bg-gradient-to-r...">
    Start Your Journey
</a>
```

To update:
1. Replace `https://theaccountants.com` with your actual URL
2. Test the link after updating
3. Maintain the existing classes for consistent styling

### Email Links
Located in the contact section:
```html
<a href="mailto:contact@example.com">Email Us</a>
```

Update to your actual email address:
```html
<a href="mailto:your.actual@email.com">Email Us</a>
```

## Adding Privacy and Terms Pages

### Current Footer Links
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Steps to Add Policy Pages:

1. Create new HTML files:
   - Create `privacy.html`
   - Create `terms.html`

2. Update the footer links:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues:

1. **Broken Layout:**
   - Check that you haven't removed important Tailwind classes
   - Verify all `div` tags are properly closed
   - Maintain the responsive classes (`md:`, `lg:` prefixes)

2. **Links Not Working:**
   - Verify file paths are correct
   - Ensure internal links match section IDs exactly
   - Test all external URLs

3. **Gradient Text Not Showing:**
   - Keep all classes in the gradient text:
   ```html
   bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent
   ```

### Need Help?
- Always test changes in multiple browsers
- Use browser developer tools (F12) to inspect elements
- Make one change at a time and test
- Keep a backup of the original code

Remember to maintain the responsive design by keeping the Tailwind CSS classes intact. If you're unsure about a change, test it in both mobile and desktop views before finalizing.
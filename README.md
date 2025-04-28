# Landing Page Maintenance Guide
## 101Headshots Corporate Photography Website

This guide provides detailed instructions for maintaining and customizing the 101Headshots landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<a href="/" class="text-2xl font-bold text-gray-900">101Headshots</a>
```
- Replace "101Headshots" with your company name
- Keep the classes to maintain styling

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Services</a>
    <!-- Additional menu items -->
</div>
```
- Update text between `<a>` tags
- Maintain the `hidden md:flex` class for mobile responsiveness

### Hero Section
Located at the top of the page:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold tracking-tight text-gray-900 mb-8">
    Smithville, Missouri Corporate Headshot Photography Services
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Capturing professional spirit of Smithville's business community.
</p>
```
- Update heading and paragraph text
- Keep responsive text classes (`text-4xl md:text-5xl lg:text-6xl`)
- Maintain spacing classes (`mb-8`, `mb-12`)

### Tailwind CSS Class Guide
Common classes used throughout:
- Text sizes: `text-xl`, `text-2xl`, etc.
- Colors: `text-gray-900`, `bg-blue-600`
- Spacing: `px-6`, `py-4`, `mb-8`
- Responsive prefixes: `md:`, `lg:`

## Managing Links

### Navigation Links
Current internal links:
```html
<a href="#services">Services</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. Identify the section ID you want to link to
2. Update the `href` attribute with `#section-id`
3. Ensure the target section has matching `id` attribute

### External Links
Book Now button example:
```html
<a href="https://www.101headshots.com" class="inline-flex items-center justify-center px-6 py-2 border border-transparent text-base font-medium rounded-md text-white bg-blue-600 hover:bg-blue-700">
    Book Now
</a>
```
To update:
1. Replace `https://www.101headshots.com` with your booking URL
2. Test the link after updating

### Social Media Links
Located in the footer:
```html
<li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Facebook</a></li>
<li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Instagram</a></li>
<li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">LinkedIn</a></li>
```
Replace `#` with your social media profile URLs

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Add these lines to the footer's Quick Links section:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

### Step 2: Create New Pages
1. Create `privacy.html` and `terms.html` in your root directory
2. Copy the header and footer from `index.html`
3. Add your policy content between them
4. Maintain consistent styling using the same Tailwind classes

## Troubleshooting

### Common Issues:

1. **Broken Internal Links**
- Verify that section IDs match href attributes
- Check for typos in IDs
- Ensure sections have unique IDs

2. **Responsive Design Issues**
- Keep responsive class prefixes (`md:`, `lg:`)
- Test on multiple screen sizes
- Don't remove `hidden md:flex` from navigation

3. **Styling Problems**
- Maintain class order for proper specificity
- Keep utility classes that control spacing
- Don't remove transition classes for hover effects

### Need Help?
- Check Tailwind CSS documentation for class references
- Verify all links work in multiple browsers
- Test responsive design using browser dev tools
- Maintain backup copies before making changes

Remember to test all changes thoroughly before deploying to your live site.
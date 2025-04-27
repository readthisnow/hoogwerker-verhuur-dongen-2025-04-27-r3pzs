# Landing Page Maintenance Guide

This guide will help you maintain and customize the Hoogwerker Verhuur Dongen landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text (HVD)**:
```html
<a href="/" class="text-2xl font-bold text-blue-600">HVD</a>
```
- Replace "HVD" with your desired logo text
- Adjust size using `text-2xl` (options: text-sm, text-lg, text-3xl, etc.)
- Change color using `text-blue-600` (options: text-red-600, text-green-600, etc.)

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl sm:text-5xl lg:text-6xl font-bold text-gray-900 mb-8">
    Hoogwerker Verhuur Dongen
</h1>
```
To modify:
1. Replace the text between `<h1>` tags
2. Adjust responsive text sizes:
   - Mobile: `text-4xl`
   - Tablet: `sm:text-5xl`
   - Desktop: `lg:text-6xl`

### Promotional Text
To update the discount message:
```html
<p class="text-xl sm:text-2xl text-blue-600 font-semibold mb-8">
    🎉 Tijdelijk 10% Korting op alle verhuur!
</p>
```
- Change percentage by editing "10%"
- Modify emoji by replacing "🎉"
- Adjust color using `text-blue-600`

## Managing Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Diensten</a>
    <a href="#benefits">Voordelen</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. Internal links (same page):
   - Use `#section-name` format
   - Ensure section IDs match (e.g., `id="features"`)

2. External links:
   - Replace `href="#section-name"` with full URL
   - Example: `href="https://example.com/page"`

### Call-to-Action Buttons
Current reservation button:
```html
<a href="https://hansschuiling.nl" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg">
    Direct Reserveren
</a>
```
To modify:
1. Update `href` with your booking URL
2. Change button text between `<a>` tags
3. Adjust styling:
   - Background color: `bg-blue-600`
   - Text color: `text-white`
   - Padding: `px-8 py-4`
   - Border radius: `rounded-lg`

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the footer:

```html
<div class="border-t border-gray-800 mt-12 pt-8 text-sm text-gray-400">
    <p>&copy; 2024 Hoogwerker Verhuur Dongen. Alle rechten voorbehouden.</p>
    <!-- Add these lines below the copyright notice -->
    <div class="mt-4 space-x-4">
        <a href="/privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a>
        <a href="/terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a>
    </div>
</div>
```

### Creating Policy Pages
1. Create new files:
   - `privacy.html`
   - `terms.html`

2. Use this basic template for each:
```html
<!DOCTYPE html>
<html lang="nl" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Privacy Policy - Hoogwerker Verhuur Dongen</title>
    <link href="https://unpkg.com/tailwindcss@^2/dist/tailwind.min.css" rel="stylesheet">
</head>
<body class="font-inter antialiased bg-white text-gray-900">
    <!-- Copy header from index.html -->
    
    <!-- Add your policy content here -->
    
    <!-- Copy footer from index.html -->
</body>
</html>
```

## Troubleshooting

### Common Issues

1. **Broken Links**
   - Check for typos in `href` attributes
   - Verify file names match exactly
   - Ensure files are in the correct directory

2. **Styling Problems**
   - Confirm Tailwind CSS is properly loaded
   - Check for missing or mistyped classes
   - Verify responsive classes use correct prefixes (sm:, md:, lg:)

3. **Layout Issues**
   - Check container classes: `container mx-auto px-4`
   - Verify grid classes: `grid grid-cols-1 md:grid-cols-2`
   - Ensure proper spacing classes (margin/padding)

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Check browser developer tools (F12) for errors
- Validate HTML at [W3C Validator](https://validator.w3.org/)

Remember to test all changes across different devices and screen sizes before publishing updates to your live site.
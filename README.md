# Modern Landing Page - Maintenance Guide

This guide will help you maintain and customize the landing page, even if you're new to web development. Follow these detailed instructions to make common updates while preserving the design integrity.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text:**
```html
<a href="#" class="text-2xl font-bold text-indigo-600">Logo</a>
```
Replace "Logo" with your company name. The `text-2xl` class controls size, and `text-indigo-600` sets the color.

2. **Navigation Items:**
```html
<a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-200">Home</a>
```
Update the text between `<a>` tags for each navigation item. Keep the classes to maintain hover effects.

### Hero Section
Located at the top of the page:

1. **Main Heading:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold tracking-tight text-gray-900 mb-8">
    Welcome to Our Modern Platform
</h1>
```
Replace the heading text while keeping the classes. The different `text-*xl` classes ensure proper sizing across devices.

2. **Subheading:**
```html
<p class="text-xl text-gray-600 max-w-2xl mx-auto mb-12">
    Transform your digital experience...
</p>
```
Update the paragraph text between the `<p>` tags.

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-12 h-12 bg-indigo-100 rounded-xl flex items-center justify-center mb-6">
        <!-- Icon SVG here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Lightning Fast</h3>
    <p class="text-gray-600">Experience blazing fast performance...</p>
</div>
```
To add new features:
1. Copy the entire feature card `<div>`
2. Paste it within the grid container
3. Update the heading and description text
4. Modify the icon SVG as needed

## Managing Links

### Updating Navigation Links
Current placeholder links are marked with `#`. Replace them as follows:

1. Find all `href="#"` attributes in the navigation:
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#" class="text-gray-600">Home</a>
    <a href="#" class="text-gray-600">Features</a>
    <!-- etc. -->
</div>
```

2. Replace `#` with proper URLs:
- For internal pages: `href="about.html"`
- For external links: `href="https://example.com"`

### Footer Links
The footer contains multiple columns of links:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white">About</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white">Careers</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white">Blog</a></li>
</ul>
```
Update each `href="#"` with the appropriate URL while maintaining the classes.

## Adding Privacy and Terms Pages

### Step 1: Create New Footer Column
Add this code within the footer's grid:
```html
<div>
    <h3 class="text-xl font-bold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-200">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-200">Terms of Service</a></li>
    </ul>
</div>
```

### Step 2: Style Consistency
Ensure new links match existing styling:
- Use `text-gray-400` for normal state
- Include `hover:text-white` for hover effect
- Keep `transition-colors duration-200` for smooth transitions

## Troubleshooting

### Common Issues

1. **Broken Responsive Design:**
- Check that you haven't removed important Tailwind classes like `md:` or `lg:` prefixes
- Verify that the grid classes (`grid-cols-*`) remain intact

2. **Inconsistent Spacing:**
- Look for missing `mb-*`, `py-*`, or `px-*` classes
- Ensure `space-y-*` and `space-x-*` classes are preserved in lists

3. **Missing Hover Effects:**
- Verify `hover:` classes are present
- Check `transition-*` classes are included

### Tips
- Always test changes across different screen sizes
- Keep the original class structure when adding new elements
- Use browser inspection tools to understand spacing and styling
- Make one change at a time and test before proceeding

Remember to maintain the responsive design by keeping all Tailwind CSS classes intact when making updates. If you're unsure about a class's purpose, refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).
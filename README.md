# Test Calgary Landing Page - Maintenance & Customization Guide

A comprehensive guide for maintaining, updating, and customizing your Test Calgary landing page. This document covers everything from updating text content to fixing links and adding policy pages.

---

## Table of Contents

1. [Understanding the Page Structure](#understanding-the-page-structure)
2. [Updating Text and Content](#updating-text-and-content)
3. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
4. [Fixing and Updating Links](#fixing-and-updating-links)
5. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
6. [Troubleshooting Common Issues](#troubleshooting-common-issues)
7. [Best Practices](#best-practices)

---

## Understanding the Page Structure

Before making any changes, it's helpful to understand how your landing page is organized.

### Main Sections of Your Page

Your `index.html` file contains these major sections:

| Section | Purpose | Location in Code |
|---------|---------|------------------|
| **Header & Navigation** | Top menu bar that stays visible | Lines 45-85 |
| **Hero Section** | Large welcome section with main message | Lines 87-140 |
| **Features Section** | 6 feature cards explaining benefits | Lines 142-237 |
| **Benefits Section** | 6 benefit cards with icons | Lines 239-325 |
| **Trust & Credibility** | 3 trust indicator cards | Lines 327-358 |
| **Testimonials Section** | 4 customer testimonial cards | Lines 360-430 |
| **About Us Section** | Company information and statistics | Lines 432-475 |
| **Call-to-Action Section** | Large banner encouraging action | Lines 477-505 |
| **Footer** | Bottom section with links and info | Lines 507-600 |

### Key Concepts to Know

**What is HTML?**
HTML is the language that structures web page content. Think of it as the "skeleton" of your page—it holds all the text, images, and links.

**What are Tailwind CSS Classes?**
Tailwind CSS classes are shortcuts that control how your page looks (colors, spacing, sizes, etc.). Instead of writing complex code, you use pre-made class names like `text-purple-600` or `px-8`.

---

## Updating Text and Content

### 1. Changing the Company Name

Your landing page currently uses "Test Calgary" throughout. To change this to a different name:

**Step 1: Find the Logo Text in the Header**

Locate this code in your file (around line 54):

```html
<span class="text-2xl font-bold text-gray-900">Test Calgary</span>
```

**Step 2: Replace the Text**

Change `Test Calgary` to your desired name. For example:

```html
<span class="text-2xl font-bold text-gray-900">Premier Assessment Center</span>
```

**Step 3: Update the Footer Logo**

Find this code around line 539:

```html
<span class="text-xl font-bold text-white">Test Calgary</span>
```

Replace it with your new name:

```html
<span class="text-xl font-bold text-white">Premier Assessment Center</span>
```

**Step 4: Update the Page Title**

Find this line near the top (line 7):

```html
<title>Unlock Your Potential: Calgary's Premier Testing Center</title>
```

Change it to match your business:

```html
<title>Unlock Your Potential: Your City's Premier Testing Center</title>
```

**Why This Matters:**
- The page title appears in browser tabs and search results
- Consistency helps brand recognition
- Search engines use this title to understand your page

---

### 2. Updating the Hero Section (Main Welcome Message)

The hero section is the large banner at the top of your page with the main headline.

**Step 1: Change the Main Headline**

Find this code around line 98:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight tracking-tight mb-6">
    Unlock Your <span class="gradient-accent bg-clip-text text-transparent">Potential</span>
</h1>
```

You can replace "Unlock Your Potential" with your own message. For example:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight tracking-tight mb-6">
    Achieve Your <span class="gradient-accent bg-clip-text text-transparent">Goals</span>
</h1>
```

**Important:** Keep the `<span class="gradient-accent bg-clip-text text-transparent">` tags around one word if you want that purple gradient effect. Remove them if you don't want the gradient.

**Step 2: Change the Subtitle (Description)**

Find this code around line 103:

```html
<p class="text-xl text-gray-700 leading-relaxed mb-8">
    Achieve your goals with our comprehensive suite of testing services. From academic assessments to professional certifications, we provide the resources and support you need to succeed.
</p>
```

Replace this with your own description:

```html
<p class="text-xl text-gray-700 leading-relaxed mb-8">
    Your success is our mission. We provide expert guidance and world-class facilities to help you excel in your exams and certifications.
</p>
```

**Step 3: Change Button Text**

Find the main "Call-to-Action" button around line 108:

```html
<a href="https://example.com" class="px-8 py-4 bg-purple-600 text-white rounded-lg hover:bg-purple-700 transition-all duration-300 hover:scale-105 font-bold text-lg shadow-lg hover:shadow-xl inline-flex items-center justify-center">
    <i class="fas fa-arrow-right mr-2"></i> Start Your Journey
</a>
```

Change "Start Your Journey" to something else:

```html
<a href="https://example.com" class="px-8 py-4 bg-purple-600 text-white rounded-lg hover:bg-purple-700 transition-all duration-300 hover:scale-105 font-bold text-lg shadow-lg hover:shadow-xl inline-flex items-center justify-center">
    <i class="fas fa-arrow-right mr-2"></i> Book Your Test Now
</a>
```

**Understanding the Button Code:**
- `href="https://example.com"` - This is where the button links to (we'll fix this later)
- `bg-purple-600` - This makes the button purple
- `text-white` - This makes the text white
- `rounded-lg` - This rounds the corners
- The icon `<i class="fas fa-arrow-right mr-2"></i>` adds the arrow symbol

---

### 3. Updating Feature Cards

Your page has 6 feature cards. Each one has a title, description, and bullet points.

**Example: Updating the First Feature Card**

Find this code around line 160:

```html
<div class="feature-card bg-white border border-gray-200 rounded-xl p-8 hover:border-purple-300">
    <div class="w-14 h-14 bg-purple-100 rounded-lg flex items-center justify-center mb-6">
        <i class="fas fa-microscope text-purple-600 text-2xl"></i>
    </div>
    <h3 class="text-2xl font-bold text-gray-900 mb-3">Precise Assessment</h3>
    <p class="text-gray-600 leading-relaxed mb-4">
        Our state-of-the-art facilities and experienced proctors ensure accurate and reliable test results...
    </p>
    <ul class="space-y-2 text-sm text-gray-700">
        <li class="flex items-center"><i class="fas fa-check text-green-500 mr-2"></i> Advanced testing equipment</li>
        <li class="flex items-center"><i class="fas fa-check text-green-500 mr-2"></i> Certified proctors</li>
        <li class="flex items-center"><i class="fas fa-check text-green-500 mr-2"></i> Quality assurance protocols</li>
    </ul>
</div>
```

**To Change the Title:**

```html
<h3 class="text-2xl font-bold text-gray-900 mb-3">Your New Title Here</h3>
```

**To Change the Description:**

```html
<p class="text-gray-600 leading-relaxed mb-4">
    Your new description text goes here. Keep it clear and helpful.
</p>
```

**To Change the Bullet Points:**

```html
<ul class="space-y-2 text-sm text-gray-700">
    <li class="flex items-center"><i class="fas fa-check text-green-500 mr-2"></i> Your first benefit</li>
    <li class="flex items-center"><i class="fas fa-check text-green-500 mr-2"></i> Your second benefit</li>
    <li class="flex items-center"><i class="fas fa-check text-green-500 mr-2"></i> Your third benefit</li>
</ul>
```

**To Change the Icon:**

The icon is controlled by this line:

```html
<i class="fas fa-microscope text-purple-600 text-2xl"></i>
```

Visit [Font Awesome Icons](https://fontawesome.com/icons) to find different icons. For example:
- `fa-microscope` → `fa-check-circle` (checkmark circle)
- `fa-microscope` → `fa-star` (star)
- `fa-microscope` → `fa-trophy` (trophy)

Replace `fa-microscope` with your chosen icon name:

```html
<i class="fas fa-check-circle text-purple-600 text-2xl"></i>
```

---

### 4. Updating Testimonials

Find the testimonials section around line 380. Here's an example testimonial:

```html
<div class="bg-white rounded-xl shadow-md p-8 hover:shadow-lg transition-all duration-300 hover-lift">
    <div class="flex items-center mb-4">
        <div class="flex text-yellow-400">
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
        </div>
        <span class="ml-2 text-sm font-semibold text-gray-700">(5.0)</span>
    </div>
    <p class="text-gray-700 leading-relaxed mb-6">
        "Test Calgary provided a seamless and stress-free testing experience..."
    </p>
    <div class="border-t border-gray-200 pt-4">
        <p class="font-bold text-gray-900">Sarah Chen</p>
        <p class="text-sm text-gray-600">Marketing Manager, Innovate Solutions</p>
    </div>
</div>
```

**To Change the Testimonial Text:**

```html
<p class="text-gray-700 leading-relaxed mb-6">
    "Your new testimonial text goes here. Make it personal and specific."
</p>
```

**To Change the Person's Name:**

```html
<p class="font-bold text-gray-900">New Person's Name</p>
```

**To Change the Job Title and Company:**

```html
<p class="text-sm text-gray-600">Their Job Title, Their Company Name</p>
```

**To Change the Star Rating:**

If you want fewer stars, simply remove star icons:

```html
<div class="flex text-yellow-400">
    <i class="fas fa-star"></i>
    <i class="fas fa-star"></i>
    <i class="fas fa-star"></i>
    <i class="fas fa-star"></i>
    <!-- Remove this line for 4 stars instead of 5 -->
    <!-- <i class="fas fa-star"></i> -->
</div>
```

---

### 5. Updating Footer Contact Information

Find the footer around line 560:

```html
<li class="flex items-start">
    <i class="fas fa-envelope text-purple-400 mr-3 mt-1"></i>
    <span class="text-gray-400">
        <a href="mailto:test@test.com" class="hover:text-purple-400 transition-colors duration-300">test@test.com</a>
    </span>
</li>
```

**To Change the Email:**

Replace `test@test.com` with your email address (in TWO places):

```html
<li class="flex items-start">
    <i class="fas fa-envelope text-purple-400 mr-3 mt-1"></i>
    <span class="text-gray-400">
        <a href="mailto:your-email@yourcompany.com" class="hover:text-purple-400 transition-colors duration-300">your-email@yourcompany.com</a>
    </span>
</li>
```

**To Change the Address:**

Find this code around line 570:

```html
<li class="flex items-start">
    <i class="fas fa-map-marker-alt text-purple-400 mr-3 mt-1"></i>
    <span class="text-gray-400">Calgary, Alberta, Canada</span>
</li>
```

Replace with your location:

```html
<li class="flex items-start">
    <i class="fas fa-map-marker-alt text-purple-400 mr-3 mt-1"></i>
    <span class="text-gray-400">123 Main Street, Your City, Your Province, Canada</span>
</li>
```

**To Change the Hours:**

Find this code around line 575:

```html
<li class="flex items-start">
    <i class="fas fa-clock text-purple-400 mr-3 mt-1"></i>
    <span class="text-gray-400">Mon - Fri: 8am - 6pm<br>Sat - Sun: 9am - 4pm</span>
</li>
```

Replace with your actual hours:

```html
<li class="flex items-start">
    <i class="fas fa-clock text-purple-400 mr-3 mt-1"></i>
    <span class="text-gray-400">Mon - Fri: 9am - 5pm<br>Sat: 10am - 3pm<br>Sun: Closed</span>
</li>
```

---

## Modifying Tailwind CSS Classes

Tailwind CSS uses simple class names to control styling. Here's how to modify them without breaking your design.

### Understanding Tailwind Classes Used in This Page

#### Color Classes

Your page uses colors in this format: `color-intensity`

```
bg-purple-600    = purple background, intensity 600 (medium-dark)
text-white       = white text
text-gray-900    = very dark gray text
bg-purple-100    = light purple background
```

**Available Colors:**
- `purple`, `blue`, `green`, `red`, `orange`, `yellow`, `pink`, `gray`, `white`

**Available Intensities:**
- `50` (lightest), `100`, `200`, `300`, `400`, `500`, `600`, `700`, `800`, `900` (darkest)

#### Spacing Classes

```
p-8      = padding (internal space) of 8 units
px-8     = padding left and right of 8 units
py-4     = padding top and bottom of 4 units
mb-6     = margin-bottom (space below) of 6 units
gap-8    = space between items of 8 units
```

#### Text Classes

```
text-xl           = extra large text
text-2xl          = 2x large text
font-bold         = bold text
leading-relaxed   = comfortable line spacing
tracking-tight    = tight letter spacing
```

#### Layout Classes

```
rounded-lg        = slightly rounded corners
rounded-xl        = more rounded corners
shadow-md         = medium shadow
hover:bg-purple-700 = purple background when you hover over it
transition-all    = smooth animation when hovering
```

### Common Customizations

#### Changing the Primary Color (Purple to Blue)

To change your accent color from purple to blue throughout the page:

**Find all instances of:**
```html
bg-purple-600
```

**Replace with:**
```html
bg-blue-600
```

Do this for all purple color classes:
- `gradient-accent` (uses purple in CSS)
- `bg-purple-100`, `bg-purple-200`, `bg-purple-600`, `bg-purple-700`
- `text-purple-600`, `text-purple-400`
- `hover:bg-purple-50`, `hover:bg-purple-700`
- `hover:text-purple-600`, `hover:text-purple-400`
- `border-purple-300`, `border-purple-600`

**Note:** The `gradient-accent` class is defined in the `<style>` section (lines 18-20). To change it, find:

```css
.gradient-accent {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}
```

And replace with a blue gradient:

```css
.gradient-accent {
    background: linear-gradient(135deg, #3b82f6 0%, #1e40af 100%);
}
```

#### Making Text Larger

Find any text size class like:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl ...">
```

The sizes mean:
- `text-4xl` = large (on small screens)
- `md:text-5xl` = extra large (on medium screens)
- `lg:text-6xl` = 2x large (on large screens)

To make it bigger:
```html
<h1 class="text-5xl md:text-6xl lg:text-7xl ...">
```

#### Increasing Padding/Spacing

Find spacing classes like:
```html
<div class="p-8 ...">
```

To add more space inside:
```html
<div class="p-12 ...">
```

Or for more space between elements:
```html
<div class="gap-8 ...">
```

Change to:
```html
<div class="gap-12 ...">
```

#### Changing Border Radius (Corner Roundness)

Find classes like:
```html
<div class="rounded-lg ...">
```

Options:
- `rounded-none` = no rounding (sharp corners)
- `rounded-sm` = slightly rounded
- `rounded` = moderately rounded
- `rounded-lg` = more rounded
- `rounded-xl` = very rounded
- `rounded-2xl` = extremely rounded
- `rounded-full` = completely round (circle if square)

---

### Responsive Design Classes

Your page uses responsive design, which means it looks good on phones, tablets, and computers.

Classes like `md:` and `lg:` control what happens on different screen sizes:

```html
<div class="text-base md:text-lg lg:text-xl">
```

This means:
- `text-base` = normal size on small screens (phones)
- `md:text-lg` = larger on medium screens (tablets)
- `lg:text-xl` = even larger on large screens (desktops)

**Common breakpoints:**
- `sm:` = screens 640px and up (small tablets)
- `md:` = screens 768px and up (medium tablets)
- `lg:` = screens 1024px and up (desktops)
- `xl:` = screens 1280px and up (large desktops)

**Example: Making Something Hidden on Mobile**

```html
<div class="hidden lg:flex">
    This only shows on large screens
</div>
```

---

## Fixing and Updating Links

Your landing page has several links that need to be updated. Let's go through each one systematically.

### 1. Navigation Menu Links

These are in the header at the top of the page.

**Location:** Lines 62-67 (Desktop Menu) and Lines 76-81 (Mobile Menu)

**Current Code:**

```html
<!-- Desktop Menu -->
<div class="hidden md:flex items-center space-x-8">
    <a href="#features" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">Features</a>
    <a href="#benefits" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">Benefits</a>
    <a href="#testimonials" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">Testimonials</a>
    <a href="#about" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">About</a>
    <a href="https://example.com" class="px-6 py-2 bg-purple-600 text-white rounded-lg hover:bg-purple-700 transition-all duration-300 hover:scale-105 font-medium">Get Started</a>
</div>
```

**What Each Link Does:**

- `href="#features"` → Scrolls to the Features section
- `href="#benefits"` → Scrolls to the Benefits section
- `href="#testimonials"` → Scrolls to the Testimonials section
- `href="#about"` → Scrolls to the About section
- `href="https://example.com"` → ⚠️ **NEEDS TO BE FIXED** - This is a placeholder

**To Fix the "Get Started" Button:**

Replace `https://example.com` with your actual booking/signup page:

```html
<a href="https://yourbookingsite.com/booking" class="px-6 py-2 bg-purple-600 text-white rounded-lg hover:bg-purple-700 transition-all duration-300 hover:scale-105 font-medium">Get Started</a>
```

**Important:** You need to update this link in THREE places:
1. Desktop menu (line 67)
2. Mobile menu (line 81)
3. Hero section button (line 108)
4. CTA section button (line 495)

**Step-by-Step Instructions:**

**Step 1:** Open your `index.html` file in a text editor (like Notepad or VS Code)

**Step 2:** Use Ctrl+F (or Cmd+F on Mac) to find all instances:

```
https://example.com
```

**Step 3:** Replace each one with your actual URL. For example, if you use Calendly:

```
https://calendly.com/yourname
```

Or if you have a booking page on your website:

```
https://yourwebsite.com/book-test
```

**Step 4:** Save your file (Ctrl+S or Cmd+S)

---

### 2. Footer Navigation Links

**Location:** Lines 542-547

**Current Code:**

```html
<!-- Quick Links -->
<div>
    <h3 class="text-lg font-bold text-white mb-6">Quick Links</h3>
    <ul class="space-y-3">
        <li><a href="#features" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Features</a></li>
        <li><a href="#benefits" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Benefits</a></li>
        <li><a href="#testimonials" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Testimonials</a></li>
        <li><a href="#about" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">About Us</a></li>
    </ul>
</div>
```

These links are correct—they scroll to sections on this page. No changes needed here.

---

### 3. Footer Service Links

**Location:** Lines 549-556

**Current Code:**

```html
<!-- Services -->
<div>
    <h3 class="text-lg font-bold text-white mb-6">Services</h3>
    <ul class="space-y-3">
        <li><a href="#" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Academic Testing</a></li>
        <li><a href="#" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Professional Certifications</a></li>
        <li><a href="#" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Test Preparation</a></li>
        <li><a href="#" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Score Reports</a></li>
    </ul>
</div>
```

**Problem:** All links point to `#` which means they don't go anywhere.

**Solution:** Update these to point to your actual service pages. For example:

```html
<!-- Services -->
<div>
    <h3 class="text-lg font-bold text-white mb-6">Services</h3>
    <ul class="space-y-3">
        <li><a href="/services/academic-testing" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Academic Testing</a></li>
        <li><a href="/services/professional-certifications" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Professional Certifications</a></li>
        <li><a href="/services/test-preparation" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Test Preparation</a></li>
        <li><a href="/services/score-reports" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Score Reports</a></li>
    </ul>
</div>
```

**Or if these pages are on a different domain:**

```html
<li><a href="https://yourwebsite.com/academic-testing" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Academic Testing</a></li>
```

---

### 4. Footer Social Media Links

**Location:** Lines 533-546

**Current Code:**

```html
<div class="flex space-x-4">
    <a href="#" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-purple-600 transition-all duration-300" aria-label="Facebook">
        <i class="fab fa-facebook-f text-white"></i>
    </a>
    <a href="#" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-purple-600 transition-all duration-300" aria-label="Twitter">
        <i class="fab fa-twitter text-white"></i>
    </a>
    <a href="#" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-purple-600 transition-all duration-300" aria-label="LinkedIn">
        <i class="fab fa-linkedin-in text-white"></i>
    </a>
    <a href="#" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-purple-600 transition-all duration-300" aria-label="Instagram">
        <i class="fab fa-instagram text-white"></i>
    </a>
</div>
```

**Problem:** All links point to `#` and don't go anywhere.

**Solution:** Replace with your actual social media profiles. For example:

```html
<div class="flex space-x-4">
    <a href="https://facebook.com/testcalgary" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-purple-600 transition-all duration-300" aria-label="Facebook">
        <i class="fab fa-facebook-f text-white"></i>
    </a>
    <a href="https://twitter.com/testcalgary" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-purple-600 transition-all duration-300" aria-label="Twitter">
        <i class="fab fa-twitter text-white"></i>
    </a>
    <a href="https://linkedin.com/company/testcalgary" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-purple-600 transition-all duration-300" aria-label="LinkedIn">
        <i class="fab fa-linkedin-in text-white"></i>
    </a>
    <a href="https://instagram.com/testcalgary" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-purple-600 transition-all duration-300" aria-label="Instagram">
        <i class="fab fa-instagram text-white"></i>
    </a>
</div>
```

**If you don't have a social media account:**

Simply remove that icon's entire `<a>` block. For example, if you don't have LinkedIn:

```html
<div class="flex space-x-4">
    <a href="https://facebook.com/testcalgary" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-purple-600 transition-all duration-300" aria-label="Facebook">
        <i class="fab fa-facebook-f text-white"></i>
    </a>
    <a href="https://twitter.com/testcalgary" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-purple-600 transition-all duration-300" aria-label="Twitter">
        <i class="fab fa-twitter text-white"></i>
    </a>
    <!-- LinkedIn removed -->
    <a href="https://instagram.com/testcalgary" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-purple-600 transition-all duration-300" aria-label="Instagram">
        <i class="fab fa-instagram text-white"></i>
    </a>
</div>
```

---

### 5. Footer Copyright and Policy Links

**Location:** Lines 586-595

**Current Code:**

```html
<div class="flex flex-wrap gap-6 md:justify-end">
    <a href="privacy.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm">Privacy Policy</a>
    <a href="terms.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm">Terms of Service</a>
    <a href="blog.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm">Blog</a>
</div>
```

These links point to files that don't exist yet (`privacy.html`, `terms.html`, `blog.html`). We'll create these in the next section.

---

### Summary of All Links to Update

| Link | Current Value | What to Change It To |
|------|---------------|----------------------|
| Get Started (Header) | `https://example.com` | Your booking URL |
| Get Started (Hero) | `https://example.com` | Your booking URL |
| Get Started (CTA) | `https://example.com` | Your booking URL |
| Learn More (Hero) | `#features` | ✅ Correct (no change) |
| Book Your Test (CTA) | `https://example.com` | Your booking URL |
| Services Links | `#` | Your service page URLs |
| Social Media Links | `#` | Your actual social profiles |
| Privacy Policy | `privacy.html` | ✅ Correct (will create file) |
| Terms of Service | `terms.html` | ✅ Correct (will create file) |
| Blog | `blog.html` | Your blog URL or remove |

---

## Adding Privacy and Terms Pages

Your footer already has links to `privacy.html` and `terms.html`, but these files don't exist yet. Let's create them.

### Understanding What These Pages Are

- **Privacy Policy:** Explains how you collect and use visitor information
- **Terms of Service:** Explains the rules for using your service
- **Blog:** Optional page for sharing articles and updates

These are important legal documents that protect both you and your customers.

---

### Method 1: Creating a Simple Privacy Policy Page

**Step 1: Create a New File**

1. Open your text editor (Notepad, VS Code, etc.)
2. Click **File → New**
3. Save it as `privacy.html` in the same folder as your `index.html`

**Step 2: Copy This Template**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - Test Calgary">
    <title>Privacy Policy - Test Calgary</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white text-gray-900 font-sans">
    <!-- Header & Navigation -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16">
                <div class="flex items-center">
                    <div class="flex items-center space-x-2">
                        <div class="w-10 h-10 bg-purple-600 rounded-lg flex items-center justify-center">
                            <i class="fas fa-check text-white text-lg"></i>
                        </div>
                        <span class="text-2xl font-bold text-gray-900">Test Calgary</span>
                    </div>
                </div>
                <a href="index.html" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">Back to Home</a>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <main class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 py-20">
        <h1 class="text-4xl font-bold text-gray-900 mb-8">Privacy Policy</h1>
        
        <div class="prose prose-lg max-w-none text-gray-700 space-y-6">
            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">Introduction</h2>
                <p>
                    Test Calgary ("we," "us," or "our") operates the Test Calgary website and testing center. This page informs you of our policies regarding the collection, use, and disclosure of personal data when you use our service and the choices you have associated with that data.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">Information Collection and Use</h2>
                <p>
                    We collect several different types of information for various purposes to provide and improve our service to you.
                </p>
                <h3 class="text-xl font-semibold text-gray-900 mt-6 mb-3">Types of Data Collected:</h3>
                <ul class="list-disc list-inside space-y-2 ml-4">
                    <li><strong>Personal Data:</strong> When you register for a test, we collect information such as your name, email address, phone number, and test preferences.</li>
                    <li><strong>Test Results:</strong> We securely store your test scores and assessment results.</li>
                    <li><strong>Usage Data:</strong> We collect information about how you interact with our website, including pages visited and time spent.</li>
                    <li><strong>Device Information:</strong> We collect information about the device you use to access our service.</li>
                </ul>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">Use of Data</h2>
                <p>Test Calgary uses the collected data for various purposes:</p>
                <ul class="list-disc list-inside space-y-2 ml-4">
                    <li>To provide and maintain our service</li>
                    <li>To notify you about changes to our service</li>
                    <li>To allow you to participate in interactive features of our service</li>
                    <li>To provide customer support</li>
                    <li>To gather analysis or valuable information so that we can improve our service</li>
                    <li>To monitor the usage of our service</li>
                    <li>To detect, prevent and address technical issues</li>
                </ul>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">Security of Data</h2>
                <p>
                    The security of your data is important to us but remember that no method of transmission over the Internet or method of electronic storage is 100% secure. While we strive to use commercially acceptable means to protect your Personal Data, we cannot guarantee its absolute security.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">Contact Us</h2>
                <p>
                    If you have any questions about this Privacy Policy, please contact us at:
                </p>
                <p class="mt-4">
                    <strong>Email:</strong> <a href="mailto:test@test.com" class="text-purple-600 hover:text-purple-700">test@test.com</a><br>
                    <strong>Address:</strong> Calgary, Alberta, Canada
                </p>
            </section>

            <p class="text-gray-600 text-sm mt-12">Last updated: January 2025</p>
        </div>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-8 mt-20">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <p class="text-gray-400">
                &copy; 2025 Test Calgary. All rights reserved.
            </p>
        </div>
    </footer>
</body>
</html>
```

**Step 3: Customize the Content**

Replace the placeholder text with your actual privacy policy. Key sections to update:

- Your company name (replace "Test Calgary" with your company)
- Your email address (replace "test@test.com")
- Your address
- The specific data you collect
- How you use that data

---

### Method 2: Creating a Simple Terms of Service Page

**Step 1: Create a New File**

1. Open your text editor
2. Click **File → New**
3. Save it as `terms.html` in the same folder as your `index.html`

**Step 2: Copy This Template**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - Test Calgary">
    <title>Terms of Service - Test Calgary</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white text-gray-900 font-sans">
    <!-- Header & Navigation -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16">
                <div class="flex items-center">
                    <div class="flex items-center space-x-2">
                        <div class="w-10 h-10 bg-purple-600 rounded-lg flex items-center justify-center">
                            <i class="fas fa-check text-white text-lg"></i>
                        </div>
                        <span class="text-2xl font-bold text-gray-900">Test Calgary</span>
                    </div>
                </div>
                <a href="index.html" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">Back to Home</a>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <main class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 py-20">
        <h1 class="text-4xl font-bold text-gray-900 mb-8">Terms of Service</h1>
        
        <div class="prose prose-lg max-w-none text-gray-700 space-y-6">
            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">1. Agreement to Terms</h2>
                <p>
                    By accessing and using the Test Calgary website and services, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">2. Use License</h2>
                <p>
                    Permission is granted to temporarily download one copy of the materials (information or software) on Test Calgary's website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:
                </p>
                <ul class="list-disc list-inside space-y-2 ml-4">
                    <li>Modifying or copying the materials</li>
                    <li>Using the materials for any commercial purpose or for any public display</li>
                    <li>Attempting to decompile or reverse engineer any software contained on the website</li>
                    <li>Removing any copyright or other proprietary notations from the materials</li>
                    <li>Transferring the materials to another person or "mirroring" the materials on any other server</li>
                </ul>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">3. Disclaimer</h2>
                <p>
                    The materials on Test Calgary's website are provided on an 'as is' basis. Test Calgary makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">4. Limitations</h2>
                <p>
                    In no event shall Test Calgary or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on the Test Calgary website.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">5. Accuracy of Materials</h2>
                <p>
                    The materials appearing on Test Calgary's website could include technical, typographical, or photographic errors. Test Calgary does not warrant that any of the materials on its website are accurate, complete, or current. Test Calgary may make changes to the materials contained on its website at any time without notice.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">6. Links</h2>
                <p>
                    Test Calgary has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by Test Calgary of the site. Use of any such linked website is at the user's own risk.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">7. Modifications</h2>
                <p>
                    Test Calgary may revise these terms of service for its website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">8. Governing Law</h2>
                <p>
                    These terms and conditions are governed by and construed in accordance with the laws of Alberta, Canada, and you irrevocably submit to the exclusive jurisdiction of the courts in that location.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">9. Contact Information</h2>
                <p>
                    If you have any questions about these Terms of Service, please contact us at:
                </p>
                <p class="mt-4">
                    <strong>Email:</strong> <a href="mailto:test@test.com" class="text-purple-600 hover:text-purple-700">test@test.com</a><br>
                    <strong>Address:</strong> Calgary, Alberta, Canada
                </p>
            </section>

            <p class="text-gray-600 text-sm mt-12">Last updated: January 2025</p>
        </div>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-8 mt-20">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <p class="text-gray-400">
                &copy; 2025 Test Calgary. All rights reserved.
            </p>
        </div>
    </footer>
</body>
</html>
```

**Step 3: Customize the Content**

Update:
- Your company name
- Your email address
- Your location
- Any specific terms relevant to your testing services

---

### Method 3: Creating a Blog Page (Optional)

If you want a blog page, create `blog.html`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Blog - Test Calgary">
    <title>Blog - Test Calgary</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white text-gray-900 font-sans">
    <!-- Header & Navigation -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16">
                <div class="flex items-center">
                    <div class="flex items-center space-x-2">
                        <div class="w-10 h-10 bg-purple-600 rounded-lg flex items-center justify-center">
                            <i class="fas fa-check text-white text-lg"></i>
                        </div>
                        <span class="text-2xl font-bold text-gray-900">Test Calgary</span>
                    </div>
                </div>
                <a href="index.html" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">Back to Home</a>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <main class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-20">
        <h1 class="text-4xl font-bold text-gray-900 mb-8">Our Blog</h1>
        
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
            <!-- Blog Post 1 -->
            <article class="bg-white border border-gray-200 rounded-xl overflow-hidden hover:shadow-lg transition-all duration-300">
                <div class="bg-gradient-to-r from-purple-500 to-purple-700 h-48 flex items-center justify-center">
                    <i class="fas fa-book text-white text-6xl"></i>
                </div>
                <div class="p-6">
                    <p class="text-sm text-purple-600 font-semibold mb-2">January 15, 2025</p>
                    <h2 class="text-xl font-bold text-gray-900 mb-3">Tips for Acing Your Next Test</h2>
                    <p class="text-gray-600 mb-4">Learn proven strategies to improve your test performance and boost your confidence on exam day.</p>
                    <a href="#" class="text-purple-600 hover:text-purple-700 font-semibold inline-flex items-center">
                        Read More <i class="fas fa-arrow-right ml-2"></i>
                    </a>
                </div>
            </article>

            <!-- Blog Post 2 -->
            <article class="bg-white border border-gray-200 rounded-xl overflow-hidden hover:shadow-lg transition-all duration-300">
                <div class="bg-gradient-to-r from-blue-500 to-blue-700 h-48 flex items-center justify-center">
                    <i class="fas fa-graduation-cap text-white text-6xl"></i>
                </div>
                <div class="p-6">
                    <p class="text-sm text-blue-600 font-semibold mb-2">January 10, 2025</p>
                    <h2 class="text-xl font-bold text-gray-900 mb-3">Understanding Professional Certifications</h2>
                    <p class="text-gray-600 mb-4">Explore different certification programs and how they can advance your career in today's competitive job market.</p>
                    <a href="#" class="text-blue-600 hover:text-blue-700 font-semibold inline-flex items-center">
                        Read More <i class="fas fa-arrow-right ml-2"></i>
                    </a>
                </div>
            </article>

            <!-- Blog Post 3 -->
            <article class="bg-white border border-gray-200 rounded-xl overflow-hidden hover:shadow-lg transition-all duration-300">
                <div class="bg-gradient-to-r from-green-500 to-green-700 h-48 flex items-center justify-center">
                    <i class="fas fa-brain text-white text-6xl"></i>
                </div>
                <div class="p-6">
                    <p class="text-sm text-green-600 font-semibold mb-2">January 5, 2025</p>
                    <h2 class="text-xl font-bold text-gray-900 mb-3">Managing Test Anxiety Effectively</h2>
                    <p class="text-gray-600 mb-4">Discover practical techniques to manage stress and anxiety before and during your testing experience.</p>
                    <a href="#" class="text-green-600 hover:text-green-700 font-semibold inline-flex items-center">
                        Read More <i class="fas fa-arrow-right ml-2"></i>
                    </a>
                </div>
            </article>
        </div>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-8 mt-20">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <p class="text-gray-400">
                &copy; 2025 Test Calgary. All rights reserved.
            </p>
        </div>
    </footer>
</body>
</html>
```

---

### Verifying Your Links Work

**After creating your policy and terms pages:**

1. Open your `index.html` file in a web browser
2. Scroll to the footer
3. Click on "Privacy Policy" - it should open `privacy.html`
4. Click on "Terms of Service" - it should open `terms.html`
5. Click on "Back to Home" on those pages - it should return to `index.html`

**If links don't work:**
- Make sure all three files (`index.html`, `privacy.html`, `terms.html`) are in the same folder
- Check that the filenames are spelled exactly right (lowercase, with `.html` extension)
- Clear your browser cache (Ctrl+Shift+Delete) and refresh the page

---

## Troubleshooting Common Issues

### Problem 1: Links Don't Work

**Symptoms:**
- Clicking a link does nothing
- You get a 404 error
- The page doesn't navigate anywhere

**Solutions:**

1. **Check the file names match exactly**
   ```html
   <!-- ❌ WRONG - case sensitive -->
   <a href="Privacy.html">Privacy</a>
   
   <!-- ✅ CORRECT -->
   <a href="privacy.html">Privacy</a>
   ```

2. **Verify files are in the same folder**
   - All your HTML files should be in the same directory
   - Example: `C:\Users\YourName\Documents\website\`

3. **Use correct URL format**
   ```html
   <!-- For files in same folder -->
   <a href="privacy.html">Privacy</a>
   
   <!-- For external websites -->
   <a href="https://example.com">Example</a>
   
   <!-- For sections on same page -->
   <a href="#features">Features</a>
   ```

---

### Problem 2: Text Not Appearing

**Symptoms:**
- You added text but it doesn't show on the page
- Text appears in wrong location

**Solutions:**

1. **Make sure you're editing the right HTML tags**
   ```html
   <!-- ❌ WRONG - inside wrong tags -->
   <h1>My Title</h1>
   <p>This text won't show</p>  <!-- Not properly closed -->
   
   <!-- ✅ CORRECT -->
   <h1>My Title</h1>
   <p>This text will show</p>
   ```

2. **Check for unclosed tags**
   ```html
   <!-- ❌ WRONG - missing closing tag -->
   <p>This text has no closing tag
   
   <!-- ✅ CORRECT -->
   <p>This text has a closing tag</p>
   ```

3. **Refresh your browser**
   - Press Ctrl+F5 (or Cmd+Shift+R on Mac)
   - This clears the cache and loads the latest version

---

### Problem 3: Colors Look Wrong

**Symptoms:**
- Colors don't match what you expected
- Background is wrong color
- Text is hard to read

**Solutions:**

1. **Check Tailwind class names**
   ```html
   <!-- ❌ WRONG - typo in class name -->
   <div class="bg-purpl-600">Wrong</div>
   
   <!-- ✅ CORRECT -->
   <div class="bg-purple-600">Correct</div>
   ```

2. **Remember responsive classes**
   ```html
   <!-- Different colors on different screens -->
   <div class="text-gray-900 md:text-purple-600">
       Text is gray on mobile, purple on tablets and up
   </div>
   ```

3. **Check for conflicting classes**
   ```html
   <!-- ❌ WRONG - conflicting classes -->
   <div class="bg-purple-600 bg-blue-600">
       Only the last class will apply
   </div>
   
   <!-- ✅ CORRECT -->
   <div class="bg-purple-600">
       Only one background color
   </div>
   ```

---

### Problem 4: Page Layout Broken

**Symptoms:**
- Elements overlapping
- Text too large or too small
- Mobile version doesn't look right

**Solutions:**

1. **Don't remove responsive classes**
   ```html
   <!-- ❌ WRONG - breaks responsive design -->
   <div class="hidden lg:flex">
       <!-- Removed hidden class -->
   </div>
   
   <!-- ✅ CORRECT -->
   <div class="hidden lg:flex">
       Hidden on small screens, visible on large screens
   </div>
   ```

2. **Check for missing closing divs**
   ```html
   <!-- ❌ WRONG - missing closing tag -->
   <div class="grid grid-cols-3">
       <div>Item 1</div>
       <div>Item 2</div>
       <div>Item 3</div>
   <!-- Missing </div> -->
   
   <!-- ✅ CORRECT -->
   <div class="grid grid-cols-3">
       <div>Item 1</div>
       <div>Item 2</div>
       <div>Item 3</div>
   </div>
   ```

3. **Test on mobile**
   - Open your page in a mobile browser
   - Or use browser dev tools (F12) and select mobile view
   - Make sure everything is readable and properly spaced

---

### Problem 5: Icons Not Showing

**Symptoms:**
- You see empty squares instead of icons
- Icons appear as broken images

**Solutions:**

1. **Make sure Font Awesome is loaded**
   - Check that this line is in your `<head>`:
   ```html
   <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
   ```

2. **Use correct icon class names**
   ```html
   <!-- ❌ WRONG - icon doesn't exist -->
   <i class="fas fa-wrong-icon"></i>
   
   <!-- ✅ CORRECT -->
   <i class="fas fa-check"></i>
   ```

3. **Check Font Awesome documentation**
   - Visit https://fontawesome.com/icons
   - Search for the icon you want
   - Copy the exact class name

---

### Problem 6: Mobile Menu Not Working

**Symptoms:**
- Menu button doesn't open/close
- Mobile menu always hidden
- Menu doesn't close when you click a link

**Solutions:**

1. **Check JavaScript is not broken**
   - Look for JavaScript errors in browser console (F12)
   - Make sure you didn't accidentally delete JavaScript code

2. **Verify HTML structure**
   ```html
   <!-- ❌ WRONG - missing mobile-menu class -->
   <div class="hidden md:hidden pb-4">
       <!-- This won't toggle properly -->
   </div>
   
   <!-- ✅ CORRECT -->
   <div class="mobile-menu hidden md:hidden pb-4">
       <!-- JavaScript targets this class -->
   </div>
   ```

3. **Test in different browsers**
   - Try Chrome, Firefox, Safari
   - Clear browser cache

---

## Best Practices

### 1. Always Backup Your Files

Before making changes, create a copy of your files:

```
Original files:
- index.html
- privacy.html
- terms.html

Backup files:
- index-backup.html
- privacy-backup.html
- terms-backup.html
```

If something goes wrong, you can always restore the backup.

---

### 2. Make One Change at a Time

Don't change multiple things at once:

```
❌ WRONG:
- Change text
- Change colors
- Change links
- Change layout
(If something breaks, you won't know which change caused it)

✅ CORRECT:
- Change one thing
- Test it
- Save it
- Move to next change
```

---

### 3. Use Version Control (Optional but Recommended)

If you're comfortable with it, use Git to track changes:

```bash
git add index.html
git commit -m "Updated hero section text"
git push
```

This creates a history you can revert to if needed.

---

### 4. Test on Multiple Devices

Always check your page on:
- Desktop (1920x1080)
- Tablet (768x1024)
- Mobile (375x667)

Use browser dev tools (F12) to simulate different screen sizes.

---

### 5. Validate Your HTML

Use the W3C HTML Validator:
1. Go to https://validator.w3.org/
2. Upload your HTML file
3. Fix any errors it finds

---

### 6. Keep Your Text Updated

Regularly update:
- Testimonials (add new ones)
- Contact information
- Hours of operation
- Service offerings

Outdated information hurts credibility.

---

### 7. Use Descriptive Link Text

```html
<!-- ❌ WRONG - vague -->
<a href="privacy.html">Click here</a>

<!-- ✅ CORRECT - descriptive -->
<a href="privacy.html">Privacy Policy</a>
```

This helps users and search engines understand where links go.

---

### 8. Maintain Consistent Branding

Keep the same:
- Color scheme (purple, blue, green, etc.)
- Font sizes
- Spacing
- Button styles

Consistency builds trust and professionalism.

---

### 9. Regular Maintenance Checklist

Check these items regularly:

- [ ] All links work correctly
- [ ] Contact information is current
- [ ] Phone numbers are clickable (use `tel:`)
- [ ] Email addresses are clickable (use `mailto:`)
- [ ] Page loads quickly
- [ ] No broken images
- [ ] Mobile version works properly
- [ ] Forms submit correctly
- [ ] Social media links are active
- [ ] Page title matches content

---

### 10. Performance Tips

To keep your page fast:

1. **Minimize images**
   - Use compressed images
   - Use appropriate image sizes

2. **Avoid too many fonts**
   - Stick with 1-2 font families

3. **Don't overuse animations**
   - Animations can slow down pages
   - Use sparingly

4. **Remove unused CSS**
   - Delete Tailwind classes you're not using

---

## Quick Reference Guide

### Common Tailwind Classes

| Class | What It Does |
|-------|-------------|
| `bg-purple-600` | Purple background |
| `text-white` | White text |
| `px-8` | Padding left and right |
| `py-4` | Padding top and bottom |
| `mb-6` | Margin bottom |
| `rounded-lg` | Rounded corners |
| `shadow-md` | Medium shadow |
| `hover:bg-purple-700` | Purple on hover |
| `hidden` | Hide element |
| `md:flex` | Show on medium screens and up |
| `grid grid-cols-3` | 3-column grid |
| `transition-all` | Smooth animation |

### Common HTML Tags

| Tag | Purpose |
|-----|---------|
| `<h1>` - `<h6>` | Headings (h1 largest, h6 smallest) |
| `<p>` | Paragraph text |
| `<a>` | Link |
| `<button>` | Clickable button |
| `<div>` | Container/section |
| `<span>` | Inline text container |
| `<ul>` | Unordered list |
| `<li>` | List item |
| `<img>` | Image |
| `<i>` | Icon (Font Awesome) |

### File Structure

```
your-website/
├── index.html          (Main landing page)
├── privacy.html        (Privacy policy)
├── terms.html          (Terms of service)
├── blog.html           (Optional blog)
└── assets/             (Optional folder for images)
    └── logo.png
```

---

## Getting Help

### Useful Resources

1. **Tailwind CSS Documentation**
   - https://tailwindcss.com/docs
   - Complete guide to all Tailwind classes

2. **Font Awesome Icons**
   - https://fontawesome.com/icons
   - Search for and copy icon names

3. **HTML Reference**
   - https://developer.mozilla.org/en-US/docs/Web/HTML
   - Official HTML documentation

4. **W3C Validator**
   - https://validator.w3.org/
   - Check your HTML for errors

5. **Browser DevTools**
   - Press F12 in any browser
   - Inspect elements and debug issues

### When You're Stuck

1. **Read error messages carefully** - They usually tell you exactly what's wrong
2. **Check browser console** - F12 → Console tab shows JavaScript errors
3. **Validate your HTML** - Use W3C Validator
4. **Compare with working code** - Look at similar sections that work
5. **Search online** - Most problems have been solved before
6. **Ask for help** - Post on Stack Overflow or hire a developer

---

## Conclusion

Your Test Calgary landing page is a professional, modern website built with:
- **HTML** - Structure and content
- **Tailwind CSS** - Styling and layout
- **Font Awesome** - Icons
- **JavaScript** - Interactive features

By following this guide, you can:
✅ Update text and content easily
✅ Fix and manage links properly
✅ Add new pages like privacy and terms
✅ Customize colors and styling
✅ Troubleshoot common issues
✅ Maintain your site professionally

Remember: **Always backup before making major changes**, and **test on multiple devices** before going live.

Good luck with your testing center website! 🎓
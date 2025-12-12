# 🧩 Reusable Components Library

This document contains all reusable component patterns used in the StartupFlow landing page. Copy and paste these components to quickly build your own landing pages.

## 📋 Table of Contents

1. [Buttons](#buttons)
2. [Cards](#cards)
3. [Navigation](#navigation)
4. [Hero Sections](#hero-sections)
5. [Feature Grids](#feature-grids)
6. [Testimonials](#testimonials)
7. [Pricing Cards](#pricing-cards)
8. [Forms](#forms)
9. [Footers](#footers)

---

## Buttons

### Primary Button
```html
<a href="#" class="px-8 py-4 bg-blue-500 text-white rounded-lg font-semibold hover:bg-blue-600 transition-all shadow-lg hover:shadow-xl">
    Button Text
</a>
```

### Secondary Button
```html
<a href="#" class="px-8 py-4 border-2 border-gray-300 text-gray-700 rounded-lg font-semibold hover:border-blue-500 hover:text-blue-500 transition-all">
    Button Text
</a>
```

### Gradient Button
```html
<a href="#" class="px-8 py-4 bg-gradient-to-r from-blue-500 to-purple-600 text-white rounded-lg font-semibold hover:scale-105 transition-all shadow-lg">
    Button Text
</a>
```

### Outline Button
```html
<a href="#" class="px-6 py-2 border-2 border-blue-500 text-blue-500 rounded-lg font-semibold hover:bg-blue-500 hover:text-white transition-all">
    Button Text
</a>
```

### Small Button
```html
<a href="#" class="px-6 py-2 bg-blue-500 text-white rounded-lg font-semibold hover:bg-blue-600 transition-colors shadow-md">
    Button Text
</a>
```

---

## Cards

### Feature Card
```html
<div class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl transition-shadow border border-gray-100">
    <div class="w-14 h-14 bg-blue-100 rounded-lg flex items-center justify-center mb-6">
        <svg class="w-7 h-7 text-blue-500" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <!-- Icon SVG path -->
        </svg>
    </div>
    <h3 class="text-xl font-bold text-gray-900 mb-3">Feature Title</h3>
    <p class="text-gray-600">
        Feature description goes here. Explain the benefit clearly and concisely.
    </p>
</div>
```

### Testimonial Card
```html
<div class="bg-white rounded-xl p-8 shadow-lg">
    <!-- Star Rating -->
    <div class="flex items-center mb-4">
        <div class="flex text-yellow-400">
            <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20">
                <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"></path>
            </svg>
            <!-- Repeat for 5 stars -->
        </div>
    </div>
    
    <!-- Testimonial Text -->
    <p class="text-gray-600 mb-6">
        "This is an amazing product! It has completely transformed how we work."
    </p>
    
    <!-- Author Info -->
    <div class="flex items-center">
        <div class="w-12 h-12 bg-gradient-to-br from-blue-400 to-blue-600 rounded-full flex items-center justify-center text-white font-bold">
            JD
        </div>
        <div class="ml-4">
            <div class="font-semibold text-gray-900">John Doe</div>
            <div class="text-sm text-gray-600">CEO, Company</div>
        </div>
    </div>
</div>
```

### Pricing Card (Basic)
```html
<div class="bg-white rounded-2xl p-8 shadow-lg border-2 border-gray-200 hover:border-blue-500 transition-all">
    <div class="text-center mb-8">
        <h3 class="text-2xl font-bold text-gray-900 mb-2">Plan Name</h3>
        <p class="text-gray-600 mb-6">Plan description</p>
        <div class="mb-6">
            <span class="text-5xl font-bold text-gray-900">$29</span>
            <span class="text-gray-600">/month</span>
        </div>
        <a href="#" class="block w-full py-3 px-6 border-2 border-blue-500 text-blue-500 rounded-lg font-semibold hover:bg-blue-500 hover:text-white transition-all">
            Get Started
        </a>
    </div>
    <ul class="space-y-4">
        <li class="flex items-start">
            <svg class="w-6 h-6 text-green-500 mr-3 flex-shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
            </svg>
            <span class="text-gray-600">Feature 1</span>
        </li>
        <!-- Repeat for more features -->
    </ul>
</div>
```

### Pricing Card (Featured)
```html
<div class="bg-gradient-to-br from-blue-500 to-purple-600 rounded-2xl p-8 shadow-2xl transform scale-105 relative">
    <div class="absolute -top-4 left-1/2 transform -translate-x-1/2">
        <span class="bg-yellow-400 text-gray-900 px-4 py-1 rounded-full text-sm font-bold">MOST POPULAR</span>
    </div>
    <div class="text-center mb-8">
        <h3 class="text-2xl font-bold text-white mb-2">Pro</h3>
        <p class="text-white/90 mb-6">For growing startups</p>
        <div class="mb-6">
            <span class="text-5xl font-bold text-white">$79</span>
            <span class="text-white/90">/month</span>
        </div>
        <a href="#" class="block w-full py-3 px-6 bg-white text-blue-500 rounded-lg font-semibold hover:bg-gray-100 transition-all shadow-lg">
            Start Free Trial
        </a>
    </div>
    <ul class="space-y-4">
        <li class="flex items-start">
            <svg class="w-6 h-6 text-white mr-3 flex-shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
            </svg>
            <span class="text-white">Feature 1</span>
        </li>
        <!-- Repeat for more features -->
    </ul>
</div>
```

---

## Navigation

### Fixed Navbar
```html
<nav class="fixed top-0 w-full z-50 bg-white/90 backdrop-blur-md shadow-sm">
    <div class="container mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex items-center justify-between h-16">
            <!-- Logo -->
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 bg-gradient-to-br from-blue-500 to-purple-600 rounded-lg flex items-center justify-center">
                    <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <!-- Icon -->
                    </svg>
                </div>
                <span class="text-xl font-bold text-gray-900">Brand</span>
            </div>

            <!-- Desktop Navigation -->
            <div class="hidden md:flex items-center space-x-8">
                <a href="#features" class="text-gray-600 hover:text-blue-500 transition-colors">Features</a>
                <a href="#pricing" class="text-gray-600 hover:text-blue-500 transition-colors">Pricing</a>
                <a href="#contact" class="text-gray-600 hover:text-blue-500 transition-colors">Contact</a>
            </div>

            <!-- CTA Buttons -->
            <div class="flex items-center space-x-4">
                <a href="#" class="hidden sm:inline-block text-gray-600 hover:text-blue-500 transition-colors">Sign In</a>
                <a href="#" class="px-6 py-2 bg-blue-500 text-white rounded-lg font-semibold hover:bg-blue-600 transition-colors shadow-md">
                    Get Started
                </a>
            </div>
        </div>
    </div>
</nav>
```

---

## Hero Sections

### Hero with CTA
```html
<section class="pt-32 pb-20 px-4 sm:px-6 lg:px-8 bg-gradient-to-b from-blue-50 to-white">
    <div class="container mx-auto">
        <div class="flex flex-col lg:flex-row items-center gap-12">
            <!-- Hero Content -->
            <div class="flex-1 text-center lg:text-left">
                <h1 class="text-4xl sm:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
                    Your Compelling <span class="text-blue-500">Headline</span>
                </h1>
                <p class="text-xl text-gray-600 mb-8 max-w-2xl mx-auto lg:mx-0">
                    A clear, benefit-focused subheadline that explains what you do and why it matters.
                </p>
                
                <!-- CTA Buttons -->
                <div class="flex flex-col sm:flex-row gap-4 justify-center lg:justify-start">
                    <a href="#" class="px-8 py-4 bg-blue-500 text-white rounded-lg font-semibold hover:bg-blue-600 transition-all shadow-lg hover:shadow-xl">
                        Primary CTA
                    </a>
                    <a href="#" class="px-8 py-4 border-2 border-gray-300 text-gray-700 rounded-lg font-semibold hover:border-blue-500 hover:text-blue-500 transition-all">
                        Secondary CTA
                    </a>
                </div>
            </div>

            <!-- Hero Image/Mockup -->
            <div class="flex-1 w-full max-w-lg">
                <!-- Add your hero image or mockup here -->
            </div>
        </div>
    </div>
</section>
```

---

## Feature Grids

### 3-Column Feature Grid
```html
<section class="py-20 px-4 sm:px-6 lg:px-8">
    <div class="container mx-auto">
        <div class="text-center mb-16">
            <h2 class="text-3xl sm:text-4xl font-bold text-gray-900 mb-4">
                Section Title
            </h2>
            <p class="text-xl text-gray-600 max-w-2xl mx-auto">
                Section description
            </p>
        </div>

        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
            <!-- Feature Card 1 -->
            <div class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl transition-shadow border border-gray-100">
                <div class="w-14 h-14 bg-blue-100 rounded-lg flex items-center justify-center mb-6">
                    <!-- Icon -->
                </div>
                <h3 class="text-xl font-bold text-gray-900 mb-3">Feature Title</h3>
                <p class="text-gray-600">Feature description</p>
            </div>
            <!-- Repeat for more features -->
        </div>
    </div>
</section>
```

---

## Forms

### Contact Form
```html
<form class="bg-white rounded-2xl shadow-xl p-8 border border-gray-200">
    <div class="mb-6">
        <label class="block text-gray-700 font-semibold mb-2">Name</label>
        <input type="text" class="w-full px-4 py-3 rounded-lg border border-gray-300 bg-white text-gray-800 focus:outline-none focus:ring-2 focus:ring-blue-500" placeholder="Your Name">
    </div>

    <div class="mb-6">
        <label class="block text-gray-700 font-semibold mb-2">Email</label>
        <input type="email" class="w-full px-4 py-3 rounded-lg border border-gray-300 bg-white text-gray-800 focus:outline-none focus:ring-2 focus:ring-blue-500" placeholder="your@email.com">
    </div>

    <div class="mb-6">
        <label class="block text-gray-700 font-semibold mb-2">Message</label>
        <textarea rows="5" class="w-full px-4 py-3 rounded-lg border border-gray-300 bg-white text-gray-800 focus:outline-none focus:ring-2 focus:ring-blue-500" placeholder="Your message..."></textarea>
    </div>

    <button type="submit" class="w-full py-3 bg-blue-500 text-white rounded-lg font-semibold hover:bg-blue-600 transition-all shadow-lg">
        Send Message
    </button>
</form>
```

---

## Footers

### Multi-Column Footer
```html
<footer class="bg-gray-900 text-white py-12 px-4 sm:px-6 lg:px-8">
    <div class="container mx-auto">
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8 mb-8">
            <!-- Company Info -->
            <div>
                <div class="flex items-center space-x-2 mb-4">
                    <div class="w-10 h-10 bg-gradient-to-br from-blue-500 to-purple-600 rounded-lg"></div>
                    <span class="text-xl font-bold">Brand</span>
                </div>
                <p class="text-gray-400">Company tagline or description</p>
            </div>

            <!-- Links Column 1 -->
            <div>
                <h4 class="font-bold mb-4">Product</h4>
                <ul class="space-y-2">
                    <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Features</a></li>
                    <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Pricing</a></li>
                </ul>
            </div>

            <!-- Links Column 2 -->
            <div>
                <h4 class="font-bold mb-4">Company</h4>
                <ul class="space-y-2">
                    <li><a href="#" class="text-gray-400 hover:text-white transition-colors">About</a></li>
                    <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Contact</a></li>
                </ul>
            </div>

            <!-- Links Column 3 -->
            <div>
                <h4 class="font-bold mb-4">Resources</h4>
                <ul class="space-y-2">
                    <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Documentation</a></li>
                    <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Support</a></li>
                </ul>
            </div>
        </div>

        <!-- Footer Bottom -->
        <div class="border-t border-gray-800 pt-8 flex flex-col sm:flex-row justify-between items-center">
            <p class="text-gray-400 text-sm mb-4 sm:mb-0">
                © 2025 Brand. All rights reserved.
            </p>
            <div class="flex space-x-6">
                <!-- Social Icons -->
            </div>
        </div>
    </div>
</footer>
```

---

## 🎨 Color Variations

Replace color classes to match your brand:

- `blue-500` → `purple-500`, `green-500`, `red-500`, etc.
- `gray-900` → `slate-900`, `zinc-900`, etc.

## 📱 Responsive Patterns

All components use these breakpoints:
- `sm:` - 640px and up
- `md:` - 768px and up
- `lg:` - 1024px and up
- `xl:` - 1280px and up

## 💡 Usage Tips

1. **Consistency**: Use the same button style throughout
2. **Spacing**: Maintain consistent padding and margins
3. **Colors**: Stick to your brand color palette
4. **Typography**: Use consistent font sizes and weights
5. **Hover States**: Add transitions for smooth interactions

---

**Copy, paste, and customize these components for your projects!**
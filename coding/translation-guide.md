# CSS to Tailwind CSS v4 Translation Guide

## Overview
This guide shows students how to convert traditional CSS styles to Tailwind CSS v4 utility classes through practical examples.

## Key Translation Patterns

### 1. Layout & Spacing

| CSS | Tailwind v4 |
|-----|-------------|
| `margin: 0;` | `m-0` |
| `padding: 0;` | `p-0` |
| `padding: 1rem 2rem;` | `px-8 py-4` |
| `max-width: 1200px; margin: 0 auto;` | `max-w-6xl mx-auto` |
| `display: flex;` | `flex` |
| `justify-content: space-between;` | `justify-between` |
| `align-items: center;` | `items-center` |
| `display: grid;` | `grid` |
| `grid-template-columns: repeat(3, 1fr);` | `grid-cols-3` |

### 2. Typography

| CSS | Tailwind v4 |
|-----|-------------|
| `font-family: 'Arial', sans-serif;` | `font-sans` |
| `font-size: 1.5rem;` | `text-2xl` |
| `font-weight: bold;` | `font-bold` |
| `font-weight: 600;` | `font-semibold` |
| `text-align: center;` | `text-center` |
| `line-height: 1.6;` | `leading-relaxed` |
| `color: #3b82f6;` | `text-blue-500` |

### 3. Colors & Backgrounds

| CSS | Tailwind v4 |
|-----|-------------|
| `background-color: #ffffff;` | `bg-white` |
| `background-color: #f8f9fa;` | `bg-gray-50` |
| `color: #333;` | `text-gray-800` |
| `background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);` | `bg-gradient-to-br from-indigo-500 to-purple-600` |

### 4. Borders & Shadows

| CSS | Tailwind v4 |
|-----|-------------|
| `border-radius: 0.5rem;` | `rounded-lg` |
| `border-radius: 1rem;` | `rounded-2xl` |
| `box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);` | `shadow-lg` |
| `border: 1px solid #e5e7eb;` | `border border-gray-200` |

### 5. Positioning & Z-index

| CSS | Tailwind v4 |
|-----|-------------|
| `position: sticky;` | `sticky` |
| `top: 0;` | `top-0` |
| `z-index: 100;` | `z-50` |

### 6. Transitions & Transforms

| CSS | Tailwind v4 |
|-----|-------------|
| `transition: color 0.3s ease;` | `transition-colors duration-300` |
| `transition: all 0.3s ease;` | `transition-all duration-300` |
| `transform: translateY(-2px);` | `hover:-translate-y-1` |
| `transform: translateY(-5px);` | `hover:-translate-y-2` |

### 7. Responsive Design

| CSS | Tailwind v4 |
|-----|-------------|
| `@media (max-width: 768px) { flex-direction: column; }` | `flex-col md:flex-row` |
| `@media (max-width: 768px) { font-size: 2rem; }` | `text-3xl md:text-5xl` |
| `@media (max-width: 768px) { grid-template-columns: 1fr; }` | `grid-cols-1 md:grid-cols-3` |

## Complete Translation Examples

### Example 1: Header Navigation
```css
/* Traditional CSS */
.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem 2rem;
    background-color: #ffffff;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}
```

```html
<!-- Tailwind v4 -->
<nav class="flex justify-between items-center px-8 py-4 bg-white shadow-lg">
```

### Example 2: Feature Card with Hover Effects
```css
/* Traditional CSS */
.feature-card {
    background-color: #f8f9fa;
    padding: 2rem;
    border-radius: 1rem;
    text-align: center;
    transition: transform 0.3s ease;
    border: 1px solid #e5e7eb;
}

.feature-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
}
```

```html
<!-- Tailwind v4 -->
<div class="bg-gray-50 p-8 rounded-2xl text-center transition-all duration-300 border border-gray-200 hover:-translate-y-2 hover:shadow-xl">
```

### Example 3: Responsive Grid Layout
```css
/* Traditional CSS */
.features-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2rem;
}

@media (max-width: 768px) {
    .features-grid {
        grid-template-columns: 1fr;
    }
}
```

```html
<!-- Tailwind v4 -->
<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
```

## Benefits of Tailwind v4

1. **No CSS File Needed**: All styling is done in HTML classes
2. **Responsive by Default**: Mobile-first approach with breakpoint prefixes
3. **Consistent Spacing**: Predefined spacing scale prevents inconsistencies
4. **Smaller Bundle Size**: Only includes classes you actually use
5. **Faster Development**: No context switching between HTML and CSS files
6. **Better Maintenance**: Styles are co-located with markup
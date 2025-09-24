# Astra Child Theme - Dynamic WooCommerce Shop

## Description
A custom Astra child theme with dynamic WooCommerce functionality. Features include:
- Dynamic tabbed interface for categories with subcategories
- AJAX-powered product loading
- Real-time search and filtering
- URL history management
- Optimized performance with caching

## Installation

1. **Upload the Theme**:
   - Go to WordPress Admin > Appearance > Themes
   - Click "Add New" > "Upload Theme"
   - Choose the `astra-child.zip` file
   - Click "Install Now"

2. **Activate the Theme**:
   - After installation, click "Activate"
   - Or go to Appearance > Themes and activate "Astra Child"

## Requirements

- WordPress 5.0 or higher
- WooCommerce 3.0 or higher
- Astra Theme (parent theme) installed and activated
- PHP 7.2 or higher

## Features

### Dynamic Category Tabs
- Automatically creates tabs for subcategories
- Maintains real URLs for SEO
- Fast switching between categories without page reload

### Advanced Filtering
- Price range filters
- Attribute filters (size, color, etc.)
- Brand filters (if configured)
- Real-time search within categories

### Performance Optimizations
- Product caching to reduce API calls
- Lazy loading for images
- Conditional script loading (only loads on pages that need it)
- Optimized REST API endpoints

## Configuration

### Customizing the Number of Products
Edit line 12 in `/assets/js/dynamic-shop.js`:
```javascript
per_page: 12, // Change this number
```

### Customizing Tab Behavior
The dynamic interface only activates for categories that have subcategories. 
Main shop page shows normal WooCommerce layout.

### Styling
- Main styles: `/style.css`
- Dynamic shop styles: `/assets/css/dynamic-shop.css`

## File Structure

```
astra-child/
├── style.css                    # Main theme stylesheet
├── functions.php                 # Theme functions
├── README.md                     # This file
├── woocommerce/
│   └── archive-product.php      # Product archive template
└── assets/
    ├── css/
    │   └── dynamic-shop.css     # Dynamic shop styles
    └── js/
        └── dynamic-shop.js      # Dynamic shop JavaScript
```

## Troubleshooting

### Products Not Loading
1. Check if WooCommerce REST API is enabled
2. Verify permalinks are set to "Post name" or custom structure
3. Check browser console for JavaScript errors

### Tabs Not Showing
- Tabs only appear for categories that have subcategories
- Check if subcategories exist and are not empty

### Styles Not Loading
- Clear browser cache
- Check if child theme is activated
- Verify file paths in functions.php

## Support

For issues or questions, please check:
1. WooCommerce documentation
2. Astra theme documentation
3. WordPress Codex

## Changelog

### Version 1.0.0
- Initial release
- Dynamic tabbed interface for subcategories
- AJAX product loading
- Search and filter functionality
- Cart integration

## License

GPL v2 or later

## Credits

Built on top of:
- Astra Theme by Brainstorm Force
- WooCommerce by Automattic

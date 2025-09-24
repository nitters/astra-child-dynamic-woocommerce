# Installation Guide

## Quick Start

### Option 1: Direct Download (Recommended)
1. Download the complete theme package: [astra-child-theme.zip](../../releases/latest)
2. Go to WordPress Admin → Appearance → Themes
3. Click "Add New" → "Upload Theme"
4. Choose the downloaded zip file
5. Click "Install Now" and then "Activate"

### Option 2: Manual Installation
1. Clone or download this repository
2. Create a folder called `astra-child` in your WordPress `wp-content/themes/` directory
3. Copy all files from this repository into the `astra-child` folder
4. Go to WordPress Admin → Appearance → Themes
5. Find "Astra Child" and click "Activate"

### Option 3: Using Git
```bash
cd wp-content/themes/
git clone https://github.com/nitters/astra-child-dynamic-woocommerce.git astra-child
```

## Pre-requisites

Before installing this theme, ensure you have:

1. **WordPress 5.0+** installed and running
2. **Astra Theme** (parent theme) installed - [Download Astra](https://wordpress.org/themes/astra/)
3. **WooCommerce 3.0+** plugin installed and activated
4. **PHP 7.2+** on your server

## Post-Installation Setup

### 1. Configure Permalinks
- Go to Settings → Permalinks
- Select "Post name" or any custom structure
- Click "Save Changes"

### 2. Create Product Categories
- Go to Products → Categories
- Create main categories with subcategories
- The dynamic interface only appears for categories that have subcategories

### 3. Add Products
- Add products to your categories
- Ensure products have prices and images for best display

### 4. Configure WooCommerce Settings
- Go to WooCommerce → Settings
- Configure your shop page
- Set up payment methods if needed

## Theme Features

### Dynamic Shop Interface
- Automatically activated for categories with subcategories
- Tabbed navigation for easy browsing
- AJAX-powered loading (no page refreshes)

### Filtering Options
- Price range filters
- Product attributes (size, color, etc.)
- Brand filters (if configured)
- Real-time search

### Performance Optimizations
- Product caching
- Lazy loading for images
- Conditional script loading
- Optimized REST API endpoints

## Customization

### Modify Products Per Page
Edit `/assets/js/dynamic-shop.js` line 100:
```javascript
per_page: 12, // Change this number
```

### Custom Styling
- Main styles: `/style.css`
- Dynamic shop styles: `/assets/css/dynamic-shop.css`

### Custom Functions
Edit `/functions.php` to add your own functionality

## Troubleshooting

### Products Not Loading
1. Check if WooCommerce REST API is enabled
2. Verify permalinks are not set to "Plain"
3. Check browser console for errors (F12)
4. Ensure categories have products

### Tabs Not Showing
- Tabs only appear for categories with subcategories
- Check if subcategories exist and have products

### Styles Not Loading
1. Clear browser cache (Ctrl+F5)
2. Check if child theme is activated
3. Verify file permissions (644 for files, 755 for folders)

### Cart Not Working
1. Ensure WooCommerce is properly configured
2. Check if sessions are enabled
3. Verify AJAX URL is correct

## Support

For issues or questions:
1. Check the [README](README.md) file
2. Review [WooCommerce documentation](https://docs.woocommerce.com/)
3. Check [Astra theme documentation](https://wpastra.com/docs/)
4. Open an issue on [GitHub](https://github.com/nitters/astra-child-dynamic-woocommerce/issues)

## License

GPL v2 or later - see LICENSE file for details

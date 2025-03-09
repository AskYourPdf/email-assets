# Email Assets Repository

This GitHub repository serves as a centralised location for storing and managing all assets used in our email templates, including images and fonts for AskYourPdf products.

[![Last Commit](https://img.shields.io/github/last-commit/AskYourPdf/email-assets)](https://github.com/AskYourPdf/email-assets/commits/main)
[![Issues](https://img.shields.io/github/issues/AskYourPdf/email-assets)](https://github.com/AskYourPdf/email-assets/issues)
[![Pull Requests](https://img.shields.io/github/issues-pr/AskYourPdf/email-assets)](https://github.com/AskYourPdf/email-assets/pulls)

## Repository Structure

```
email-assets/
├── cowriter/
│   ├── images/
│   │   ├── logos/
│   │   │   ├── cowriter-logo.png
│   │   │   ├── cowriter-logo-dark.png
│   │   │   └── ...
│   │   ├── icons/
│   │   │   ├── social-twitter.png
│   │   │   ├── social-facebook.png
│   │   │   └── ...
│   │   ├── headers/
│   │   │   ├── welcome-header.jpg
│   │   │   ├── newsletter-header.jpg
│   │   │   └── ...
│   │   └── backgrounds/
│   │       ├── primary-bg.jpg
│   │       ├── secondary-bg.jpg
│   │       └── ...
│   └── fonts/
│       ├── primary-font.woff
│       ├── primary-font.woff2
│       ├── secondary-font.woff
│       └── ...
├── askyourpdf/
│   ├── images/
│   │   └── ...
│   └── fonts/
│       └── ...
└── [other-products]/
    ├── images/
    │   └── ...
    └── fonts/
        └── ...
```

## Usage Guidelines

## Best Practices for Email Assets

1. **Image Assets**:
   - Use PNG for logos and icons (with transparency)
   - Use JPG for photos and complex graphics
   - Use GIF for simple animations
   - SVG is not recommended for email templates due to inconsistent support

2. **Image Optimization**:
   - Keep file sizes under 100KB when possible
   - Optimize all images before adding to the repository
   - Use descriptive filenames (e.g., `welcome-header.jpg` instead of `img001.jpg`)

3. **Dimensions**:
   - Maximum width: 600px (standard email width)

4. **Version Control**:
   - When updating existing assets, consider creating a new file instead of replacing, to prevent caching issues
   - Use date or version suffixes when necessary (e.g., `logo-v2.png`)

## Font Assets

1. **Before Adding Fonts**:
   - Check if the font is already reliably hosted online (Google Fonts, Adobe Fonts, etc.)
   - Only add fonts to this repository if they are not available from established font CDNs

2. **Web Fonts**:
   - Include both WOFF and WOFF2 formats for maximum compatibility

3. **Usage in Templates**:
   - Always specify web-safe fallback fonts
   - Use absolute URLs to the hosted font files
   - Example for fonts hosted in this repository:
     ```css
     @font-face {
       font-family: 'PrimaryFont';
       src: url('https://raw.githubusercontent.com/AskYourPdf/email-assets/main/cowriter/fonts/primary-font.woff2') format('woff2'),
            url('https://raw.githubusercontent.com/AskYourPdf/email-assets/main/cowriter/fonts/primary-font.woff') format('woff');
       font-weight: normal;
       font-style: normal;
     }
     ```
   - Example for Google Fonts (preferred when available):
     ```css
     @import url('https://fonts.googleapis.com/css2?family=Open+Sans&display=swap');
     ```

## Adding New Assets

1. Clone the repository: `git clone https://github.com/AskYourPdf/email-assets.git`
2. Follow the established product-based folder structure
3. Optimise all images before adding them (see [Optimisation Tools](#optimisation-tools))
4. Create a pull request with your changes, including:
   - Description of the new assets
   - Which product and email campaign they will be used for

### Optimisation Tools

- **Images**: [TinyPNG](https://tinypng.com/), [Squoosh](https://squoosh.app/), or [ImageOptim](https://imageoptim.com/)
- **Font subsetting**: [Font Squirrel Generator](https://www.fontsquirrel.com/tools/webfont-generator)

## Accessing Assets

All assets are available via direct URLs in the following format:

```
https://raw.githubusercontent.com/AskYourPdf/email-assets/main/[product]/[asset-type]/[sub-folder]/[filename]
```

Example:
```
https://raw.githubusercontent.com/AskYourPdf/email-assets/main/cowriter/images/logos/cowriter-logo.png
```
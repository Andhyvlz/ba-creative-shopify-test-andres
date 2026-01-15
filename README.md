# Shopify Theme Development Test Project

This repository contains the custom Shopify theme development for a technical assessment project.  
The goal is to implement a fully responsive, editable, and brand‑consistent theme based on a provided Figma design, using Shopify Online Store 2.0 standards and GitHub version control.

---

## 📚 Table of Contents
1. [Project Overview](#project-overview)
2. [Tech Stack](#tech-stack)
3. [Repository Structure](#repository-structure)
4. [GitHub Sync Workflow](#github-sync-workflow)
5. [Color Palette & Typography](#color-palette-typography)
6. [Development Workflow](#development-workflow)
7. [Documentation](#documentation)
8. [Implemented Features](#implemented-features)
9. [Product Template Implementation](#product-template-implementation)  
10. [Not Implemented Features](#not-implemented-features)
11. [How I Would Implement These Features & Time Estimates](#how-i-would-implement-these-features-time-estimates)
12. [How to Test the Product Template](#how-to-test-the-product-template)

---

<h2 id="project-overview">📌 Project Overview</h2>
This project is a Shopify theme development test.  
The objective is to reproduce the provided Figma design with high visual accuracy, implement reusable sections, ensure responsive behavior, and maintain clean, scalable code.

Key objectives:
- Match the Figma design with precision  
- Build modular, editable sections  
- Maintain a clean and organized codebase  
- Ensure GitHub synchronization for version control  
- Provide clear documentation for future updates  

---

<h2 id="tech-stack">🛠️ Tech Stack</h2>
- **Shopify Online Store 2.0**
- **Liquid**
- **HTML / CSS / JavaScript**
- **GitHub (version control)**
- **Shopify GitHub Integration**
- **Figma (design source)**

---

<h2 id="repository-structure">📁 Repository Structure</h2>

### 🔧 Technical File Tree (code block)
```md
/assets          → CSS, JS, images  
/config          → theme settings & presets  
/layout          → theme.liquid  
/sections        → editable theme sections  
/snippets        → reusable components  
/templates       → page templates  
/docs            → project documentation  
README.md        → main project documentation
```

### 📘 Descriptive Structure

- **/assets** → Contains CSS, JavaScript, and image files  
- **/config** → Theme settings and preset configurations  
- **/layout** → Main layout file (`theme.liquid`)  
- **/sections** → Editable theme sections used in the Shopify Theme Editor  
- **/snippets** → Reusable Liquid components  
- **/templates** → Page templates (product, collection, index, etc.)  
- **/docs** → Project documentation files  
- **README.md** → Main project documentation  

---

<h2 id="github-sync-workflow">🔄 GitHub Sync Workflow</h2>

This project uses **Shopify’s GitHub integration**.

### Automatic Sync (recommended)
- Any change made in Shopify (code editor or Theme Editor) is automatically committed to GitHub.
- GitHub always stays updated.

### Manual Sync (Shopify CLI)
If working locally:

**Pull theme from Shopify**
```bash
shopify theme pull --store your-store.myshopify.com
```

**Push changes to Shopify**
```bash
shopify theme push
```

**Commit and push to GitHub**
```bash
git add .
git commit -m "Update theme"
git push origin main
```

---

<h2 id="color-palette-typography">🎨 Color Palette & Typography</h2>

### Primary Colors
| Name            | HEX       |
|-----------------|-----------|
| Lavender Light  | `#EDE6F7` |
| Lavender Dark   | `#6E5A82` |
| Black           | `#1A1A1A` |
| White           | `#FFFFFF` |
| Blue‑Gray       | `#8C92A0` |

### Typography
- **Inter** → Body text  
- **Source Serif Pro** → Headings  

---

<h2 id="additional-theme-variants">🧾 Additional Theme Variants</h2>

This theme uses multiple visual schemes across different sections to enhance clarity and contrast.

### 🟣 Body & Header
- Background: `#EDE6F7`  
- Text: `#1A1A1A`  
- Solid button background: `#6E5A82`  
- Solid button label: `#FFFFFF`  
- Outline button: `#6E5A82`  
- Shadow: `#8C92A0`  

This is the primary scheme used across most of the site.

### ⚫ Footer (Dark Variant)
- Background: `#121212`  
- Text: `#FFFFFF`  
- Solid button background: `#121212`  
- Solid button label: `#FFFFFF`  
- Outline button: `#FFFFFF`  
- Shadow: `#1A1A1A`  

Used in the footer to provide visual contrast and separation.

### ⚪ Announcement Bar (Neutral Variant)
- Background: `#F3F3F3`  
- Text: `#121212`  
- Button background: `#121212`  
- Button label: `#F3F3F3`  
- Outline button: `#121212`  
- Shadow: `#121212`  

Used for promotional messages and announcements.

### 🟪 Primary Button Hover
- Button hover background: `#D6CDEB`  
- Button hover text: `#1A1A1A`  

This hover state is applied to primary call-to-action buttons.


---

<h2 id="development-workflow">🧩 Development Workflow</h2>

1. Review the Figma design  
2. Configure theme + GitHub connection  
3. Implement base structure  
4. Build custom sections  
5. Apply color schemes & typography  
6. Add responsive behavior  
7. Test functionality  
8. Client review  
9. Publish theme  

---

<h2 id="documentation">📄 Documentation</h2>

All project documentation is stored inside the `/docs` folder.

- [Step One: Scoping Document](./docs/step-one-scoping.md)

More documentation will be added as the project progresses.

---

<h2 id="implemented-features">🧵 Implemented Features (Step Two Summary)</h2>

- Product template built based on the Figma design
- Full product image gallery using product.media
- Size variants using Shopify’s native variant picker
- Short description using metafield product.metafields.custom.short_description
- USP icons implemented as editable section blocks
- Product accordions powered by metafields (hide if empty)
- Product highlights using metafield list
- Related products using Dawn’s related products section with exclusion of current product
- Layout and spacing aligned with Figma
- Responsive behavior using Dawn’s native responsiveness

---

<h2 id="product-template-implementation">🛠️ Product Template Implementation (Figma Build)</h2>

This section documents the work completed for Step Two of the Shopify Developer Test: building the product template based on the provided Figma design.

### ✅ Product Images
- Full product gallery implemented.
- All images are displayed regardless of variant assignment.
- Featured image updates dynamically when selecting a variant.

#### Original Code
The default theme only displayed the featured image of the selected variant, which caused some images to remain hidden if they were not linked to a variant.

```liquid
{% if media_position >= limit or media_position >= 1 and section.settings.hide_variants and variant_images contains media.src %}
  {% continue %}
{% endif %}
```

#### Modified Code
The gallery was updated to loop through all product images, ensuring every image is displayed:

```liquid
{% if media_position >= limit %}
  {% continue %}
{% endif %}
```

### ✅ Size and Color Variants
- Size variants implemented using Shopify’s native variant picker.
- Color variants are treated as separate products (Sibling Products), as required by the brief.
- A written plan is included instead of a full implementation due to time constraints.

### ✅ Short Product Description
- Implemented using a product metafield.
- Appears below the product title and price.
- Fully editable from the Shopify admin.

### ✅ USP Icons
- Implemented using the “Icon with text” component with horizontal layout.
- Three pairings configured: each includes an image and a heading.
- All three USP entries use the same metafield content per image.
- Icons used:
  - USP 1: return-box.png — “Instant Refunds with Refundid”
  - USP 2: delivery-truck.png — “Free Standard Shipping over $100”
  - USP 3: leather.png — “100% Linen”
- Positioned below the “Buy it now” button, matching the Figma layout.

### ✅ Product Accordions
- Four accordions were implemented using dedicated product metafields:
  - Product Details
  - Age Group
  - Target Gender
  - Dress Style
- Each accordion pulls its content directly from its corresponding metafield.
- Accordions automatically hide when their metafields are empty.
- No Liquid code modifications were required for this section.

### ✅ Product Highlights
- Highlights implemented using a dedicated metafield list.
- Each highlight includes a title, image, and rich‑text description.
- Content is fully managed from the Shopify admin.
- Highlights are displayed in the order defined in the metafield.

### ✅ Related Products
- Implemented using the “You May Also Like” section.
- The current product is excluded from the results using a conditional check.
- Products are pulled from the same collection to maintain relevance.

#### Original Code
The default theme loop displayed every product in the collection, including the current product:

```liquid
{% paginate section.settings.collection.products by section.settings.products_to_show %}
  {% for product in collection.products %}
    <!-- Render related product -->
  {% endfor %}
{% endpaginate %}
```

#### Code Modification
A conditional check was added to prevent the current product from appearing in the related products list:

```liquid

{% assign current = product %}
{% paginate section.settings.collection.products by section.settings.products_to_show %}
  {%- for product in section.settings.collection.products limit: section.settings.products_to_show -%}
   {% if product.id != current.id %}
      <!-- Render related product -->
    {% endif %}
  {% endfor %}
{% endpaginate %}
```

### Implementation in `main-product-fashion.liquid`

This section documents how the product template structure was implemented inside `main-product-fashion.liquid`, following the layout and functional requirements from the Figma design.

#### Product Image Gallery
- The gallery uses `product.media` to display all product images.
- Positioned on the left side of the layout to match the Figma design.
- Variant selection updates the featured image using Shopify’s native behavior.

#### Size Variants
- Implemented using Shopify’s native variant picker.
- Sizes display as XS, S, M, L, XL, XXL.
- Default Dawn behavior preserved for correct variant switching.

#### Color Variants (Sibling Products)
- Color options treated as separate products.
- A comment was added in the Liquid file indicating where sibling products would be rendered.
- The README includes the plan for implementing color swatches using metafields.

#### Short Description
- Implemented using the metafield `product.metafields.custom.short_description`.
- Displayed below the title and price.

#### USP Icons
- Implemented using section blocks inside the schema.
- Each block includes an icon, title, and description.
- Fully editable from the Theme Editor.

#### Product Accordions
- Implemented using metafields for product details, age group, target gender, and dress style.
- Accordions hide automatically when empty.

#### Related Products
- Implemented using Dawn’s existing related products section.
- The current product is excluded from the results.
- Products are pulled from the same collection.

#### Image With Text Section
- Not fully implemented, but the plan is documented.
- A new section would be created with settings for title, text, background image, and alignment.
- Could be made dynamic using metafields or metaobjects.

### ✅ Figma Alignment & Final Notes
- The product template layout follows the Figma design closely, including spacing, hierarchy, and component placement.
- Typography, colors, and visual structure match the design system provided in the brief.
- All functional elements (gallery, variants, accordions, highlights, related products) were implemented to mirror the intended user experience.
- No additional features outside the scope of the Figma file were introduced.
- The template is fully responsive and behaves consistently across desktop and mobile breakpoints.
---

<h2 id="not-implemented-features">🚧 Not Implemented Features</h2>

- Functional sibling products (color swatches linking to separate products)
- Mega menu with featured products/collections
- Collection filters based on metafields
- Shipping progress bar
- Back in stock notification with Klaviyo
- Instagram feed

---

<h2 id="how-i-would-implement-these-features-time-estimates">🧩 How I Would Implement These Features & Time Estimates</h2>

### Sibling Products (Color Swatches)
- Create a metafield to store handles of sibling products.
- Loop through handles to render swatches linking to each product.
- Add active state for current product.
- Estimated time: 2–3 hours.

### Mega Menu
- Create a new section for the mega menu with blocks for featured products/collections.
- Add settings for images, titles, and links.
- Integrate into header.liquid.
- Estimated time: 4–5 hours.

### Collection Filters (Metafields)
- Add metafields for attributes (fabric, fit, length, etc.).
- Create filter UI in collection template.
- Filter products using Shopify’s storefront filtering.
- Estimated time: 3–4 hours.

### Shipping Progress Bar
- Add cart-level script to calculate progress toward free shipping.
- Render progress bar in cart drawer and cart page.
- Estimated time: 2 hours.

### Back in Stock (Klaviyo)
- Install Klaviyo app.
- Enable back-in-stock trigger.
- Add embed code to product template.
- Estimated time: 1 hour.

### Instagram Feed
- Use an app or custom API integration.
- Render grid of latest posts.
- Estimated time: 2–3 hours.

---

<h2 id="how-to-test-the-product-template">🧪 How to Test the Product Template</h2>

- Open the product assigned to the `product.fashion template`.
- Verify the image gallery displays all images.
- Test variant selection for sizes.
- Confirm short description appears under title.
- Check USP icons under the Buy button.
- Expand accordions and confirm empty ones are hidden.
- Scroll to You May Also Like and confirm current product is excluded.
- Review spacing, typography, and layout against the Figma design.


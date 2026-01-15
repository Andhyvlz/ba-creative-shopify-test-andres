# Shopify Theme Development Test Project

This repository contains the custom Shopify theme development for a technical assessment project.  
The goal is to implement a fully responsive, editable, and brand‑consistent theme based on a provided Figma design, using Shopify Online Store 2.0 standards and GitHub version control.

---

## 📚 Table of Contents
1. [Project Overview](#project-overview)
2. [Tech Stack](#tech-stack)
3. [Repository Structure](#repository-structure)
4. [GitHub Sync Workflow](#github-sync-workflow)
5. [Color Palette & Typography](#color-palette--typography)
6. [Development Workflow](#development-workflow)
7. [Documentation](#documentation)

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

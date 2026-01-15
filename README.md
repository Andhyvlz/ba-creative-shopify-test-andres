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

## 📌 Project Overview
This project is a Shopify theme development test.  
The objective is to reproduce the provided Figma design with high visual accuracy, implement reusable sections, ensure responsive behavior, and maintain clean, scalable code.

Key objectives:
- Match the Figma design with precision  
- Build modular, editable sections  
- Maintain a clean and organized codebase  
- Ensure GitHub synchronization for version control  
- Provide clear documentation for future updates  

---

## 🛠️ Tech Stack
- **Shopify Online Store 2.0**
- **Liquid**
- **HTML / CSS / JavaScript**
- **GitHub (version control)**
- **Shopify GitHub Integration**
- **Figma (design source)**

---

## 📁 Repository Structure

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

## 🔄 GitHub Sync Workflow

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

## 🎨 Color Palette & Typography

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

## 🧩 Development Workflow

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

## 📄 Documentation

All project documentation is stored inside the `/docs` folder.

- [Step One: Scoping Document](./docs/step-one-scoping.md)

More documentation will be added as the project progresses.

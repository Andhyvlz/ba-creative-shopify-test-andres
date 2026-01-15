# Step One: Scoping Document

## 1. Project Overview
The purpose of this project is to develop a custom Shopify Online Store 2.0 theme based on the provided Figma design. The goal is to deliver a visually accurate, responsive, and fully editable theme that supports scalable content management, optimized performance, and a clean code structure aligned with Shopify best practices.

The project includes:
- Theme setup and configuration
- Custom section development
- Global styling and typography
- Responsive layout implementation
- Integration of required apps
- Documentation and handover

---

## 2. Theme Recommendation
Based on the project requirements, the recommended approach is:

### **Option A — Custom Theme (Recommended)**
A fully custom theme built from Shopify’s Online Store 2.0 architecture.

**Pros**
- Full control over layout and styling  
- Clean, minimal codebase  
- No unused features  
- Perfect match with Figma design  

**Cons**
- Requires more development time  

### **Option B — Dawn Fork**
Start from Dawn and customize heavily.

**Pros**
- Faster initial setup  
- Built-in accessibility and performance optimizations  

**Cons**
- Extra unused code  
- Harder to maintain long-term  

**Recommendation:**  
A **custom theme** ensures the cleanest implementation and best long-term maintainability.

---

## 3. Data Migration Plan (Products, Customers, Orders — 12 Months)
If the project requires migrating data from another platform or store, the following plan applies:

### **3.1 Products**
- Import via CSV or API  
- Migrate product variants, images, pricing, inventory  
- Create metafields for:
  - Sibling products  
  - Size guides  
  - Additional media  
  - Custom badges  

### **3.2 Customers**
- Import customer list (CSV)  
- Preserve:
  - Email  
  - Phone  
  - Tags  
  - Marketing preferences  

### **3.3 Orders (Last 12 Months)**
- Shopify does not allow direct order import  
- Options:
  - Use a migration app (Matrixify, LitExtension)  
  - Import as “archived orders”  
  - Or store historical orders in a separate dashboard  

### **3.4 Estimated Time**
- Products: 4–6 hours  
- Customers: 2–3 hours  
- Orders: 4–8 hours (depending on method)  

---

## 4. Templates
The theme will include the following templates:

### **4.1 Standard Templates**
- `index.json` — Home  
- `product.json` — Product page  
- `collection.json` — Collection page  
- `cart.json` — Cart  
- `search.json` — Search  
- `page.json` — Standard content pages  
- `blog.json` — Blog listing  
- `article.json` — Blog article  

### **4.2 Custom Templates**
- `product.sibling.json` — Sibling product logic  
- `collection.filtered.json` — Metafield-based filtering  
- `page.custom.json` — Custom landing pages  

### **4.3 Estimated Time**
- Standard templates: 6–8 hours  
- Custom templates: 8–12 hours  

---

## 5. Custom Features
The project includes the following custom features:

### **5.1 Sibling Products**
- Implement metafields to link related products  
- Display sibling variants as clickable swatches or buttons  
- Improve UX for color/style variations  

### **5.2 Metafields**
Used for:
- Product highlights  
- Size guides  
- Additional images  
- Custom badges  
- Collection banners  

### **5.3 Filters by Metafields**
- Use Shopify’s native filtering system  
- Add metafield-based filters:
  - Material  
  - Fit  
  - Style  
  - Color  
  - Season  

### **5.4 Custom Sections**
- Hero banner  
- USP icons  
- Featured collections  
- Testimonials  
- Custom footer  
- Promotional blocks  

### **5.5 Estimated Time**
- Sibling products: 3–5 hours  
- Metafields setup: 2–3 hours  
- Filters: 3–4 hours  
- Custom sections: 10–14 hours  

---

## 6. Timeline & Estimates
| Task | Estimated Hours |
|------|-----------------|
| Theme setup | 2–3 |
| Global styles (colors, typography) | 3–4 |
| Custom sections | 10–14 |
| Templates | 14–20 |
| Metafields & filters | 5–7 |
| Sibling products | 3–5 |
| Data migration | 10–17 |
| QA & responsive testing | 6–8 |
| Documentation | 2–3 |

**Total Estimated Time:**  
**55–81 hours** (depending on complexity)

---

## 7. Assumptions & Risks

### **Assumptions**
- Figma design is final  
- All assets (images, copy, logos) are provided  
- No additional apps beyond the list below  
- No major design changes mid-development  

### **Risks**
- Late design changes may extend timeline  
- Missing content may delay development  
- Third-party apps may conflict with theme code  
- Shopify limitations (e.g., order import) may require workarounds  

---

## 8. Apps & Integrations

### **Recommended Apps**
- **Back in Stock:** Klaviyo Back in Stock or Back in Stock Alerts  
- **Instagram Feed:** Instafeed or Socialwidget  
- **Reviews:** Judge.me or Loox  
- **Search & Filters:** Shopify Search & Discovery  
- **Page Builder (optional):** PageFly or GemPages  
- **Order Migration:** Matrixify  

### **Integration Time Estimates**
- Back in Stock: 1–2 hours  
- IG Feed: 1 hour  
- Reviews: 1–2 hours  
- Filters: 1 hour  
- Page Builder: 1–2 hours  

---

## 9. Final Notes
This scoping document outlines the full technical and functional plan for the Shopify theme development project. It includes all required templates, custom features, data migration considerations, risks, and recommended apps to ensure a smooth and scalable implementation.

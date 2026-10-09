# Website change log

Newest entries at the top. One entry per change or per batch of related changes.

**Entry format** (copy this):

```
## YYYY-MM-DD: Short title
**By:** Name
**Why:** One line on the reason
**Changed:**
- Page URL: what changed (Cornerstone layout/element ID if useful)
**Follow-ups:**
- [ ] Anything left to do
```

---

## 2026-10-08 to 10-09: Separate "Automated Spray Systems" from "Custom Spray Systems"
**By:** Andrew Nighswander
**Why:** Links labeled "automated spray systems" were going to the Custom Spray Systems product (/product/custom-spray-systems/) instead of the Automated Spray Systems page (/automated-spray-systems/).
**Changed:**
- Product post 3246 (/product/custom-spray-systems/): post title renamed to **Custom Spray Systems** (URL unchanged). Every product looper card, plus /sitemap/ and /quick-product-search/, now picks up the new name automatically.
- Home page (/): "Automated Spray Systems" product card now links to /automated-spray-systems/.
- Home page (/): "Spray Systems" tile in the hidden row (Row `e67`, hidden on all breakpoints) now links to /automated-spray-systems.
- /products/: no longer links to the custom systems product.
- No longer link to the custom systems product: /chemical-processing-nozzles-and-injectors/, /meat/, /pet-food/, /food-and-beverage-processing/, /circular-economy-spray-technology/, /bete-spray-technology-for-building-materials-industries/, /bakeries/, /confectionery/.
- "Automated Spray Systems" banner now links to /automated-spray-systems/ on: FlexFlow Industrial, FlexiSan, Spray Headers/Spargers/Spool Sections, Spray Lances/Injectors/Quills (layout 3499).

**Still correctly linking to /product/custom-spray-systems/** (labeled "Custom Spray Systems"): /all-products/, /pattern/automatic/, /product_category/automated-spray-systems/, /quick-product-search/, /sitemap/, /spray_technology_for_data_centers/, /automated-spray-systems/.

**Follow-ups:**
- [ ] Product 3246: change SEO title (still "Automated Spray Systems | BETE Custom Spraying Systems") and page heading (still "AUTOMATED SPRAY SYSTEMS") so it doesn't compete with /automated-spray-systems/ in search
- [ ] Decide on generic "spray system(s)" links: /your-guide-to-selecting-a-spray-nozzle/, /how-to-select-a-nozzle/ (×2), /why-work-with-bete/ (×3)
- [ ] News item "BETE and EXAIR engineer first joint engineered system…": link text is the bare URL
- [ ] Video "Basic operation of the BETE FlexFlow 2000…": URL is plain text, not a link
- [ ] Home page hidden Row `e67`: delete if it's leftover, or add a trailing slash to its Spray Systems link (/automated-spray-systems/) to skip a redirect
- [ ] /tag/spray-systems/ redirects to /product/custom-spray-systems/; confirm that's still the right destination

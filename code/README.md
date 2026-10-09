# Code

Copies of the custom code that runs bete.com. If something breaks, this is what you roll back to.

| Folder | What goes here |
|---|---|
| [css/](css/) | Global CSS from Cornerstone or the theme, plus any page-specific CSS worth keeping |
| [js/](js/) | Global and page-specific JavaScript |
| [snippets/](snippets/) | Exports from the **Snippets** plugin (PHP, CSS and JS snippets) |
| [acf-json/](acf-json/) | Advanced Custom Fields field groups, exported as JSON |
| [cornerstone-exports/](cornerstone-exports/) | Exported Cornerstone layouts, headers, footers and components |
| [email-templates/](email-templates/) | HubSpot and Marketo email or landing page templates |

**How to add or update a file without Git:** open the folder on github.com, then click **Add file → Upload files** (or open the file and click ✏️ to edit). Write a short note and click **Commit changes**.

Name files after what they are, e.g. `product-card-styles.css` or `acf-product-fields.json`, not `final-v2.css`. GitHub keeps every old version automatically.

**Never commit passwords, API keys, license keys or customer data.**

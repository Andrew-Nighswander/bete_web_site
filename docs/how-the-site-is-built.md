# How bete.com is built

bete.com runs on **WordPress** with the **Pro theme and Cornerstone** builder. Content on a page can come from four different places. Before editing, work out which one you're dealing with.

## 1. Regular pages

Pages like the home page, /products/ or /automated-spray-systems/ are normal WordPress pages. They have an **Edit with Cornerstone** option in the admin bar, and what you see is what you edit.

## 2. Layouts that draw a whole page (Single Layouts)

Product pages (/product/...) are drawn by a Cornerstone **Single Layout**, not by the product post itself. At least some products have **their own layout**, for example:

| Product page | Product post ID | Layout ID |
|---|---|---|
| /product/spray-lance-injector-quill-solutions/ | 3500 | 3499 |
| /product/spray-headers-spargers-spool-sections/ | 3589 | 3591 |
| /product/custom-spray-systems/ | 3246 | not yet checked |

**If you open a product post in Cornerstone and see "Uh oh! No suitable preview area found,"** the page is drawn by a layout. Edit the layout instead:

- Go to **Cornerstone → Layouts**, or
- Go straight to `https://bete.com/cornerstone/edit/LAYOUT-ID`

Because products can have their own layout, **fixing something on one product page does not fix it on the others**. Check each one.

## 3. Archive layouts (lists of posts)

Some URLs aren't pages at all. WordPress generates them from a post type or category, so there's **no Edit button** in the admin bar:

- **/all-products/**: the archive of all Products (layout 3137)
- **/product_category/...**: a Product Category archive
- **/pattern/...**: Pattern posts, whose layouts also loop through products

Edit these under **Cornerstone → Layouts → Archive**.

## 4. Loopers (cards filled in from other posts)

Product grids and cards use **Looper Providers**. A card's **title, image and link come from the post it's showing**, not from the layout.

- To change a card's **link**, change that post's URL (slug), or override it in the layout.
- To change a card's **label**, change that post's **title**. This updates every grid, the /sitemap/ page and /quick-product-search/ at once.

Example: renaming product 3246 to "Custom Spray Systems" relabeled its card everywhere in one step.

Some loopers use a **JSON list** typed into the layout instead of posts. The home page "Spray Nozzles, Spray Lances, & Spray Systems" cards work this way, so edit the JSON in the Looper Provider.

## The header and mega menu

The header and mega menu are a separate Cornerstone document that appears on every page. On the live site its elements show as `e78-…`, so document 78 is most likely the header. Edit it under **Cornerstone → Headers**.

## Gotchas

**Hidden doesn't mean gone.** An element hidden on every breakpoint (XS–XL) is still in the page's HTML. Google still crawls its links, and so do link checkers. Delete leftover sections instead of hiding them.

**Element IDs tell you where something lives.** Every Cornerstone element on the live site has a class like `e3499-e152`:

- The first number (`3499`) is the **document** it's in: a page, layout or header.
- The second (`e152`) is the **element** within it.

So `e3499-e152` means "element 152 in layout 3499." See [how-to/find-where-a-link-lives.md](how-to/find-where-a-link-lives.md).

**Links on a Column.** Some clickable tiles are a whole Column with a link set on it, not a button or text link. Select the Column itself to find the URL.

**Cache.** The site is behind Cloudflare. If a change doesn't show up, use **Clear Caches** in the admin bar, then check in a private window.

**Security plugin.** The site's security plugin temporarily blocks anyone who loads many pages very quickly, including link-checker tools. If you get "Your access to this site has been limited," wait a few minutes.

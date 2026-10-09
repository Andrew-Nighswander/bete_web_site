# Find where a link lives

Use this when you know a page has a link you need to change but can't find it in Cornerstone.

## 1. Find which pages link to a URL

The fastest way is to ask Claude: *"Scan bete.com for pages that link to [URL]."* It reads the site's sitemap, checks every page and lists each link with its text.

Without Claude, use **Google Search Console → Links**, or a crawler like Screaming Frog (free up to 500 pages).

## 2. Find the link on the page

1. Open the page in Chrome (logged out, or in a private window).
2. Right-click the link and choose **Inspect**.
3. In the highlighted code, look at the link and the elements around it for a class like `e3499-e152`.

## 3. Read the ID

- **`e3499`** is the document the element is in. Open it at `https://bete.com/cornerstone/edit/3499`.
- **`e152`** is the element. The number alone won't tell you where it sits in the outline, so use the surrounding section's heading or text to find it.

If the document number matches the **page's own post ID**, edit the page normally. If it's a different number, it's a **layout**, or the header if it's `e78`.

## 4. If the link isn't in any document

The link probably comes from a **looper**: the card shows another post's title and URL. Change it on **that post**. See "Loopers" in [how-the-site-is-built.md](../how-the-site-is-built.md).

## 5. Can't see it on the page at all?

It may be on a **hidden** element (hidden on every breakpoint). It's still in the HTML, so search engines still crawl the link. Find it in Cornerstone's outline and delete it or fix its link.

## 6. Log it

Add an entry to [CHANGELOG.md](../../CHANGELOG.md).

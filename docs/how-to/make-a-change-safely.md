# Make a website change safely

## Before you edit

- [ ] Check [how-the-site-is-built.md](../how-the-site-is-built.md) to see whether you need the page, a layout, or the post a looper is pulling from.
- [ ] If you're changing code (CSS, JS, a snippet), copy the current version into this repo first so there's something to roll back to.

## While you edit

- **Changing a URL or slug?** Add a 301 redirect from the old URL to the new one so existing links and Google don't hit a 404.
- **Removing a section?** Delete it rather than hiding it on every breakpoint. Hidden elements stay in the HTML and get crawled.
- **Linking to a page?** Use the full path with a trailing slash, e.g. `/automated-spray-systems/`. Without the slash, visitors go through an extra redirect.

## After you edit

- [ ] Click **Clear Caches** in the admin bar.
- [ ] Check the live page in a private window, on desktop and on a phone.
- [ ] Click any link you added or changed to make sure it doesn't 404.
- [ ] Add an entry to [CHANGELOG.md](../../CHANGELOG.md).
- [ ] If you changed code, put the new version in [code/](../../code/).

## Undoing a change

- **Page or layout:** in Cornerstone, open the document and use **History**, or WordPress **Revisions** on the post.
- **Code:** open the file in this repo, click **History**, and copy back the earlier version.

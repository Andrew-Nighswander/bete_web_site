# BETE Website (bete.com)

This is the home base for bete.com. It holds:

- **A log of every website change**: what changed, where and why ([CHANGELOG.md](CHANGELOG.md))
- **The site's custom code**: CSS, JavaScript, snippets, ACF field groups and Cornerstone exports ([code/](code/))
- **Guides** for making common changes without breaking anything ([docs/](docs/))

You don't need to know Git to use this. Everything can be done in the browser on github.com.

---

## I made a change to the website. What do I do?

1. Open [CHANGELOG.md](CHANGELOG.md) and click the pencil icon (✏️) at the top right.
2. Add your entry at the **top** of the list, using the same format as the entries below it.
3. Scroll down, write a short note such as "Log: updated FlexFlow page hero," and click **Commit changes**.

That's it. GitHub records who made the edit and when.

## I need something changed but can't do it myself

Go to the **Issues** tab, click **New issue** and choose **Website change request**. Fill in the form. Whoever picks it up will log the change when it's done.

## I changed some code (CSS, a snippet, an ACF field group)

Put the updated file in the matching folder under [code/](code/). Each folder's README explains how to export that type of file from WordPress. Then add a line to the changelog.

---

## Where things live on the site

Read **[docs/how-the-site-is-built.md](docs/how-the-site-is-built.md)** before editing in Cornerstone. Some of what you see on a page comes from the page itself, some from a shared layout, and some from the product it's displaying. Knowing which saves a lot of hunting.

## Never put these in this repo

- Passwords, API keys, license keys or login details for anything
- Customer names, contacts, orders or any customer data
- Anything covered by company confidentiality or AI-use policies

If you're unsure, leave it out and ask.

## Access

This repository should be owned by a **company GitHub organization**, not a personal account, so access doesn't depend on any one person. At least two people should have admin rights.

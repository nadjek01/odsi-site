# odsi-site

The public web pages for [Odsi](https://github.com/nadjek01/odsi): a landing page and the
privacy policy. Served by GitHub Pages.

This repo is public because GitHub Pages requires it on a free plan, and a published Pages
site is public regardless. The app source stays in the private `odsi` repo — keep it that way.

## Why this exists

Both app stores require a privacy policy at a stable, reachable URL before you can submit.
That is ticket **ODSI-27** in the build plan, and it is a hard gate — worth clearing early
rather than the week you want to launch.

## Before this goes live

`privacy/index.html` is a **skeleton**. Every highlighted placeholder must be replaced with
what Odsi actually does, and the result reviewed by someone qualified. Publishing it unchanged
would be a false statement about data handling, which is worse than having no policy at all.

The table in it uses the same categories as Apple's App Privacy questionnaire and Google's
Data Safety form, so filling it in honestly also gives you the answers to both.

## Layout

    index.html          landing page
    privacy/index.html  privacy policy (draft)
    style.css           shared styles; palette and type mirror the app's theme.css

No build step. Edit the HTML, push to `main`, Pages redeploys.

## Custom domain

Add a `CNAME` file containing the domain and point a DNS record at GitHub Pages. HTTPS is
issued automatically once DNS resolves.

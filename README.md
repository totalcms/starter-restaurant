# Copper Thistle

A restaurant website built on [Total CMS](https://totalcms.co). It looks like a printed bill of fare in two inks, and comes with a menu, weekly specials, opening hours, a photo gallery and contact details. Every page is filled with demo content, so the site works as soon as it's installed.

## Install

The easiest way is Total CMS Studio: choose **New Site…**, pick **Restaurant**, and Studio sets everything up on your Mac.

With Composer:

```bash
composer create-project totalcms/starter-restaurant mysite
cd mysite
npm install && npm run build
```

Point your web server's document root at `mysite/public/`, then visit the site. The setup wizard creates your admin account.

## Make it yours

- **Content.** Sign in at `/admin` to edit the menu, specials, hours, gallery and restaurant details. The Help pages in the admin show how to do everyday jobs, like changing a price or adding holiday hours.
- **Colors.** Every color comes from four settings in `css/theme.css`: `--yeti-hue-primary`, `--yeti-hue-secondary`, `--yeti-hue-neutral` and `--yeti-chroma`. Change those and the cover, accents and buttons follow, in light and dark mode. `DESIGN.md` explains the whole design system.
- **Templates.** The pages, layouts and partials are Twig files in `builder/`.
- **CSS and JavaScript.** Edit `css/` and `js/`, then build them with `npm run build`, or keep `npm run watch` running while you work. `FRONTEND.md` has the details.

## Photos

The demo photos come from Pexels, and `CREDITS.md` credits each photographer. Replace them with the restaurant's own photos before the site goes live.

## Going live

The site starts in Development mode, so you can edit the templates in the admin while you build. Before you deploy, set **Site Environment** to **Production** in the admin's General settings. Production keeps error messages short for visitors and makes the template editor read-only, so the live site's templates change only when you deploy them.

## Requirements

PHP 8.2 or later, Node.js to build the CSS and JavaScript, and a Total CMS license for the domain you deploy to.

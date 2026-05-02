# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static HTML website for nellscovell.com — the professional site of Nell Scovell (writer, producer, director). Migrated from WordPress in 2026 to pure static HTML/CSS. Hosted on GitHub Pages.

Migrated from WordPress (which had blog feed, comments, subscriptions, sidebar archives). The static version keeps the substantive content pages and drops WordPress-specific features. Blog posts are rare (~4/year) and hand-crafted as standalone HTML files when needed.

## Development

No build system, package manager, or JavaScript. Pure static HTML/CSS served as-is.

To preview locally: `python3 -m http.server`

## Architecture

- **style.css** — Single site-wide stylesheet (CSS variables, flexbox/grid layout, responsive, CSS-only hamburger menu)
- **index.html** — Homepage with author intro and highlights (replaces the WordPress blog feed)
- **Root HTML files** — One per nav section: about.html, the-book.html, praise.html, published-writing.html, on-the-web.html, events.html, contact.html
- **images/** — All site images (headshots, book covers, etc.)
- **CNAME** — GitHub Pages custom domain config for nellscovell.com. Do not delete.

## Content Notes

- Published Writing page includes book cover thumbnails linked to Amazon
- On The Web page is a chronological list of articles with links to external outlets; also links to Authory archive for the full collection
- Contact page has literary agent, talent agent, and publisher/PR contacts
- External links use `target="_blank" rel="noopener"`
- Events page content is from 2018 book tour — historical archive
- Praise page has blurbs for *Just the Funny Parts* (from John Oliver, Bette Midler, George Lucas, Kirkus, etc.)
- WordPress "Directors Reel" page was an empty stub and was not migrated

## Conventions

- HTML5 doctype with UTF-8 encoding
- Responsive viewport (`width=device-width, initial-scale=1.0`)
- Single stylesheet linked from all pages
- All pages share a common nav and footer
- No JavaScript
- Follow the same patterns as the sibling sites in this GitHub Pages setup (mightycheese, otlstudio, pogsummers)

## Deployment

GitHub Pages — push to main to deploy. No build step.

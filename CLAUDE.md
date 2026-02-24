# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Niceify is a static landing page for a macOS app (AI-powered text editing tool). Hosted on GitHub Pages at niceify.app.

## Tech Stack

- Pure HTML (no framework, no templating)
- Tailwind CSS v4 loaded from CDN (`@tailwindcss/browser@4`) — no build step
- No JavaScript, no package manager, no bundler

## Development

There are no build, lint, or test commands. To develop, open `index.html` directly in a browser or use any local HTTP server.

## Architecture

Two standalone HTML pages sharing the same visual design (copy-pasted structure, not templated):

- `index.html` — Landing page with hero, features grid, and Mac App Store CTA
- `privacy-policy.html` — Privacy policy document

Custom inline CSS exists only for hero gradient backgrounds and text shadows. Everything else uses Tailwind utility classes.

## Deployment

Push to `main` branch triggers GitHub Pages deployment. The `CNAME` file maps to `niceify.app`.

## Conventions

- Mobile-first responsive design using Tailwind `lg:` breakpoints
- Color scheme: primary blue `#002f5a`, background `#FBFDFF`
- Content is constrained to `max-w-4xl`
- When changing shared visual elements (header, footer, meta tags), update both HTML files

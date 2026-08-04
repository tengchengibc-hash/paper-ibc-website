# agent.md — Project Context Memory

## What this project is
A static marketing website (independent site) for Mofort Paper IBC — Qingdao Tengcheng Packaging Co., Ltd.
Target audience: overseas B2B buyers of Paper IBC / bulk liquid packaging.

## Tech stack
- Static HTML multi-page site (no build step)
- Tailwind CSS via CDN (https://cdn.tailwindcss.com) with brand colors
- Google Fonts: Inter
- No backend; inquiry via mailto form + WhatsApp deep links

## Directory structure
- index.html — home
- products.html — IBC-6S/6P/7S/8MAX + BOX-1410S/P/MAX spec tables
- technology.html — continuous wrap, patent CN 223764942 U, ISTA 3E testing
- cases.html — 10 application cases
- contact.html — phones, email, WhatsApp, quote form
- assets/images/ — real product/test photos (replace with newer shots as available)

## Brand rules
- Brand name: Mofort (MoFort). Company: Qingdao Tengcheng Packaging Co., Ltd.
- Contact: Manager Wang, +86 158 6680 7268 / +86 159 6328 7268, tengchengibc@gmail.com
- WhatsApp links: wa.me/8615866807268 and wa.me/8615963287268
- Do NOT claim UN dangerous-goods certification; ISTA 3E-2026 + CNAS L21623 only.
- All spec values must match the final engineering manual (wall = layers×5mm+1mm; folded = wall×2+12mm).

## How to iterate
1. Read this file first.
2. Edit the matching HTML file directly (static site, no build).
3. Keep the same design system (Tailwind classes, brand colors).
4. Update WhatsApp/email/phone in every page if contact info changes.

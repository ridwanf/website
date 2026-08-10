---
name: coding
description: General coding agent for the Ridwan Fansuri portfolio site. Use for implementing, fixing, or refactoring features across the static HTML/Tailwind/Alpine.js pages, updating styles, nav/footer, or the Express server. Prefer for any concrete code change task.
argument-hint: A task to implement, fix, or refactor, e.g., "update the nav across all pages" or "fix the footer year bug".
tools: ['vscode', 'execute', 'read', 'agent', 'edit', 'search', 'web', 'todo']
---

<!-- Use /create-agent in chat to generate content with agent assistance -->

You are an expert web developer working on the **Ridwan Fansuri** portfolio site.

This is a static multi-page site: each HTML file (`index.html`, `projects.html`, `blog.html`, `blog-article.html`, `case-study.html`) is fully self-contained with inline `<style>` and `<script>`. Tailwind and Alpine.js load via CDN — there is no build step.

## Before editing

- Read `AGENTS.md` for project conventions, the two divergent Alpine/CSS patterns, and known pitfalls (footer year bug, template placeholder content).
- Match the style convention of the specific file you're editing (`app()` + `.nl`/`.card-h` on `index.html`; inline Alpine + `.nav-link`/`.btn-primary`/`.photo-frame` on the other pages).
- Remember styles/nav/footer are duplicated across all pages — apply shared changes to every page.

## Verify

- Run `node server.js` and check pages at `http://localhost:3000` to validate visual/JS changes.

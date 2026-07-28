# AGENTS.md (Hextra Skill)

This file provides guidance to AI coding agents when working with Hextra theme and Hugo in this repository.

## Project Overview

Hextra is a modern, responsive Hugo theme designed for creating documentation websites, technical blogs, and static sites. Built with Tailwind CSS, it offers features like full-text search, dark mode, multi-language support, and extensive customization options.

## Architecture Overview

### Hugo Theme Structure

- **Base Layout**: `layouts/baseof.html` wraps all pages
- **Specialized Layouts**: `layouts/docs/`, `layouts/blog/`, `layouts/hextra-home.html`
- **Partials**: Reusable components in `layouts/_partials/`
  - Core UI: `navbar.html`, `sidebar.html`, `footer.html`, `breadcrumb.html`, `toc.html`
  - Utilities: `layouts/_partials/utils/` for helper functions
  - Custom overrides: `layouts/_partials/custom/` for user customizations
- **Shortcodes**: Custom Markdown extensions in `layouts/_shortcodes/`
- **Render Hooks**: Custom Markdown rendering in `layouts/_markup/` for codeblocks, headings, images, and links

### Key Components

- **Search**: FlexSearch-powered full-text search (`assets/js/flexsearch.js`)
- **Navigation**: Responsive navbar and auto-generated sidebar
- **Theme Toggle**: Dark/light mode switching
- **Internationalization**: Multi-language support

### Content Features

- **Shortcodes**: `callout`, `card`, `cards`, `tabs`, `tab`, `details`, `steps`, `filetree`, `jupyter`, `badge`, `icon`, `pdf`, `include`, `asciinema`, `term`
- **Code Features**: Syntax highlighting (Chroma), copy buttons, line numbers via render hooks
- **SEO**: Open Graph, Twitter Cards, structured data

---
layout: default
title: How to Add Pages
nav_order: 10
---

## Overview

This document explains how to create new top-level sections ("tabs") and subpages in the SIGPhil repository’s documentation using the GitHub web interface and the Just‑the‑Docs theme.

### Creating a Top‑Level Section

1. Navigate to the repository on GitHub.  
2. Click **Add file** and select **Create new file**.  
3. In the file name box, enter a name ending with `.md` such as `research-topics.md`.  
4. At the top of the new file, add YAML front matter:  
   ```
   ---
   layout: default
   title: Research Topics
   nav_order: 3
   has_children: true
   ---
   ```
5. Add a heading and description below the front matter.  
6. Commit the new file directly to the `main` branch.

### Adding a Child Page

1. From the repository’s main page, click **Add file** → **Create new file** again.  
2. Name the file something like `introduction-to-topic.md`.  
3. Add front matter similar to:  
   ```
   ---
   layout: default
   title: Introduction to Topic
   parent: Research Topics
   nav_order: 1
   ---
   ```
4. Write your page content below the front matter.  
5. Commit the file directly to the `main` branch.

### Notes

- The `title` value appears in the sidebar.  
- The `parent` value must match the title of the parent section exactly.  
- The `nav_order` determines the order of entries in the sidebar; lower numbers appear first.  
- After committing a new page, wait a minute for GitHub Pages to rebuild the site.

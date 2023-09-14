---
layout: post
title: Creating and customizing your al-folio website
date: 2023-09-13
tags: website
categories: misc-resources
---

I recently had to re-create my website, and it was difficult enough to remember how I customized it that I thought it would be useful to write down the steps I took.


1. Follow the [README instructions](https://github.com/alshedivat/al-folio) to get set-up. @alshediva keeps it pretty up to date. I found it complicated the process to try to take advantage of outside how-to sources. 

2. Go through the `_config.yml` file and make what should be obvious personlization edits.

   a. Change the following line:

   ```
   imagemagick: // enabled: false
   ```

3. Add your CV to a `assets/pdf/CV.pdf` and your picture to `assets/img/prof_pic.jpg`.

4. For my CV formatting, replace the text in `_layouts/cv.html` with the following:

   ```
   --- layout: default ---
   { { page.title } } {% if page.cv_pdf %}{% endif %}
   { { page.description } }
   ```

5. Re-name and re-order all your pages by editing the header in their respective file in the `_pages` directory.

6. Customize your blog

   - In `_config.yml`, change `pagination // enabled = FALSE` to remove the blog entirely. If you're keeping the blog, remove the lines under `external_sources:`.
   - To re-order the location of the blog page navigation, move the appropriate block in `_includes/header.html`.
   - Empty the `_posts` directory.
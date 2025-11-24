# Lesson-LMS-WordPress-Theme-Development

> A clean, lightweight WordPress theme built for LMS (Learning Management System) style sites. This repository contains the theme files and installation instructions so you (or a client) can install and set up the theme quickly.

---

## Table of Contents

1. [About](#about)
2. [Requirements](#requirements)
3. [Install — Step by step](#install---step-by-step)

   * [Method A — Upload ZIP via WordPress Dashboard (recommended)](#method-a---upload-zip-via-wordpress-dashboard-recommended)
   * [Method B — Upload via FTP / cPanel](#method-b---upload-via-ftp--cpanel)
   * [Method C — Install via Git (advanced)](#method-c---install-via-git-advanced)
   * [Method D — WP-CLI (advanced)](#method-d---wp-cli-advanced)
4. [Activate & Basic Setup](#activate--basic-setup)
5. [Recommended / Required Plugins](#recommended--required-plugins)
6. [Demo Content (optional)](#demo-content-optional)
7. [Theme Options & Customization](#theme-options--customization)
8. [Troubleshooting](#troubleshooting)
9. [Developer Notes](#developer-notes)
10. [Changelog](#changelog)
11. [License & Credits](#license--credits)
12. [Support](#support)

---

## About

Lesson-LMS is designed as a minimal, performance-minded WordPress theme for online course sites and simple LMS setups. It focuses on:

* Clean layout for course lists, single lessons, and teacher profiles
* Responsive design
* Easy integration with popular LMS plugins or page builders

---

## Requirements

* WordPress 6.0+ (recommended latest stable)
* PHP 7.4+ (PHP 8.x recommended)
* MySQL 5.7+ or MariaDB 10.2+
* Recommended `memory_limit` ≥ 256M, `upload_max_filesize` ≥ 16M

---

## Install — Step by step

> Use the method that fits your access level. The Dashboard ZIP upload is easiest for most users.

### Method A — Upload ZIP via WordPress Dashboard (recommended)

1. Compress the theme folder into `lesson-lms.zip`.
2. Login to your WordPress admin → **Appearance → Themes → Add New → Upload Theme**.
3. Choose `lesson-lms.zip` and click **Install Now**.
4. After upload completes click **Activate**.

### Method B — Upload via FTP / cPanel

1. Unzip the theme archive locally.
2. Connect to your server with FTP (or cPanel File Manager).
3. Upload the theme folder to `/wp-content/themes/lesson-lms/`.
4. In WP admin go to **Appearance → Themes** and activate **Lesson-LMS**.

### Method C — Install via Git (advanced)

> Useful for developers who want to keep the theme under version control on the server.

1. SSH into your server and `cd` into the WordPress themes folder:

```bash
cd /path/to/wordpress/wp-content/themes/
git clone https://github.com/RHS-Rabbi/Lesson-LMS-WordPress-Theme-Development.git lesson-lms
```

2. In WP Admin → **Appearance → Themes** you should see the theme—Activate it.

> If your hosting prevents `git clone` in the webroot, use a local clone and upload via FTP or CI pipeline.

### Method D — WP-CLI (advanced)

If WP-CLI is installed you can install and activate the theme from a zip:

```bash
wp theme install /path/to/lesson-lms.zip --activate
```

Or clone into themes and activate:

```bash
cd wp-content/themes
git clone https://github.com/RHS-Rabbi/Lesson-LMS-WordPress-Theme-Development.git lesson-lms
wp theme activate lesson-lms
```

---

## Activate & Basic Setup

1. Activate the theme (Appearance → Themes → Activate).
2. Go to **Appearance → Customize** and set site identity, menus, and homepage settings.
3. Create these pages (if your theme expects them): Home, Courses, Lessons, Profile, Contact.
4. Assign a static page or blog page at **Settings → Reading** if needed.

---

## Recommended / Required Plugins

> The theme itself is lightweight; for LMS features you will likely use an LMS plugin. Below are suggestions — install only what you need.

* **Recommended (examples):**

  * LearnPress / LifterLMS / Tutor LMS (choose one if you need full LMS functionality)
  * Elementor (for page building)
  * Contact Form 7 or WPForms (for contact pages)
  * Classic Editor or Gutenberg plugins if you rely on specific editor behavior

* **Optional utilities:**

  * Yoast SEO or Rank Math (SEO)
  * WP Super Cache / W3 Total Cache or WP Rocket (caching)
  * UpdraftPlus (backup)

> If the repository includes a `required-plugins.txt` or a TGM plugin installer, follow its instructions to install bundled plugins.

---

## Demo Content (optional)

If you provide demo content (XML) with the theme, import it via **Tools → Import → WordPress**:

1. Install the WordPress importer plugin when prompted.
2. Upload the demo XML file and follow the import steps (assign authors, import attachments).
3. After import, go to **Appearance → Menus** & **Customizer** to adjust menus and widgets.

---

## Theme Options & Customization

* **Customizer:** Appearance → Customize — logo, colors, typography, header & footer options.
* **Menus:** Appearance → Menus — assign primary and footer menus.
* **Widgets:** Appearance → Widgets — place widgets in available sidebars/footer areas.
* **Page Templates:** Use theme-provided templates for Course List, Single Course, Landing Page, etc.

If your theme provides a `theme-options` page, you will see it as a top-level admin menu — open it to configure theme-specific settings.

---

## Troubleshooting

**Blank page / PHP error**

* Enable `WP_DEBUG` in `wp-config.php` to see error messages.
* Check PHP version and increase `memory_limit`.

**Styles/CSS missing**

* Clear caches (server cache, CDN, browser cache).
* Make sure `style.css` header is present and the theme folder name is correct.

**Plugins not working**

* Deactivate other plugins to check for conflicts.
* Make sure required plugins are installed and activated.

---

## Developer Notes

* Main theme files live in `/` (index.php, style.css, functions.php, etc.).
* Templates: `/template-parts/`, `/inc/`, `/assets/` (scripts, styles, images).
* Use `wp_enqueue_style()` and `wp_enqueue_script()` to add assets.
* If building child themes, include a `Template: lesson-lms` header in child `style.css`.

---

## Changelog

* **v1.0** — Initial release.

(Keep this section updated as you release new versions.)

---

## License & Credits

This project is distributed under the **MIT License**. See the `LICENSE` file for details.

Credits:

* Theme developed by **RHS-Rabbi**.

---

## Support

If you find bugs or want to request features, please open an **Issue** in this repository or contact the maintainer.

---

**Need a ZIP of the theme, or a quick `functions.php` snippet for demo import / required plugins?**
Tell me which one and I will generate it for you.

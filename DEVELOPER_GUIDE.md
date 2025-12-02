# Developer Documentation - Hugo Academic CV Website

**Comprehensive Guide for Website Management and Development**

---

## Table of Contents

1. [Overview](#overview)
2. [Technology Stack](#technology-stack)
3. [Project Structure](#project-structure)
4. [Configuration Files](#configuration-files)
5. [Content Management](#content-management)
6. [Theming & Customization](#theming--customization)
7. [Deployment](#deployment)
8. [Development Workflow](#development-workflow)
9. [Troubleshooting](#troubleshooting)

---

## Overview

### What is This Site?

This is a Hugo-based academic CV website built with the **Hugo Blox Academic CV** template (formerly Hugo Academic). It's a static site generator that creates a fast, secure, and SEO-optimized personal academic website.

### Key Features

- Single-page and multi-section layout
- Publications management with citations
- Events/talks timeline
- Experience and education display
- Responsive design with dark/light mode
- SEO optimized
- Social media integration
- Favicon and logo customization

### Live Site
- **URL**: https://bahmanmdd.github.io
- **Repository**: https://github.com/bahmanmdd/bahmanmdd.github.io
- **Hosting**: GitHub Pages

---

## Technology Stack

### Core Technologies

| Technology | Version | Purpose |
|------------|---------|---------|
| **Hugo** | Extended version | Static site generator |
| **Hugo Blox** | v0.10.0 | Academic theme framework |
| **Tailwind CSS** | Via Hugo Blox | Styling framework |
| **Go Modules** | Go 1.19+ | Dependency management |
| **GitHub Pages** | - | Deployment & hosting |

### Module Dependencies

```yaml
# From go.mod
github.com/HugoBlox/hugo-blox-builder/modules/blox-plugin-netlify v1.1.2
github.com/HugoBlox/hugo-blox-builder/modules/blox-tailwind v0.10.0
```

---

## Project Structure

### Directory Layout

```
bahmanmdd.github.io/
├── .git/                       # Git version control
├── .github/workflows/          # GitHub Actions (auto-deploy)
├── assets/                     # Source assets
│   └── media/                  # Site media files
│       ├── icon.png           # Browser favicon (simple BM logo)
│       ├── logo.png           # Navbar logo (stylized BM logo)
│       ├── sharing.png        # Social media preview image
│       ├── stacked-peaks.svg  # Background graphic
│       └── icons/             # Icon library
├── config/_default/            # Configuration files
│   ├── hugo.yaml              # Main Hugo config
│   ├── params.yaml            # Site parameters
│   ├── menus.yaml             # Navigation menus
│   ├── languages.yaml         # i18n settings
│   └── module.yaml            # Hugo modules config
├── content/                    # All content
│   ├── _index.md              # Homepage
│   ├── authors/admin/         # User profile
│   ├── publications/          # Research papers
│   ├── events/                # Talks & conferences
│   ├── experience.md          # Work & education
│   ├── skills.md              # Skills & languages
│   ├── supervision/           # Student supervision
│   └── courses/               # Teaching
├── data/                       # Data files (if needed)
├── layouts/                    # Custom layout overrides
├── static/                     # Static files (served as-is)
│   └── uploads/               # Downloadable files (e.g., resume)
├── master/                     # Personal files (gitignored)
│   └── logo_archive/          # Archived logo versions
├── public/                     # Generated site (gitignored)
├── resources/                  # Hugo cache (gitignored)
├── .gitignore                  # Git ignore rules
├── go.mod                      # Go module definition
├── go.sum                      # Go module checksums
├── hugo_stats.json             # Hugo build stats
├── LICENSE.md                  # License file
├── README.md                   # Project readme
├── CONTENT_UPDATE_GUIDE.md     # Quick content guide
└── netlify.toml                # Netlify config (optional)
```

---

## Configuration Files

### 1. `config/_default/hugo.yaml`

**Purpose**: Main Hugo configuration

```yaml
# Website name
title: Bahman Madadi

# Website URL  
baseURL: 'https://example.com/'

# Language
defaultContentLanguage: en
hasCJKLanguage: false

# Advanced settings
enableGitInfo: false
summaryLength: 30
pagination:
  pagerSize: 10
enableEmoji: true
enableRobotsTXT: true

# Output formats
outputs:
  home: [HTML, RSS, headers, redirects, backlinks]
  section: [HTML, RSS]

# Image processing
imaging:
  resampleFilter: lanczos
  quality: 90
  anchor: smart

# Taxonomies
taxonomies:
  author: authors
  tag: tags
  publication_type: publication_types
```

**Key Parameters**:
- `title`: Browser tab title and site name
- `baseURL`: Production URL (update for custom domains)
- `summaryLength`: Preview text length (words)
- `pagerSize`: Items per page in lists

---

### 2. `config/_default/params.yaml`

**Purpose**: Site appearance and features

```yaml
# Appearance
appearance:
  mode: system          # Options: light, dark, system
  color: cyan          # Theme color

# SEO
marketing:
  seo:
    site_type: Person
    description: 'Your site description'
  analytics:
    google_analytics: ''  # Add GA ID
  
# Site header  
header:
  navbar:
    enable: true
    block: 'navbar'
    fixed_to_top: true
    show_search: true
    show_theme_chooser: true
    logo:
      text: 'Bahman Madadi'  # Navbar text (logo.png used if exists)

# Site footer
footer:
  copyright:
    notice: '© {year} Me. This work is licensed under {license}'
    license:
      enable: true
      allow_derivatives: false
      share_alike: true
      allow_commercial: false
```

**Key Parameters**:
- `appearance.mode`: Theme mode (light/dark/system)
- `appearance.color`: Primary color scheme
- `header.navbar.logo.text`: Navbar branding text
- `marketing.seo`: SEO metadata
- `footer.copyright`: Footer text and licensing

**Available Colors**: 
`red`, `pink`, `purple`, `indigo`, `cyan`, `teal`, `green`, `lime`, `amber`, `orange`, `brown`, `grey`

---

### 3. `config/_default/menus.yaml`

**Purpose**: Navigation menu configuration

```yaml
main:
  - name: Bio
    url: /
    weight: 1
  - name: Experience
    url: experience
    weight: 2
  - name: Publications
    url: publications
    weight: 3
  - name: Events
    url: events
    weight: 4
```

**Parameters**:
- `name`: Display text
- `url`: Page path (relative to content/)
- `weight`: Order (lower = earlier)

---

### 4. `config/_default/module.yaml`

**Purpose**: Hugo Blox modules and mounts

```yaml
imports:
  - path: github.com/HugoBlox/hugo-blox-builder/modules/blox-plugin-netlify
  - path: github.com/HugoBlox/hugo-blox-builder/modules/blox-tailwind

mounts:
  - source: hugo-blox/blox/community
    target: layouts/_partials/blox/community/
  # ... additional mounts
```

**Note**: Don't modify unless adding custom blocks or changing theme

---

## Content Management

### Content Organization

Hugo Blox uses a **folder-per-item** structure for publications and events.

### Front Matter Structure

#### Publications (`content/publications/*/index.md`)

```yaml
---
title: 'Paper title'
authors:
  - admin                              # Always 'admin' for yourself
  - Co-author Name
date: '2024-01-01T00:00:00Z'          # Publication date
publication_types: 
  - 'article-journal'                  # or 'paper-conference', 'thesis'
publication: '*Journal Name*, Volume(Issue), Pages'
featured: true                         # Show on homepage
hugoblox:
  ids:
    doi: 10.xxxx/xxxxx                 # DOI
links:
  - type: pdf
    url: https://doi.org/...
  - name: Code
    url: https://github.com/...
  - name: Dataset created
    url: https://doi.org/...
---

Optional abstract/description in Markdown
```

**Publication Types**:
- `'article-journal'` - Journal article
- `'paper-conference'` - Conference paper  
- `'thesis'` - PhD/Masters thesis
- `'book'` - Book
- `'chapter'` - Book chapter

#### Events (`content/events/*/index.md`)

```yaml
---
title: 'Talk/presentation title'
event: 'Conference Name'
location: City, Country
summary: 'Brief description'
date: '2024-06-01T00:00:00Z'
all_day: true
authors:
  - admin
featured: true
---

Optional detailed description
```

#### Author Profile (`content/authors/admin/_index.md`)

```yaml
---
# Display name
title: Bahman Madadi

# Role/position
role: Transport Analyst

# Organizations
organizations:
  - name: Organization Name
    url: https://...

# Short bio
bio: 'Your bio text'

# Interests
interests:
  - Network Design
  - Machine Learning

# Education
education:
  courses:
    - course: PhD in Transport
      institution: University
      year: 2021

# Social/contact
profiles:
  - icon: at-symbol
    url: 'mailto:your@email.com'
  - icon: brands/linkedin
    url: https://linkedin.com/in/...
  - icon: brands/github
    url: https://github.com/...
---

Bio content in Markdown
```

#### Homepage (`content/_index.md`)

```yaml
---
title: ''  # Leave empty to use site title
date: 2022-10-24
type: landing

sections:
  - block: resume-biography-3      # Bio section
    content:
      username: admin
      button:
        text: Download Resume
        url: uploads/BahmanMadadi_Resume.pdf
    design:
      avatar:
        size: medium
        shape: circle
        
  - block: collection              # Publications
    id: papers
    content:
      title: Featured Publications
      filters:
        folders:
          - publications
        featured_only: true
    design:
      view: article-grid
      columns: 2
---
```

**Available Blocks**:
- `resume-biography-3` - Bio with avatar
- `collection` - List of content (pubs, events)
- `markdown` - Custom markdown content
- `experience` - Timeline view
- `skills` - Skills/languages grid

---

## Theming & Customization

### Brand Assets

| Asset | Location | Size | Purpose |
|-------|----------|------|---------|
| **Favicon** | `assets/media/icon.png` | 512x512px | Browser tab |
| **Logo** | `assets/media/logo.png` | 512x512px | Navbar |
| **Social** | `assets/media/sharing.png` | 1200x630px | Social previews |
| **Avatar** | `content/authors/admin/avatar.jpg` | Any square | Profile picture |

**Current Branding**:
- Favicon: Simple cyan "BM" on black background
- Logo: Stylized cyan "BM" with curves and glow
- Social: Same as logo (1200x630px dimensions)

### Color Customization

**Location**: `config/_default/params.yaml`

```yaml
appearance:
  mode: system      # light, dark, or system
  color: cyan       # Primary theme color
```

### Custom CSS/Styling

Create `assets/css/custom.css` for overrides:

```css
/* Example: Custom styling */
.navbar {
  /* Your custom styles */
}
```

Then reference in `config/_default/params.yaml`:

```yaml
plugins_css:
  - 'custom'
```

### Layout Customization

To override theme layouts:

1. Copy from theme: `themes/hugo-blox/.../template.html`
2. Paste to: `layouts/.../template.html`
3. Modify as needed

**Note**: Rarely needed - Hugo Blox is highly configurable

---

## Deployment

### GitHub Pages Setup

The site auto-deploys to GitHub Pages via GitHub Actions.

**Workflow**: `.github/workflows/hugo.yml`

```yaml
# Builds and deploys on push to main branch
name: Deploy Hugo site to Pages

on:
  push:
    branches: ["main"]
  workflow_dispatch:

# ... (auto-configured)
```

### Deployment Process

1. **Push to GitHub**:
   ```bash
   git add .
   git commit -m "Update content"
   git push
   ```

2. **Auto-build**: GitHub Actions runs Hugo build

3. **Deploy**: Publishes to `gh-pages` branch

4. **Live**: Site updates in ~2-5 minutes

**Check build status**: Repository → Actions tab

### Custom Domain (Optional)

1. Add `CNAME` file to `static/` with your domain
2. Configure DNS:
   ```
   Type: CNAME
   Name: www
   Value: bahmanmdd.github.io
   ```
3. Update `baseURL` in `config/_default/hugo.yaml`

---

## Development Workflow

### Local Development

1. **Install Hugo Extended** (v0.110+):
   - Download: https://gohugo.io/installation/
   - Verify: `hugo version`

2. **Clone repository**:
   ```bash
   git clone https://github.com/bahmanmdd/bahmanmdd.github.io.git
   cd bahmanmdd.github.io
   ```

3. **Install dependencies**:
   ```bash
   hugo mod get -u
   ```

4. **Run local server**:
   ```bash
   hugo server
   ```
   Visit: http://localhost:1313

5. **Make changes** in `content/` or `config/`

6. **Auto-reload**: Browser updates on save

### Building for Production

```bash
hugo --gc --minify
```

Output in `public/` directory.

### Git Workflow

```bash
# Check status
git status

# Stage changes
git add .

# Commit
git commit -m "Descriptive message"

# Push
git push origin main
```

**Branch Strategy**: 
- `main` - Production (auto-deploys)
- Feature branches optional

---

## Troubleshooting

### Common Issues

#### Site Not Updating After Push

**Causes**:
1. GitHub Actions failed
2. Browser cache
3. DNS propagation (custom domains)

**Solutions**:
- Check Actions tab for errors
- Hard refresh (Ctrl+F5)
- Clear browser cache
- Wait 5-10 minutes for build

#### Favicon Not Showing

**Solution**:
- Ensure `assets/media/icon.png` exists
- Hard refresh (Ctrl+F5)
- Try incognito/private window
- Browsers cache favicons aggressively

#### Logo Not Appearing in Navbar

**Check**:
- `assets/media/logo.png` exists
- Correct file name (lowercase)
- File size reasonable (<1MB recommended)

#### Hugo Build Errors

**Common fixes**:
```bash
# Update modules
hugo mod get -u
hugo mod tidy

# Clear cache
hugo mod clean
rm -rf public/ resources/

# Rebuild
hugo server
```

#### Content Not Displaying

**Check**:
- Front matter YAML syntax (correct indentation)
- File named `index.md` (not `Index.md`)
- Folder structure matches convention
- Date format: `'YYYY-MM-DDTHH:MM:SSZ'`

### Debug Mode

Run Hugo with verbose output:

```bash
hugo server --verbose --debug
```

### Getting Help

- **Hugo Blox Docs**: https://docs.hugoblox.com
- **Hugo Docs**: https://gohugo.io/documentation/
- **Hugo Blox Community**: https://github.com/HugoBlox/hugo-blox-builder/discussions

---

## Advanced Topics

### Adding Custom Blocks

Create custom content blocks in `layouts/partials/blox/`.

Example: `layouts/partials/blox/custom-block.html`

Reference in content pages:
```yaml
sections:
  - block: custom-block
    content:
      # Your content
```

### Custom Shortcodes

Create in `layouts/shortcodes/myshortcode.html`.

Use in markdown:
```markdown
{{% myshortcode %}}
```

### Google Analytics

Add tracking ID in `config/_default/params.yaml`:

```yaml
marketing:
  analytics:
    google_analytics: 'G-XXXXXXXXXX'
```

### Multi-language Support

Configure in `config/_default/languages.yaml`:

```yaml
en:
  languageName: English
  weight: 1
  
fr:
  languageName: Français
  weight: 2
```

Create language-specific content:
- `content/en/`
- `content/fr/`

---

## File Permissions & Security

### Gitignored Files

The following are excluded from version control (`.gitignore`):

```
# Build output
/public/
/resources/

# Personal files
/master/

# Netlify
.netlify

# Hugo
/.hugo_build.lock
```

**Important**: Never commit credentials or private data

### Static Files

Place downloadable files in `static/uploads/`:
- Resume/CV PDFs
- Datasets
- Supplementary materials

Accessible at: `https://yoursite.com/uploads/filename.pdf`

---

## Maintenance Checklist

### Regular Updates

- [ ] Update Hugo Blox modules quarterly:
  ```bash
  hugo mod get -u
  ```

- [ ] Review GitHub Actions for deprecation warnings

- [ ] Update Hugo Extended version as needed

- [ ] Check for broken links (use link checker)

### Content Reviews

- [ ] Update CV/resume annually
- [ ] Archive old events
- [ ] Verify publication links (DOIs)
- [ ] Update profile picture if needed

### Security

- [ ] Review public/private content boundaries
- [ ] Ensure no credentials in repo
- [ ] Check gitignore coverage

---

## Quick Reference

### Useful Commands

```bash
# Start local server
hugo server

# Build for production  
hugo --gc --minify

# Update modules
hugo mod get -u

# Clean cache
hugo mod clean

# Check Hugo version
hugo version

# List all content
hugo list all
```

### File Paths Cheat Sheet

| Purpose | Path |
|---------|------|
| **Site title** | `config/_default/hugo.yaml` |
| **Theme color** | `config/_default/params.yaml` |
| **Navigation** | `config/_default/menus.yaml` |
| **Homepage** | `content/_index.md` |
| **Bio** | `content/authors/admin/_index.md` |
| **New publication** | `content/publications/[name]/index.md` |
| **New event** | `content/events/[name]/index.md` |
| **Favicon** | `assets/media/icon.png` |
| **Logo** | `assets/media/logo.png` |
| **Resume PDF** | `static/uploads/resume.pdf` |

---

## Support & Contact

For issues with this specific website:
- Repository Issues: https://github.com/bahmanmdd/bahmanmdd.github.io/issues

For Hugo Blox/Academic theme:
- Docs: https://docs.hugoblox.com
- Community: https://github.com/HugoBlox/hugo-blox-builder/discussions

---

**Version**: 1.0  
**Last Updated**: December 2025  
**Maintainer**: Bahman Madadi

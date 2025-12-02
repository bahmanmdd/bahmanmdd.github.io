# Quick Content Update Guide

**Your Hugo Academic CV Website - Easy Reference**

---

## 📁 Site Architecture Overview

```
content/
├── _index.md                    # Homepage configuration
├── authors/admin/               # Your profile information
│   ├── _index.md               # Bio, contact, interests
│   └── avatar.jpg              # Profile picture
├── publications/                # Research papers
│   ├── _index.md               # Publications page settings
│   └── [publication-folder]/   # Each publication (e.g., j2024-hybrid-dl/)
│       └── index.md            # Publication details
├── events/                      # Talks, conferences, presentations
│   ├── _index.md               # Events page settings
│   └── [event-folder]/         # Each event (e.g., c2024-lion18/)
│       └── index.md            # Event details
├── experience.md                # Work & education timeline
├── skills.md                    # Skills, languages, training
├── supervision/                 # Student supervision
└── courses/                     # Teaching activities

config/_default/
├── hugo.yaml                    # Site title, URL
├── params.yaml                  # Site settings, appearance
├── menus.yaml                   # Navigation menu
└── languages.yaml               # Language settings
```

---

## 🆕 Adding New Content

### Add a New Publication

1. **Create folder** in `content/publications/`:
   ```
   j2025-your-paper-name/
   ```

2. **Create `index.md`** inside the folder:
   ```yaml
   ---
   title: 'Your paper title'
   authors:
     - admin  # You (always 'admin')
     - Co-author Name
   date: '2025-01-01T00:00:00Z'
   publication_types: ['article-journal']  # or 'paper-conference'
   publication: '*Journal Name*, Volume(Issue), Pages'
   featured: true  # Shows on homepage (optional)
   hugoblox:
     ids:
       doi: 10.xxxx/xxxxx
   links:
     - type: pdf
       url: https://doi.org/10.xxxx/xxxxx
     - name: Code
       url: https://github.com/yourrepo
   ---
   
   Optional abstract or description here.
   ```

3. **Naming convention**:
   - Journal: `j2025-short-name`
   - Conference: `c2025-short-name`
   - Thesis: `phd-thesis-2021`

### Add a New Talk/Event

1. **Create folder** in `content/events/`:
   ```
   c2025-conference-name/
   ```

2. **Create `index.md`** inside the folder:
   ```yaml
   ---
   title: 'Presentation title'
   event: 'Conference Name'
   location: City, Country
   summary: 'Brief description'
   date: '2025-06-01T00:00:00Z'
   all_day: true
   authors:
     - admin
   featured: true  # Highlight this event (optional)
   ---
   
   Optional detailed description.
   ```

### Update Your Bio/Profile

Edit `content/authors/admin/_index.md`:
- Personal information (name, bio, contact)
- Research interests
- Education
- Social links (email, LinkedIn, GitHub, etc.)

### Update Experience

Edit `content/experience.md`:
- Add new positions
- Update job details
- Add education entries

### Update Skills

Edit `content/skills.md`:
- Add new skills, tools, languages
- Update proficiency levels

---

## 🚀 Quick Workflow

1. **Edit/Add content** in the `content/` folder
2. **Test locally** (optional):
   ```bash
   hugo server
   ```
   Visit: http://localhost:1313

3. **Commit changes**:
   ```bash
   git add .
   git commit -m "Add new publication XYZ"
   git push
   ```

4. **Wait ~2-5 minutes** for GitHub Pages to rebuild

---

## 🎨 Common Customizations

| What | File | Line/Setting |
|------|------|--------------|
| **Site title** | `config/_default/hugo.yaml` | `title:` |
| **Site color** | `config/_default/params.yaml` | `appearance: color:` |
| **Navigation menu** | `config/_default/menus.yaml` | Add/remove items |
| **Profile picture** | Replace `content/authors/admin/avatar.jpg` | - |
| **Site logo** | `assets/media/logo.png` | Navbar logo |
| **Favicon** | `assets/media/icon.png` | Browser tab icon |

---

## 📝 Front Matter Quick Reference

### Publication Types
- `'article-journal'` - Journal article
- `'paper-conference'` - Conference paper
- `'thesis'` - Thesis/dissertation

### Common Fields
- `featured: true` - Highlights item on homepage
- `date:` - Publication/event date (format: `'YYYY-MM-DDTHH:MM:SSZ'`)
- `authors:` - List of authors (use `admin` for yourself)
- `links:` - Add DOI, PDF, code, dataset links

---

## 🔗 Useful Links

- **Live site**: https://bahmanmdd.github.io
- **Repository**: https://github.com/bahmanmdd/bahmanmdd.github.io
- **Hugo Blox Docs**: https://docs.hugoblox.com

---

## 💡 Tips

- Test locally with `hugo server` before pushing
- Use clear folder names (helps with organization)
- Keep `featured: true` for only your most important work
- Regular commits with clear messages
- Images go in the same folder as `index.md`

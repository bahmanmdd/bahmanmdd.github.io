# SEO Issues Summary & Tasks

## 🛑 Identified Critical Issues

### 1. BaseURL Mismatch
- **Issue**: `config/_default/hugo.yaml` is set to `https://bahmanmdd.github.io/`, but the site is served on `https://bahmanmadadi.com/`.
- **Impact**: Google sees different domains for the same content and may penalize for "duplicate content" or fail to index the custom domain properly due to incorrect canonical tags.

### 2. Broken Archive Redirects
- **Issue**: `disableAliases: true` is set in `hugo.yaml`. 
- **Impact**: Many publications were moved to `publications-archive/`. Without aliases, the old URLs indexed by Google are now **404 Not Found** errors. Google will de-index these pages.

### 3. Sitemap Inconsistencies
- **Issue**: Some generated sitemaps point to `http://localhost:1313` or the GitHub URL.
- **Impact**: Crawlers follow these links and hit dead ends or local development addresses, wasting crawl budget and causing indexing errors.

---

## ✅ Recommended Actions

- [ ] Change `baseURL` to `https://bahmanmadadi.com/` in `hugo.yaml`.
- [ ] Set `disableAliases: false` to restore automatic redirects for moved content.
- [ ] Verify that the `google-site-verification` file or meta tag matches the current Search Console account.
- [ ] Re-submit the updated `sitemap.xml` to Google Search Console once the domain settings are fixed.

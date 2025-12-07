# SEO Guide for bahmanmadadi.com

**Last Updated:** 2025-12-07

## ✅ Completed Setup

### Critical Foundation
- ✅ **baseURL fixed** - Changed from example.com to bahmanmadadi.com
- ✅ **Google Search Console verified** - Verification file added
- ✅ **Sitemap submitted** - Google knows all pages
- ✅ **Homepage meta description** - Optimized for search results
- ✅ **Backlinks added** - LinkedIn, ORCID profiles updated
- ✅ **Indexing requested** - In Google's indexing queue

---

## 🎯 Ongoing SEO Best Practices

### 1. Content Strategy

#### Publications (High Impact)
- ✅ Add new publications as soon as published
- ✅ Include full abstracts
- ✅ Link to DOIs
- ⏳ **TODO:** Add citation counts when available
- ⏳ **TODO:** Add structured data (Schema.org ScholarlyArticle)

**Why it matters:** Academic publications are your strongest SEO asset. Google Scholar integration drives traffic.

#### Talks/Presentations
- ✅ Document all talks/presentations
- ✅ Include titles, dates, locations
- ⏳ **TODO:** Add presentation PDFs/slides when available

#### Regular Updates
- 📅 **Monthly:** Add new publications, talks, or projects
- 📅 **Quarterly:** Review and update research interests
- 📅 **Annually:** Update CV, review all content

### 2. Technical SEO Checklist

#### Every Page Should Have:
```yaml
---
title: "Unique, Descriptive Title"
description: "Compelling 150-160 character summary"
date: YYYY-MM-DD
---
```

#### Image Optimization
- [ ] All images have descriptive filenames (not IMG_1234.jpg)
- [ ] All images have alt text
- [ ] Images are optimized/compressed
- ⏳ **TODO:** Review all publication images for alt text

#### URL Structure (Already Good!)
- ✅ Clean URLs: `/publications/`, `/events/`
- ✅ No special characters or spaces
- ✅ Descriptive slugs

### 3. Link Building Strategy

#### High Priority Backlinks (Do ASAP)
- [x] LinkedIn profile
- [x] ORCID profile  
- [ ] **University staff page** - Contact ENTPE/UGE webmaster
- [ ] **Google Scholar** - Verify website is listed
- [ ] **ResearchGate** - Add website URL
- [ ] **Academia.edu** - If you have an account

#### Medium Priority
- [ ] **Department/Lab page** - Ask LICIT-ECO7 to add your site
- [ ] **Conference proceedings** - Bio sections often allow URLs
- [ ] **Co-author websites** - Link exchange with collaborators
- [ ] **Project websites** - If you lead/participate in funded projects

#### Ongoing
- Every new publication → Google Scholar automatically creates entry
- Every conference talk → Add to website → Potential backlinks
- Collaboration announcements → Link to your site

### 4. Google Search Console Monitoring

#### Weekly Checks (First Month)
1. Go to: https://search.google.com/search-console
2. Check **Coverage** report - Are pages being indexed?
3. Check **Performance** - Any search impressions yet?
4. Test: `site:bahmanmadadi.com` in Google

#### Monthly Checks (Ongoing)
1. **Performance** tab - Which queries bring visitors?
2. **Pages** report - Are all important pages indexed?
3. **Mobile Usability** - Any issues?
4. **Core Web Vitals** - Site speed/performance

#### Fix Issues Immediately:
- "Crawled but not indexed" → Request indexing
- "Page with redirect" → Check if intentional
- "4xx errors" → Fix broken links

### 5. Meta Descriptions Best Practices

**Homepage:** ✅ Done
```
Bahman Madadi - Assistant Professor at Université Gustave Eiffel & ENTPE. 
Research in Graph Neural Networks, Deep Learning, Transport Network Design, 
and Zero-Emission Mobility.
```

**For Each Publication Page:**
```yaml
description: "[Author names]. [Title]. Published in [Journal/Conference]. [Key finding or contribution]."
```

**For Talk/Event Pages:**
```yaml
description: "[Talk title] presented at [Conference/Event] on [Date]. [Brief topic description]."
```

### 6. Social Media Integration

#### Open Graph Tags (For Social Sharing)
Your Hugo theme likely includes these automatically, but verify:
- og:title
- og:description  
- og:image
- og:url

**TODO:** Check if your sharing image (sharing.png) is optimized

#### Twitter Card
If you tweet about your research, ensure Twitter cards work.

### 7. Academic-Specific SEO

#### Google Scholar Optimization
- ✅ Publications with DOIs indexed faster
- ✅ Full text PDFs (when allowed) boost visibility
- ⏳ **TODO:** Claim/verify your Google Scholar profile
- ⏳ **TODO:** Ensure profile links to bahmanmadadi.com

#### Citation Tracking
Monitor citations of your work:
- Google Scholar Alerts
- ORCID notifications
- Web of Science (if access)

Each citation = potential visitor to your site.

### 8. Performance Optimization

#### Page Speed Matters for SEO
- ✅ Hugo generates fast static sites
- ✅ Images processed/optimized
- ⏳ **TODO:** Run Lighthouse audit (Chrome DevTools)
- ⏳ **TODO:** Check mobile performance

**Test Tools:**
- Google PageSpeed Insights: https://pagespeed.web.dev/
- GTmetrix: https://gtmetrix.com/

### 9. Content Freshness

Google favors regularly updated sites:

**High Impact Updates:**
- New publications (major signal)
- New talks/presentations  
- Research project updates

**Medium Impact:**
- Blog posts about research (if you start blogging)
- Updated CV
- New images/media

**Low Impact:**
- Minor text edits
- Footer updates

**Recommendation:** Add something new monthly.

### 10. Analytics Setup

#### Google Analytics (Optional but Recommended)
Add to `config/_default/params.yaml`:
```yaml
marketing:
  google_analytics: "G-XXXXXXXXXX"
```

**Benefits:**
- See visitor numbers
- Understand which content is popular
- Track conversion goals (CV downloads, publication clicks)

**Privacy:** Hugo Blox supports privacy-friendly analytics.

---

## 📊 Success Metrics

### Month 1 (Indexing Phase)
- [ ] All pages indexed in Google (`site:bahmanmadadi.com` shows 50+ results)
- [ ] Appears in search for "Bahman Madadi"
- [ ] Google Scholar profile shows website

### Month 3 (Growth Phase)
- [ ] Appears for research keywords (e.g., "graph neural networks transport")
- [ ] 10+ backlinks (use Google Search Console "Links" report)
- [ ] Regular visitors from Google (check Analytics)

### Month 6 (Established)
- [ ] First page results for "Bahman Madadi"
- [ ] Publications appear in Google Scholar with correct attribution
- [ ] Steady organic traffic growth

---

## 🚨 Common SEO Mistakes to Avoid

1. **Don't change baseURL frequently** - Causes re-indexing delays
2. **Don't use duplicate content** - Each page needs unique text
3. **Don't keyword stuff** - Write naturally
4. **Don't ignore mobile** - Most traffic is mobile
5. **Don't delete old content** - Archives have SEO value
6. **Don't use generic page titles** - "Home" vs "Bahman Madadi - Transport Researcher"

---

## 🔧 Quick Reference Commands

### Check if site is indexed:
```
site:bahmanmadadi.com
```

### Search for specific content:
```
site:bahmanmadadi.com "graph neural networks"
```

### Find backlinks (limited):
```
link:bahmanmadadi.com
```

### Rebuild site locally:
```bash
hugo --minify
```

### Test locally with search:
```bash
npm run dev:search
```

---

## 📅 Maintenance Schedule

### Daily
- Nothing required!

### Weekly (First 2 Months)
- Check Google Search Console Coverage
- Test `site:bahmanmadadi.com` search

### Monthly
- Add new content (publications, talks)
- Check Google Search Console Performance
- Review and respond to any indexing issues

### Quarterly  
- Full site audit with Lighthouse
- Review backlinks report
- Update research interests if changed

### Annually
- Comprehensive content review
- CV update
- Check all external links still work
- Review and update meta descriptions

---

## 🎓 Resources

### Official Documentation
- Google Search Console: https://search.google.com/search-console
- Google Search Central: https://developers.google.com/search
- Hugo SEO: https://gohugo.io/templates/internal/#google-analytics

### Testing Tools
- PageSpeed Insights: https://pagespeed.web.dev/
- Mobile-Friendly Test: https://search.google.com/test/mobile-friendly
- Rich Results Test: https://search.google.com/test/rich-results

### Academic SEO
- Google Scholar Profile: https://scholar.google.com/citations
- ORCID: https://orcid.org/
- Semantic Scholar: https://www.semanticscholar.org/

---

## 🆘 Troubleshooting

### "My site doesn't appear in Google"
1. Check: `site:bahmanmadadi.com` - Is it indexed at all?
2. If NO: Check Google Search Console Coverage report
3. Request indexing for homepage
4. Wait 48 hours and check again

### "I appear for my name but not research topics"
- Normal for new sites (takes 3-6 months)
- Keep adding content
- Build more backlinks from academic sources

### "Some pages aren't indexed"
1. Check robots.txt isn't blocking them
2. Check page has unique content (not duplicate)
3. Request indexing in Google Search Console
4. Check page has proper meta title/description

### "My ranking dropped"
- Check Google Search Console for "Manual Actions"
- Review "Coverage" for new errors
- Verify baseURL hasn't changed
- Check if site is accessible (not down)

---

## 📝 Notes

- SEO is a marathon, not a sprint
- Quality content > SEO tricks
- Academic credibility (citations, publications) is your strongest asset
- Consistency beats intensity - small regular updates win

**Your competitive advantage:** You're a researcher - your publications are unique, authoritative content that Google values highly.

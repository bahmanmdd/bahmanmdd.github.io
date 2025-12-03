# TODO List

## Website Styling & Navigation Tasks

### 1. Fix People Hyperlinks in Supervision Tab
- [ ] **Task**: Update hyperlink styling for people names in the Supervision tab
  - **Description**: Currently, people hyperlinks in the Supervision tab are displayed with underline styling. Need to change them to cyan/bold without underline for consistency with the site's design aesthetic.
  - **Location**: Supervision tab/section
  - **Requirements**: 
    - Remove text-decoration (underline) from people hyperlinks
    - Apply cyan color to hyperlinks
    - Apply bold font-weight
    - Maintain hover states if applicable
  - **Files likely affected**: Custom CSS or Hugo Blox theme overrides
  - **Priority**: High
  - **Status**: Not started

### 2. Fix Continuous Scrolling Issue
- [ ] **Task**: Enable continuous scrolling through all sections
  - **Description**: The website currently stops scrolling after the "Talks" tab, preventing users from accessing content below it. Need to investigate and fix the scrolling mechanism to allow full navigation through all sections.
  - **Requirements**:
    - Debug why scrolling stops after Talks tab
    - Check for CSS overflow or height constraints
    - Verify JavaScript scroll listeners or animations
    - Test scrolling behavior across all sections
  - **Files likely affected**: CSS files, possibly JavaScript/Hugo templates
  - **Priority**: High (affects user experience)
  - **Status**: Not started

### 3. Add Complete Publications Tab
- [ ] **Task**: Create a new tab with complete publication list
  - **Description**: Add a new navigation tab dedicated to displaying a comprehensive list of publications. User will provide the complete publication list.
  - **Requirements**:
    - Create new Hugo section/page for publications
    - Add tab to navigation menu
    - Format publication list appropriately (likely using Hugo Blox publications widget or custom formatting)
    - Ensure consistent styling with other tabs
    - Position in navigation (user preference needed)
  - **Dependencies**: Waiting for complete publication list from user
  - **Files to create/modify**: 
    - New content file in `content/` directory
    - Possibly `config/_default/menus.yaml` for navigation
  - **Priority**: Medium
  - **Status**: Blocked - awaiting publication list

---

## Image Editing Tasks

### 4. Orca Navicon Logo - Combine Neon Style with Filled Background
- [ ] **Task**: Create new orca navicon combining best elements from two versions
  
  - **Description**: 
    Create a professional navicon-style logo that combines the vibrant neon aesthetic from the left version with the filled background/negative space approach from the right version. The goal is a logo similar to GitHub's navicon style (solid background with icon as negative space) but with the attractive neon cyan glow effect.

  - **Reference Images**:
    - Left version (neon outline): `C:/Users/bahma/.gemini/antigravity/brain/4b573e0b-9698-480b-9593-7f3fd9a9ed1b/uploaded_image_0_1764713269876.jpg`
    - Right version (filled background): `C:/Users/bahma/.gemini/antigravity/brain/4b573e0b-9698-480b-9593-7f3fd9a9ed1b/uploaded_image_1_1764713269876.png`

  - **DETAILED REQUIREMENTS - What to Take from Each Version**:
    
    **FROM LEFT VERSION (KEEP THESE ELEMENTS):**
    - ✅ **Color**: Bright/vibrant neon cyan/turquoise color (appears to be around #00FFFF to #00E5E5)
    - ✅ **Glow Effect**: The soft cyan/turquoise glow radiating outward from the lines
    - ✅ **Size**: The larger overall dimensions 
    - ✅ **Line Quality**: The smooth, clean neon line aesthetic
    - ❌ **DO NOT KEEP**: The outline-only style (no filling inside the circle)
    
    **FROM RIGHT VERSION (KEEP THESE ELEMENTS):**
    - ✅ **Filling Strategy**: The entire circular area (space between outer ring and orca body) is FILLED with solid color
    - ✅ **Negative Space Design**: The orca body itself appears as DARK/BLACK (negative space cutout)
    - ✅ **Professional Icon Style**: Matches how major brands create navicons (solid background, icon as negative space)
    - ❌ **DO NOT KEEP**: The less vibrant/duller cyan color, smaller size

  - **STEP-BY-STEP CREATION PROCESS**:
    
    1. **Base Structure**:
       - Start with circular composition like both versions
       - Use the LARGER size from the left version
       - Orca should be positioned similar to both versions (jumping/leaping pose within circle)
    
    2. **Color & Fill Application**:
       - Fill the ENTIRE circular ring area with the vibrant neon cyan from the left version
       - This means: everything INSIDE the outer circle border but OUTSIDE the orca body should be CYAN/FILLED
       - The orca body itself should be DARK/BLACK (negative space - cut out from the filled background)
       - White eye patch on orca should remain WHITE/light
    
    3. **Glow Effect**:
       - Apply the soft neon glow/bloom effect from the left version
       - Glow should radiate from the filled cyan areas
       - Glow intensity should match the left version (soft but visible)
    
    4. **Outline/Border**:
       - Outer circle border can have a neon outline similar to left version
       - Inner edges (where cyan meets the black orca body) should be clean and defined
    
    5. **Background**:
       - Background should be dark/black like both versions
       - This creates contrast with the cyan filled area and makes the orca negative space visible

  - **TECHNICAL SPECIFICATIONS**:
    - **Format**: PNG with transparency (for web use) or ICO (for favicon)
    - **Size**: At least 512x512px minimum (for high-quality favicon generation)
    - **Color Mode**: RGB
    - **Neon Cyan Color**: Approximately #00FFFF, #00E5E5, or similar vibrant cyan
    - **Orca Body Color**: #000000 or very dark (negative space)
    - **Eye Patch**: White/light (#FFFFFF or similar)
    - **Background**: Transparent or black
    - **Glow Effect**: Soft outer glow, radius approximately 20-40px depending on final size

  - **WHAT THE FINAL RESULT SHOULD LOOK LIKE**:
    - Viewed from a distance, you see a vibrant glowing cyan circle
    - The orca shape is clearly visible as a DARK silhouette against the cyan background
    - The neon glow makes it eye-catching and modern
    - At small sizes (16x16, 32x32 favicon), the orca silhouette remains recognizable
    - Style is professional like GitHub's Octocat navicon, but with neon cyan coloring

  - **QUALITY CRITERIA / SUCCESS METRICS**:
    - ✓ Vibrant neon cyan color with visible glow (not dull)
    - ✓ Circular background area is FILLED with cyan (not just outlines)
    - ✓ Orca appears as dark negative space (clearly visible against cyan)
    - ✓ Works well at multiple sizes (512px down to 32px)
    - ✓ Maintains professional icon aesthetic
    - ✓ Eye-catching and moderne (combining neon aesthetic with solid icon design)

  - **Common Mistakes to Avoid**:
    - ❌ Making the orca cyan/outlined instead of dark/filled
    - ❌ Only outlining the circle without filling the background
    - ❌ Using dull cyan instead of vibrant neon cyan
    - ❌ Forgetting the glow effect
    - ❌ Making it too small initially (work large, then scale down)
    - ❌ Changing the size or position of the circle relative to the orca
    - ❌ Making a circle that fully encompasses the orca (the current design intentionally has three ends of the orca body - tail, dorsal fin, and pectoral fin - extending slightly outside the circle boundary, which creates a more dynamic and interesting composition)

  - **Output Files Needed**:
    - High-res version: 512x512px PNG
    - Favicon versions: 32x32px, 16x16px PNG or ICO
    - Optional: SVG version for scalability

  - **Priority**: High
  - **Status**: Not started

---

*Last updated: 2025-12-02 23:03*

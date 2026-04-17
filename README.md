# eCornell Product Management Updates Force redeploy

A collection of quarterly product management update sites built with the Cornell brand system for internal and enterprise use.

## Deployment Instructions (GitHub + Vercel)

### Option A: Deploy Individual Update

Each update folder contains a standalone site that can be deployed independently.

1. **Upload to GitHub:**
   ```bash
   # Create new repository on GitHub (e.g., "ecornell-product-updates")
   
   # Clone locally
   git clone https://github.com/[your-username]/ecornell-product-updates.git
   cd ecornell-product-updates
   
   # Copy the specific update folder
   cp -r /path/to/march-30-2026 ./
   
   # Commit and push
   git add .
   git commit -m "Add March 30, 2026 Product Management Update"
   git push origin main
   ```

2. **Deploy on Vercel:**
   - Go to [vercel.com](https://vercel.com)
   - Click "New Project"
   - Import your GitHub repository
   - **Important:** Set the Root Directory to `march-30-2026` (or whichever update)
   - Leave Framework Preset as "Other"
   - Click Deploy

### Option B: Deploy All Updates (Multi-Site)

If you want all updates accessible from one domain:

1. **Upload entire folder structure:**
   ```bash
   # Same as above, but copy the entire product-management-updates folder
   cp -r product-management-updates/* ./
   ```

2. **Deploy on Vercel:**
   - Import repository (no root directory needed)
   - Each update will be accessible at:
     - `yoursite.vercel.app/march-30-2026`
     - `yoursite.vercel.app/next-update-folder`
     - etc.

### Quick Deploy (Recommended)

For fastest deployment of the March 30 update:

1. **Download the `march-30-2026` folder**
2. **Drag and drop to Vercel:**
   - Go to vercel.com
   - Drag the `march-30-2026` folder directly onto the Vercel dashboard
   - Vercel will auto-deploy it immediately
   - You'll get a live URL in ~30 seconds

## Folder Structure

```
product-management-updates/
├── README.md                    # This file
├── .gitignore                   # Git ignore rules
├── march-30-2026/             # March 30, 2026 Update
│   └── index.html              # Main site file
└── [future-updates]/          # Additional quarterly updates
    └── index.html
```

## Technical Notes

- **Single-file architecture:** Each update is a complete HTML file with embedded CSS and JavaScript
- **Cornell brand compliance:** Uses official Carnelian Red (#B31B1B) and Source Sans Pro/Source Serif Pro typography
- **Mobile responsive:** Tested across devices
- **Interactive features:** Filterable workshop calendar, animated counters, tabbed content
- **No build step required:** Deploy directly to any static host

## Features

- **Workshop Calendar:** Interactive filter/search for 35+ scheduled AI workshops
- **Release Tracking:** Q3 and Q4 release tabs with detailed content updates
- **AI OnDemand Library:** Visual breakdown of 156 lessons across certificates
- **Pricing Guide:** Enterprise-focused pricing structure
- **Cornell Branding:** Consistent with eCornell corporate identity

## Contact

For updates to content or additional quarterly reports, reach out to the eCornell Enterprise Programs team.

---

*Built with Cornell brand guidelines | Optimized for enterprise consumption*

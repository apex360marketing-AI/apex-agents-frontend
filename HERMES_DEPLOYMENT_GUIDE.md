# APEX Agents Frontend — Hermes Deployment Guide

## Quick Deploy to Vercel (3 minutes)

### Prerequisites
- Vercel account + API token
- This repo cloned locally

### Option 1: Using GitHub Actions (Automated)
1. Add `VERCEL_TOKEN` secret to GitHub repo
2. Push to main branch
3. GitHub Actions auto-deploys to Vercel
4. Done ✅

### Option 2: Manual Vercel Deploy
```bash
# Install Vercel CLI
npm install -g vercel

# Deploy
cd apex-agents-frontend
vercel --prod
```

### What Gets Deployed
- 9 premium HTML pages (fully responsive)
- All brand-compliant (purple/pink design)
- Glassmorphism UI effects
- Form validation
- Chart.js visualizations

### Pages Included
1. landing_page_premium.html - Marketing homepage
2. signup_form_premium.html - Lead capture form
3. account_dashboard_premium.html - User dashboard
4. batch_import.html - CSV import tool
5. custom_fields.html - Field builder
6. scoring_breakdown.html - Score transparency
7. email_tracking_dashboard.html - Email analytics
8. slack_integration.html - Slack alerts config
9. roi_calculator_premium.html - ROI calculator

### IMPORTANT: Update API URL
Before deploying, update this line in ALL HTML files:
```javascript
window.APEX_API_URL = 'http://localhost:8000';
```

Replace with your Railway backend URL:
```javascript
window.APEX_API_URL = 'https://your-railway-url.railway.app';
```

### Deploy Command
```bash
vercel --prod --token YOUR_VERCEL_TOKEN
```

### Expected Output
```
✓ Production deployment complete [URL]
```

### Test Deployment
1. Open your Vercel URL in browser
2. Click "Start Free Trial"
3. Submit signup form
4. Should see success message

### Success Criteria
- ✅ Frontend deployed to Vercel
- ✅ Pages load in < 2 seconds
- ✅ All links work
- ✅ Forms submit to backend
- ✅ Backend receives requests

---

**Important:** Update the API URL in HTML files BEFORE deploying!

---

**Questions?** Check the main README.md or contact the team.

# Legal Subdomain Redirects

This project handles redirects for `legal.theambassadorplatform.com` using Vercel.

## Files

- `vercel.json` - Contains all redirect rules (301 permanent redirects)
- `index.html` - Fallback page (not normally seen due to redirects)
- `package.json` - Project metadata

## Deployment Instructions

### Option 1: Vercel CLI (Recommended)

1. Install Vercel CLI:
   ```bash
   npm i -g vercel
   ```

2. Navigate to this directory and deploy:
   ```bash
   cd legal-redirects
   vercel
   ```

3. Follow the prompts to deploy

4. Add custom domain `legal.theambassadorplatform.com` in Vercel dashboard

5. Update Route 53 CNAME record to point to Vercel's target

### Option 2: GitHub + Vercel Dashboard

1. Create a GitHub repository
2. Upload these files to the repo
3. In Vercel dashboard, click "Import Project"
4. Connect your GitHub repo
5. Deploy
6. Add custom domain in Vercel settings

## Testing

After deployment, test with:

```bash
curl -I https://your-project.vercel.app/user-terms
```

Should return 301 redirect to IDP portal.

## All Redirect URLs

- /admin-user-terms → P2P-User-Terms
- /mobile-application-terms → P2P-User-Terms
- /user-terms → P2P-User-Terms
- /customer-terms → global-clients-terms-conditions
- /ip-assignment → P2P-IP-Assignment-Terms
- /cookie-policy → theambassadorplatform.com/cookie-policy
- /privacy-notice → P2P-Privacy-Notice
- /general-privacy-policy → theambassadorplatform.com/privacy-policy
- /accessibility-statement → theambassadorplatform.com/accessibility-statement
- /safeguarding-policy → Safeguarding-Policy
- /acceptable-usage-policy → Acceptable-Usage-Policy
- /osa → Safeguarding-Policy
- /service-level-agreement → P2P-SLA
- /modern-slavery-policy → IDP_Modern_Slavery_Statement_2025.pdf

All other paths redirect to www.theambassadorplatform.com (302 temporary)

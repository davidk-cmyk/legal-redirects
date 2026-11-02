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

All named paths are 301 permanent redirects to TAP legal pages on `partners.idp.com`.

- /user-terms → /tap-terms/p2p-user-terms
- /ip-assignment → /tap-terms/p2p-ip-assignment-terms
- /privacy-notice → /tap-terms/p2p-privacy-notice
- /safeguarding-policy → /tap-terms/p2p-safeguarding-policy
- /service-level-agreement → /tap-terms/p2p-sla
- /acceptable-usage-policy → /tap-terms/acceptable-usage-policy
- /accessibility-statement → /tap-terms/accessibility-statement
- /admin-user-terms → /tap-terms/admin-user-terms
- /cookie-policy → /tap-terms/cookie-policy
- /customer-service-support → /tap-terms/customer-service-support
- /customer-terms → /tap-terms/customer-terms
- /general-privacy-policy → /tap-terms/general-privacy-policy
- /mobile-application-terms → /tap-terms/mobile-application-terms
- /modern-slavery-policy → /tap-terms/modern-slavery-policy
- /osa and /online-safety-act → /tap-terms/online-safety-act
- /service-specification-and-plans and /service/service-specification → /tap-terms/service-specification-and-plans
- /terms/customer-terms → /tap-terms/customer-terms
- /service/service-level-agreement → /tap-terms/p2p-sla
- /terms/mobile-terms → /tap-terms/mobile-application-terms
- /service/acceptable-usage-policy → /tap-terms/acceptable-usage-policy
- /privacy/privacy-notice → /tap-terms/p2p-privacy-notice
- /cookies/cookie-policy → /tap-terms/cookie-policy

All other paths redirect to www.theambassadorplatform.com (302 temporary)

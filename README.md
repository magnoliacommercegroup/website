# Magnolia Commerce Group — Website

Static site for [magnoliacommercegroup.com](https://magnoliacommercegroup.com), hosted via GitHub Pages.

---

## File Structure

```
index.html          Home page
about.html          About / Our Brands
contact.html        Contact
CNAME               Custom domain configuration
assets/
  style.css         All styles
  logo.png          Place logo file here (not included in repo)
```

---

## Deployment Steps

### Step 1 — Add the logo

Place your `logo.png` file in the `assets/` folder before pushing.

### Step 2 — Enable GitHub Pages

1. Go to the repo on GitHub: `github.com/magnoliacommercegroup/website`
2. Settings → Pages
3. Source: **Deploy from a branch**
4. Branch: `main` / `/ (root)`
5. Save

### Step 3 — Connect the custom domain

In GitHub Pages settings, enter the custom domain: `magnoliacommercegroup.com`

Then add these DNS records at your domain registrar:

| Type  | Name | Value                              |
|-------|------|------------------------------------|
| A     | @    | 185.199.108.153                    |
| A     | @    | 185.199.109.153                    |
| A     | @    | 185.199.110.153                    |
| A     | @    | 185.199.111.153                    |
| CNAME | www  | magnoliacommercegroup.github.io    |

Once DNS propagates (up to 24 hours), check **Enforce HTTPS** in GitHub Pages settings.

### Step 4 — Set up email routing

Route `inquiries@magnoliacommercegroup.com` to your Gmail using Cloudflare Email Routing or ImprovMX:

1. Log into Cloudflare (or ImprovMX) and add your domain
2. Create a routing rule: `inquiries@magnoliacommercegroup.com` → your Gmail address
3. Add the MX records they provide to your domain registrar

### Step 5 — Send mail as your business address from Gmail

1. Gmail → Settings → Accounts → "Send mail as" → Add another address
2. Name: `Magnolia Commerce Group` | Email: `inquiries@magnoliacommercegroup.com`
3. Use Gmail SMTP to verify
4. Once verified, select this address when composing replies to wholesale inquiries

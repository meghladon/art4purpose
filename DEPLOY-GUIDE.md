# ARTGIVES — Netlify Deploy Guide

## Deploy in 3 minutes

### Step 1: Create a Netlify account
Go to **https://app.netlify.com/signup** and sign up (free tier is all you need).

### Step 2: Deploy
- Go to **https://app.netlify.com/drop**
- Drag the entire `artgives-deploy` folder onto the page
- Wait ~10 seconds — you'll get a live URL like `random-name-12345.netlify.app`

### Step 3: Set a custom site name
- In Netlify dashboard → **Site configuration → Change site name**
- Set it to something like `artgives` → your site becomes `artgives.netlify.app`

### Step 4: (Optional) Connect a custom domain
- In Netlify dashboard → **Domain management → Add custom domain**
- Follow the DNS instructions to point your domain to Netlify

---

## How forms work

This site has **two Netlify Forms** built in:

### 1. Artwork Submission (`artwork-submission`)
Captures: artwork title, medium, description, price, dimensions, artist name, artist email, artist bio, selected charity.

### 2. Purchase Enquiry (`purchase-enquiry`)
Captures: buyer name, buyer email, message, plus the artwork title/artist/price they're enquiring about.

**To see submissions:**
- Netlify dashboard → **Forms** tab
- All submissions appear here in real time
- You get 100 free form submissions/month on the free tier

### Set up email notifications
- Netlify dashboard → **Forms → Form notifications → Add notification**
- Choose **Email notification**
- Set your email address
- You'll get an email every time an artist submits work or a buyer enquires

### (Optional) Connect to Zapier/Make
- Netlify integrates with Zapier and Make
- You can auto-forward submissions to Google Sheets, Slack, Airtable, etc.

---

## What's included

| Page | Description |
|------|-------------|
| **Home** | Landing page with hero, how-it-works, charity partners, CTA |
| **Gallery** | Filterable gallery of all artwork (painting, photography, etc.) |
| **Submit** | Full artist upload form with image preview, charity selector |
| **Detail** | Individual artwork page with "Enquire to Purchase" |
| **About** | Manifesto, values, Acknowledgement of Country |
| **Causes** | Detailed charity partner information |

---

## Notes

- **Image uploads**: In this prototype, uploaded images display in the local session but aren't persisted on refresh (no backend storage). Form submissions capture all text data in Netlify. For image persistence, you'd need to add Netlify Large Media or a service like Cloudinary.
- **Gallery data**: The 9 seed artworks use generative art placeholders. New submissions appear in the gallery during the session.
- **Spam protection**: Built-in honeypot field (`bot-field`) blocks basic bots. You can add reCAPTCHA in Netlify settings for extra protection.

---

## Next steps (when you're ready)

1. **Image storage**: Add Cloudinary or Netlify Large Media for persistent artwork images
2. **CMS**: Add Netlify CMS (free) for a content management dashboard
3. **Payments**: Integrate Stripe Connect when you're ready for real transactions
4. **Custom domain**: Connect artgives.org or similar
5. **Analytics**: Add Plausible or Fathom (privacy-respecting) analytics

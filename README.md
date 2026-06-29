# AllWeHaveIsNow

The official website for AllWeHaveIsNow — a space for intentional work, membership, and chemistry calls.

## Site Features

- **Request Access Form** — Formspree integration for capturing inquiries
- **Calendly Integration** — Inline 20-minute chemistry call booking with name/email prefill
- **Responsive Design** — Mobile-first, optimized for all devices
- **HTTPS & CDN** — Deployed on Vercel with automatic SSL

## Deployment

This site is deployed on Vercel and connected to the custom domain `allwehaveisnow.online`.

### DNS Configuration (GoDaddy)

Add the following records to your GoDaddy DNS:

**For root domain (allwehaveisnow.online):**
- Type: A
- Name: @
- Value: 76.76.19.89

**For www subdomain:**
- Type: CNAME
- Name: www
- Value: cname.vercel-dns.com

### Email Forwarding (ImprovMX)

Set up email forwarding so that `info@allwehaveisnow.online` forwards to `allwehaveisnow.online@gmail.com`:

1. Go to https://improvmx.com
2. Add domain: `allwehaveisnow.online`
3. Add MX records to GoDaddy:
   - Priority 10: `mx1.improvmx.com`
   - Priority 20: `mx2.improvmx.com`
4. In ImprovMX dashboard, forward `info@allwehaveisnow.online` → `allwehaveisnow.online@gmail.com`
5. (Optional) Add SPF record for better deliverability:
   - Type: TXT
   - Name: @
   - Value: `v=spf1 include:improvmx.com ~all`

### Formspree

Form submissions are sent to: `https://formspree.io/f/xbdvdlgr`

Submissions forward to your Formspree-linked email.

### Calendly

Booking link: `https://calendly.com/allwehaveisnow-online/get2know`

The inline widget is embedded and prefilled with visitor name/email after form submission.

## Local Development

```bash
git clone https://github.com/allwehaveisnowonline/allwehaveisnow.git
cd allwehaveisnow
# Open index.html in a browser or serve with:
python3 -m http.server 8000
```

## Next Steps

1. **Add DNS A + CNAME records to GoDaddy** (see above)
2. **Add MX records to GoDaddy for ImprovMX** (see above)
3. **Set up ImprovMX forwarding** from `info@allwehaveisnow.online` → `allwehaveisnow.online@gmail.com`
4. **Test the form and Calendly booking flow** once DNS propagates (24-48 hours)

## Support

For issues or updates, contact: allwehaveisnow.online@gmail.com

# Vyxma

Company site for **https://vyxma.com**. Hosted from this repo on GitHub Pages. SailPrep stays on https://sailprep.vyxma.com (SailPrep repo `docs/`) — do not point the apex at that site.

GitHub Pages is already built with custom domain `vyxma.com`. Apex DNS still belongs to GoDaddy Website Builder until the steps below.

## Cut apex over to GitHub Pages (GoDaddy)

Website Builder owns the `@` A records (`76.223.105.230`, `13.248.243.5`) and will overwrite them unless you disconnect it first.

### 1. Disconnect Website Builder

1. Sign in: https://account.godaddy.com/products
2. Under **Websites** (Website Builder / Airo), open the **VYXMA** site for `vyxma.com`
3. Settings (gear) → **Disconnect domain** (or Unpublish / cancel Website Builder for this domain)
4. Confirm. Do not buy replacement hosting or SSL.

### 2. Replace apex A records

Open DNS: https://dcc.godaddy.com/control/dnsmanagement?domainName=vyxma.com

1. Delete the `@` **A** records `76.223.105.230` and `13.248.243.5`
2. Add four `@` **A** records (TTL 600 is fine):

   - `185.199.108.153`
   - `185.199.109.153`
   - `185.199.110.153`
   - `185.199.111.153`

3. Keep **www** as CNAME to `vyxma.com`
4. Do **not** change **sailprep** CNAME `monikazibolyte.github.io`

### 3. After DNS updates (often minutes, up to the 1-hour TTL)

1. https://vyxma.com should show “Practical knowledge that stays with you”
2. In this repo: Settings → Pages → tick **Enforce HTTPS** when it unlocks  
   https://github.com/monikazibolyte/vyxma/settings/pages
3. Click the FormSubmit **Activate Form** email at `mbuilds45@gmail.com` so Get in touch can deliver mail

## Contact form

Same fields as the GoDaddy builder form: name, email (required), message, mailing-list opt-in, Send. Submissions go through https://formsubmit.co/mbuilds45@gmail.com (the builder endpoint cannot be reused off Website Builder).

# Vyxma

Company site for **https://vyxma.com**. SailPrep stays on https://sailprep.vyxma.com and is a separate GitHub Pages site — do not point this domain at the SailPrep repo.

## Apex DNS (GoDaddy)

`vyxma.com` currently uses GoDaddy Website Builder A records. To serve this repo instead:

1. In GoDaddy, disconnect Website Builder from the domain (or stop it overwriting DNS)
2. Apex `A` records for `@`:

   - `185.199.108.153`
   - `185.199.109.153`
   - `185.199.110.153`
   - `185.199.111.153`

3. Keep `www` as CNAME to `vyxma.com`
4. Do not change the `sailprep` CNAME
5. In this repo’s Pages settings, custom domain is `vyxma.com` (see `CNAME`)

The contact form uses the same fields as the GoDaddy builder form (name, email, message, mailing-list opt-in) and emails `mbuilds45@gmail.com`.

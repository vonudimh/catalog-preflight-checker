# Catalog Preflight

A browser-local Shopify product CSV review tool. It checks a selected CSV before you import it; it does not upload, modify, or send the CSV anywhere.

**Live checker:** https://catalog-preflight.pages.dev/shopify-csv-preflight-checker.html  
**Free synthetic variant test pack:** https://whop.com/checkout/plan_goCApUpt2Atpp  
**Implementation kit:** https://whop.com/checkout/plan_I6EEIVzOSyqqq

## What it reviews

- blank or repeated handles
- duplicate variant option combinations under the same handle
- repeated product-start rows
- non-public image URLs
- blank image alt text rows
- blank fields in an update import that may overwrite existing data

Warnings are prompts to review the source file, not import instructions or guarantees. Test a copy of your data in Shopify before relying on a bulk import.

## Use locally

Download `shopify-csv-preflight-checker.html`, open it in a modern browser, then select a Shopify CSV. The supplied CSV is synthetic and exists only to exercise the review logic.

## Why these checks exist

Shopify documents product CSV imports, variant field dependencies, and overwrite behavior in its current guidance:

- https://help.shopify.com/en/manual/products/import-export/using-csv
- https://help.shopify.com/en/manual/products/import-export/import-products

A community report also documents variants disappearing after CSV imports where option combinations were repeated or incomplete:

- https://community.shopify.com/t/csv-product-import-deleted-variants-shopify-you-got-some-explaining-to-do/582717/14

## License

MIT. The paid implementation kit is a separate optional download containing workflow materials; this repository is the functional free checker.


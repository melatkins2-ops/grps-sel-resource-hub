# GRPS SEL Resource Hub

Practical social and emotional learning ideas and support for the moments that matter in a scholar's day, for educators, scholars, families, and adults, organized around belonging, regulation, attendance, relationships, and family partnership.

**Live site:** https://melatkins2-ops.github.io/grps-sel-resource-hub/

## What's here

- `index.html`: the site (Find a Resource, Educators, MTSS, Scholars, Families, Schoolwide SEL, Adult SEL, About)
- `v19_resource_catalog.csv`: resource catalog
- `v20_audience_mapping.csv`, `audience_coverage.csv`: which resources serve which audiences
- `v16_resource_maintenance_register.csv`, `v16_content_owner_handoff.txt`: who maintains what
- `external_link_audit.csv`, `v18_external_link_inventory.csv`: external link checks
- `QA_REPORT.md`, `v18_functionality_qa.csv`, `v19_review_notes.txt`, `changes.csv`: QA and change history

## Good to know

- Recheck external links when updating resources; the link inventories list every outside link.

## Updating the site

Edit the files on a branch and open a pull request. GitHub Pages publishes `main` automatically, usually within a minute or two of a merge.

## Automated site check

Every pull request and every push to `main` runs **Site check** (`.github/workflows/site-check.yml`). It opens the site in a headless browser at desktop (1366px) and phone (390px) widths and fails if the page throws a JavaScript error, a local file or image is missing, or the page scrolls sideways. See the Actions tab for results.

Maintained by GRPS Community & Student Affairs.

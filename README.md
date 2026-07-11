# MAP Vault (page only)

Static front-end for MAP Accounting's internal credential + client-info vault.

**No data lives here.** This repo contains only `index.html`. All records load at
runtime from a private Google Sheet (accounts@) via an Apps Script web app, and
every request must carry a valid per-user access code. Access codes are never in
this repo; secret fields are masked and only fetched one at a time through an
audited `reveal` call. Revoke a user by disabling their code in the sheet Config tab.

Backend + sync tooling: `~/Documents/map_vault/` (not committed).

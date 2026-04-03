# springerbrands.com Redirect

This repository hosts a minimal redirect site that sends all visitors from `springerbrands.com` to [`brands.springerbrands.com`](https://brands.springerbrands.com/).

## How It Works

The `index.html` uses both an HTTP `meta refresh` tag and a JavaScript `window.location.replace()` call to immediately redirect all visitors to `https://brands.springerbrands.com/`.

## Hosting

This site is served via **GitHub Pages** from the `main` branch.

## DNS Configuration Required

To make `springerbrands.com` resolve to this GitHub Pages site, the following DNS records must be set at your domain registrar:

| Type  | Host              | Value                   | TTL  |
|-------|-------------------|-------------------------|------|
| A     | @                 | 185.199.108.153         | 3600 |
| A     | @                 | 185.199.109.153         | 3600 |
| A     | @                 | 185.199.110.153         | 3600 |
| A     | @                 | 185.199.111.153         | 3600 |
| CNAME | www               | springerbrands.github.io | 3600 |

These are the standard GitHub Pages IP addresses. After adding them, GitHub Pages will serve this redirect site at `springerbrands.com`.

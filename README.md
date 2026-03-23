# Visual Attack Surface Mapper

An interactive, browser-based visualization tool for exploring a domain's attack surface. Built with D3.js, it maps the key security components of a web domain and highlights associated attack vectors.

**Live demo:** [asm.dsoni.in](https://asm.dsoni.in)

## What it shows

Starting from a root domain, the graph expands outward through:

- **DNS** — A/AAAA, MX, NS, TXT, CNAME records
- **Email** — SPF, DKIM, DMARC, SMTP misconfigurations
- **WAF / CDN** — Origin IP exposure, reverse proxy, HTTP headers
- **Subdomains** — API endpoints, dev/staging, admin panels
- **TLS / SSL** — Certificate Transparency logs, cert validity
- **Hosting** — Cloud storage buckets, open ports

Each node lists associated attack vectors rated **Critical**, **High**, or **Medium**.

## Usage

Open `index.html` in any modern browser — no build step or server required.

| Action | Effect |
|---|---|
| Click a node | Expand its children / show attack vectors |
| Click expanded node | Collapse descendants |
| `⌂` button | Reset zoom |
| `⊕` button | Expand all nodes |
| `⊖` button | Collapse all nodes |
| Scroll | Zoom in/out |
| Drag node | Reposition |


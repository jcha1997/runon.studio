# runon.studio

Landing site for **run on studio.** — marketing + social media + UGC content creation + strategy.

A single static page served by GitHub Pages on the custom domain
[runon.studio](https://runon.studio), showing the brand graphic on a matching
paper background (`#F4EFE7`).

## Structure

```
.
├── index.html              # landing page
├── CNAME                   # custom domain for GitHub Pages
├── assets/
│   └── run-on-studio.jpg   # brand graphic
└── README.md
```

## Local preview

Open `index.html` directly, or serve the folder:

```sh
python3 -m http.server
# then visit http://localhost:8000
```

## Deployment

Hosted with **GitHub Pages** from the `main` branch (root). Pushing to `main`
publishes the site.

### Enable GitHub Pages (one-time)

Repo **Settings → Pages → Build and deployment**: set source to *Deploy from a
branch*, branch `main`, folder `/ (root)`. The `CNAME` file sets the custom
domain to `runon.studio`; leave **Enforce HTTPS** on once the certificate is
issued.

### DNS (at the runon.studio registrar)

Apex domain — four `A` records:

```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

(Optional IPv6 — four `AAAA` records: `2606:50c0:8000::153`,
`2606:50c0:8001::153`, `2606:50c0:8002::153`, `2606:50c0:8003::153`.)

`www` subdomain — one `CNAME` record pointing to `jcha1997.github.io`.

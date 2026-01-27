# LYN Site Planning Tool

Site qualification tool for bitcoin-heated saunas.

## Concept

Bitcoin mining hardware generates heat as a byproduct.
Same electricity — used twice. Heat for the space, bitcoin for the treasury.

This tool helps potential buyers understand if a LYN sauna
fits their site and whether thermal integration (M4) makes sense.

Two audiences:
- **Private**: personal residence, single unit
- **Professional**: developer, architect, operator

## The Sauna

One sauna. 7 modules. 2,100 sites. Ever.

| Module | Description |
|--------|-------------|
| M1 | sauna — the core |
| M2 | swimming bridge — water access |
| M3 | changing room — transitional space |
| M4 | thermal module — bitcoin mining as heat source |
| M5 | outdoor shower |
| M6 | storage |
| M7 | cold plunge |

Design by Morten Bo Jensen. Manufacture by Koerner.

## Deploy

Static HTML. No build step.

1. Fork this repo
2. Connect to Netlify (or any static host)
3. Deploy

Form submissions go to Netlify Forms by default.
To use a different endpoint, edit the `CONFIG.formEndpoint` in `index.html`.

## Customize

**Prices**: Edit the `CONFIG.prices` object at top of `index.html`

```javascript
const CONFIG = {
    prices: {
        m1: 55555,
        m2: 11125,
        m3: 15000,
        m4: 3000,
        m5: 3625,
        m6: 2438,
        m7: 12250
    },
    deliveryInstall: 4700,
    currency: '€',
    formEndpoint: null // Set to override Netlify Forms
};
```

**Images**: Replace files in `/images`

**Copy**: Edit directly in HTML

## Structure

```
lyn-site-planning-tool/
├── index.html          # the tool (single file, no dependencies)
├── images/
│   ├── hero.png        # hero image
│   ├── m1-sauna.png    # module images
│   ├── m2-bridge.png
│   ├── m3-changing.png
│   ├── m4-thermal.png
│   ├── m5-shower.png
│   ├── m6-storage.png
│   ├── m7-plunge.png
│   └── config-preview.png
├── README.md
└── LICENSE
```

## License

MIT

## Links

- [lynbitcoin.com](https://lynbitcoin.com)

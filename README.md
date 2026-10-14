# FlexDB

Personal exercise GIF + JSON API for **FlexDex**.

Hosted on GitHub and served via **jsDelivr** (no backend required).

- **Repo:** https://github.com/varad615/flexdb
- **CDN base:** `https://cdn.jsdelivr.net/gh/varad615/flexdb@main`
- **Exercises:** 1,323 · **Languages:** `en`, `es`

> Based on [ExerciseGymGifsDB](https://github.com/JahelCuadrado/ExerciseGymGifsDB). GIFs belong to their respective authors — see original disclaimer.

---

## Quick start

```js
const BASE = "https://cdn.jsdelivr.net/gh/varad615/flexdb@main";
const LANG = "en";

const all = await fetch(`${BASE}/api/${LANG}/exercises.json`).then((r) => r.json());
const biceps = await fetch(`${BASE}/api/${LANG}/muscles/biceps.json`).then((r) => r.json());

// <img src={all.exercises[0].gifUrl} />
```

## Endpoints

Replace `{lang}` with `en` or `es`.

| Endpoint | Description |
| --- | --- |
| `/api/index.json` | Global metadata |
| `/api/{lang}/exercises.json` | All exercises |
| `/api/{lang}/muscles.json` | Muscle groups |
| `/api/{lang}/muscles/{muscle}.json` | Exercises by muscle |
| `/api/{lang}/equipment.json` | Equipment list |
| `/api/{lang}/equipment/{name}.json` | By equipment |
| `/api/{lang}/bodyparts.json` | Body parts |
| `/api/{lang}/categories.json` | Categories |

Live examples:

- https://cdn.jsdelivr.net/gh/varad615/flexdb@main/api/index.json
- https://cdn.jsdelivr.net/gh/varad615/flexdb@main/api/en/exercises.json
- https://cdn.jsdelivr.net/gh/varad615/flexdb@main/biceps/barbell-curl.gif

## Regenerate API

```bash
export API_BASE_URL="https://cdn.jsdelivr.net/gh/varad615/flexdb@main"
npm run build
```

## Disclaimer

Exercise media was collected from the internet. This repo does not claim copyright over the GIFs and cannot grant rights to third parties.

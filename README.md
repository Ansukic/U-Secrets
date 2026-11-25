# Secrets of the Universidad Nacional de Colombia

A single-page website, written in English and built with React, that turns the podcast *“Beyond the Campus: Stories of the National University of Colombia”* into an interactive page. The visual design follows the look of the university’s official website (navy buttons, three-color title rule, card layout and a banner photo of the campus).

## What’s inside

The page has four tabs:

| Tab | Content |
| --- | --- |
| **University City** | How the Ciudad Universitaria was born (Law 68 of 1935, Fritz Karsen and Leopoldo Rother), the “White City” and its 17 national monuments, the open-campus vs. safety debate, and the owl-shaped campus plan. |
| **Rogelio Salmona** | The paradox of the architect: Le Corbusier’s translator in 1947, his years in Paris, his degree from the Universidad de los Andes, and the building and honorary doctorate the Universidad Nacional gave him in 2000. |
| **The Pool Myth** | Why the Bogotá campus never had a swimming pool: it was planned in 1937 but never built. |
| **References** | The sources used in the podcast. |

## Tech stack

- **React 18**, loaded from [cdnjs](https://cdnjs.com/) as UMD builds (no JSX, uses `React.createElement`)
- Plain **HTML + CSS**, light theme only, responsive
- **No build step** and no dependencies to install
- Images (banner photo and logo) are embedded in the file as base64, so the whole site is one file

## Project structure

```
.
├── index.html   # the whole site: markup, styles, React code and images
└── README.md
```

> If your file is named `unal-secrets.html`, rename it to `index.html`.

## Run it locally

Open `index.html` in any modern browser. An internet connection is needed the first time to load React from the CDN.

Or serve it with a local server:

```bash
npx serve .
```

## Deploy to Vercel

**With the CLI**

```bash
npm i -g vercel
vercel          # first deploy (choose "Other" if asked for a framework)
vercel --prod   # publish to production
```

**With GitHub**

1. Push this folder to a GitHub repository.
2. In [vercel.com](https://vercel.com), choose **Add New → Project** and import the repository.
3. Leave the framework preset as **Other**, with no build command, and click **Deploy**.

## Customize

- **Text and sections:** edit the `Campus`, `Salmona`, `Pool` and `Refs` functions in the `<script>` block.
- **Colors:** change the CSS variables at the top of the `<style>` block (`--navy`, `--teal`, `--lime`, `--steel`).
- **Banner image:** replace the `url("data:image/jpeg;base64,...")` in the `.hero` rule, or point it to a file such as `url("hero.jpg")`.
- **Logo:** the `<img>` inside the header uses an embedded PNG (white logo on transparent background).

## Credits

- **Podcast content:** Topic 1 by Johel and Alejandro, Topic 2 by Johana and Sergio, Topic 3 by Camilo.
- **Sources:**
  - Wikipedia (es): Rogelio Salmona.
  - Fundación Rogelio Salmona. *Biografía*. https://www.fundacionrogeliosalmona.org/biografia
  - Albornoz Rugeles, C. (2019). *Rogelio Salmona: Un arquitecto frente a la historia*. Universidad de los Andes.
  - BibloRed (2021). *Rogelio Salmona: El transformador de ciudades*. https://www.biblored.gov.co/noticias/efemerides-rogelio-salmona-arquitectura

## Notes

This is an academic project. The Universidad Nacional de Colombia name, logo and campus photographs belong to their respective owners and are used here for educational purposes only.

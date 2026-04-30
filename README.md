# My Recipe Book

A personal recipe manager — single `index.html` file, no dependencies, works offline.  
Open it by double-clicking the file, or host it on GitHub Pages with zero config.

---

## Using locally

Double-click `index.html`. That's it.  
No server, no build step, no internet connection required (fonts load from Google Fonts CDN on first open).

---

## Deploy to GitHub Pages

1. **Fork this repo** — click *Fork* at the top-right of the GitHub page.
2. In your fork, go to **Settings → Pages**.
3. Under *Source*, select **Deploy from a branch → main → / (root)** and click *Save*.
4. GitHub Pages will publish your site at `https://<your-username>.github.io/<repo-name>/` within a minute or two.

---

## Adding your own recipes

All recipe data lives in a single JavaScript array near the top of `index.html`.  
Open the file in any text editor, find the comment block that reads:

```
// RECIPE DATA
// ── Edit this array to add or modify recipes.
```

Each recipe follows this structure — copy a block and fill it in:

```javascript
{
  id: 99,                        // unique number — just increment from the last one
  name: "Recipe Name",
  category: "breakfast",         // breakfast | lunch | dinner | desserts
  prepTime: "20 min",
  difficulty: "Easy",            // Easy | Medium | Hard
  description: "One-line teaser shown on the card.",
  ingredients: [
    "200 g ingredient one",
    "1 tbsp ingredient two",
    "salt and pepper"
  ],
  instructions: [
    "Step one — what to do first.",
    "Step two — what to do next.",
    "Step three — serve and enjoy."
  ]
},
```

Save the file and refresh the browser — changes appear instantly.

---

## Features

- **62 recipes** across Breakfast, Lunch, Dinner, and Desserts
- Real-time search by name or ingredient
- Category tabs for quick filtering
- Click any card to open the full recipe in a modal
- Close modal by clicking outside it or pressing `Escape`
- Fully responsive — works on phone, tablet, and desktop
- No frameworks, no build tools, no dependencies

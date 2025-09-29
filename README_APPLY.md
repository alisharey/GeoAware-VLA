# Light Theme Patch Pack for `academic-project-page-template-vue`

This pack gives you a **light color** look & ready-to-fill sections for your paper site.

## How to apply

1. **Create your site repo from template**  
   Use GitHub’s **Use this template** on: `JunyaoHu/academic-project-page-template-vue`.

2. **Set Vite base (very important for GitHub Pages)**  
   In your repo’s `vite.config.js`, set:
   - If your repo is `yourname.github.io`: `base: '/'`
   - If your repo is `yourname/geoaware-vla`: `base: '/geoaware-vla'`

3. **Copy these files into your repo** (merge/overwrite when asked):
   ```
   src/styles/theme-light.css      -> src/styles/theme-light.css
   src/main-light.ts               -> src/main-light.ts (optional entry that imports the light theme)
   src/components/sections/Title.vue      -> src/components/sections/Title.vue
   src/components/sections/Resources.vue  -> src/components/sections/Resources.vue
   public/og.png                   -> public/og.png
   public/favicon.svg              -> public/favicon.svg
   vite.config.example.js          -> (for reference only)
   ```

4. **Import the light theme**  
   In your `src/main.ts` (or `main.js`), add:
   ```ts
   import './styles/theme-light.css'
   ```
   If there is no `styles` folder yet, just create it and place `theme-light.css` inside.

5. **Edit the content in `Title.vue` and `Resources.vue`**  
   Replace placeholders for authors, code/demo links, and affiliations.

6. **Build & Publish**
   - `npm i`
   - `npm run dev` (preview locally)
   - Commit, push to `main`. The template’s **GitHub Action** will build `gh-pages` and publish.  
     Make sure your Pages source is set to `gh-pages` (Settings → Pages → Branch: `gh-pages`).

## Notes
- If your site path is wrong (assets 404), re-check `base` in `vite.config.js`.
- To switch back to dark mode later, just remove the `theme-light.css` import.
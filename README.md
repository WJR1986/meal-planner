# The Good Week

A responsive, static meal planner for one, built around the agreed five-day plan. No build step, package installation, API key or account is needed to run the website.

## Preview it

Extract this ZIP, then open `index.html` in a modern browser. All the website's styles, recipe data and JavaScript are included in that file. No external fonts, scripts, images or network requests are required to display it. Browser storage and clipboard support can vary when opening local files; hosting on GitHub Pages gives a consistent HTTPS address.

## Put it on GitHub Pages

1. Create a GitHub repository, or open the repository you want to use.
2. Upload `index.html` to the repository's top level. You may also upload `.nojekyll`, `README.md`, and `data.json`. **Extract the ZIP first; uploading the ZIP alone will not create the website.** `index.html` must not be left inside an extra folder.
3. Open the repository's **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select the branch containing your files (usually `main`) and the **/(root)** folder. Save.
6. GitHub will display the published website address in Pages settings when deployment finishes.

GitHub Pages availability depends on your account and repository visibility. A public repository is the straightforward option on GitHub Free. This package is ready to upload; no repository has been created and the website has not been published on your behalf.

Official instructions: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

Relative hash navigation works at both `username.github.io/` and `username.github.io/repository-name/`. No base URL configuration is needed. `.nojekyll` disables Jekyll processing if you include it.

## Included features

- Responsive desktop, tablet and mobile layouts, with bottom navigation on small screens.
- Five-day menu linking directly to all full recipes.
- Recipe and ingredient search, category filters, saved recipes.
- Ingredient lists, tickable method steps, and a large one-step-at-a-time cooking view.
- A consolidated shopping checklist with pack-use explanations, search, remaining-only view and copying. If clipboard access is unavailable, the list downloads as text.
- Weekend and evening prep schedule with completion tracking.
- Actual freezer stock counters, initially zero. Add meals individually or record a fully cooked batch, then subtract each portion as you take it out.
- Print layouts for the weekly menu, shopping list, prep schedule and individual recipes. Printing shopping uses the current filter.
- Keyboard focus styles, semantic controls, labelled inputs, native modal dialogue and reduced-motion support.
- Browser-local persistence for checklist ticks, favourite recipes, recipe steps and freezer counts.

## Using the plan

Start in Shopping and tick cupboard items you already have. Follow Prep plan, then use the meal links during the week. All lunch preparation happens at the weekend or the evening before. Work lunches must stay cold.

The full batch yields 2 bolognese, 2 chilli, 3 curry and 2 fishcake dinner portions, all frozen initially. Four are used in this week's dinners; five remain. The traybake is cooked fresh. Freezer counters are manual records: completing prep tasks or recipes does not change them automatically. They do not record dates; label your containers.

The plan covers five weekday breakfasts, lunches and dinners, daily fruit, and five spare main portions. It does not fully cover weekend meals. £50 is a target, not a priced or verified shopping basket. Prepared vegetable weights may require a small allowance for trimming. Check product labels for allergens and storage requirements.

## Progress and privacy

There are no analytics, login, cookies or backend. Progress is stored using `localStorage` on the current browser and website path. It does not sync between devices, and clearing site data deletes it. Private browsing or storage restrictions may prevent persistence; the site shows when storage is unavailable. Follow the same URL each time.

“Reset checklists” resets shopping, prep and recipe steps after confirmation. It keeps saved recipes and freezer stock. Confirmations prevent accidental bulk stock additions and checklist resets. There are no notifications, date-based reminders, service worker or automatic offline caching. An already downloaded `index.html` is self-contained; the hosted website requires connectivity to load.

## Editing the content

`index.html` is the live source. Its `<script id="meal-data" type="application/json">` block contains the recipes, shopping list, menu and prep schedule. Its following script controls the application and the `<style>` block controls its appearance.

`data.json` is a readable copy of the initial content for reference. **The website does not fetch this file.** If you change it, replace the matching JSON block inside `index.html` as well. Keep recipe IDs and references consistent. Changing quantities may require updates in several places: recipes, consolidated shopping, prep and freezer instructions.

## Checks and limits

Checked all recipe/menu references, embedded JSON, JavaScript syntax and application logic for navigation, search, filters, checklists, saved recipes, cooking mode, reset behaviour, storage reload and freezer counts. Layout includes breakpoints at 1000px and 640px, flexible grids and a full-screen mobile recipe dialogue.

A real-browser visual and interaction pass was not available in the build environment. Before sharing widely, check the published page in your phone and desktop browser, including print preview, keyboard navigation and clipboard permissions. The app uses native `dialog`, `localStorage` and standard modern JavaScript.

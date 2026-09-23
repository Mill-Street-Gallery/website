# Mill Street Gallery Website Guide for Haedan

## Website and repository

- Live website: https://millstreetgallery.org
- GitHub repository: https://github.com/Mill-Street-Gallery/website
- Production branch: `main`
- Hosting: GitHub Pages
- Publishing: Changes merged into `main` automatically deploy to the live website.

## Getting access

Jinsa should invite you to the `Mill-Street-Gallery/website` repository with **Write** access. Accept the invitation using your own GitHub account.

For this website alone, repository access is enough. You do not need owner or administrator access.

## Recommended applications

- GitHub Desktop for syncing and managing branches
- Visual Studio Code for editing files
- Chrome for reviewing the website at desktop and mobile widths

## First-time setup

1. Accept the GitHub invitation.
2. Install GitHub Desktop and sign in.
3. Clone `Mill-Street-Gallery/website` to your computer.
4. Open the cloned folder in Visual Studio Code.
5. Before starting any work, fetch and pull the latest `main` branch.
6. Create a new branch for your work. Use a clear name such as:
   - `haedan/update-about`
   - `haedan/add-exhibition`
   - `haedan/homepage-layout`

Never begin new work from an old branch.

## Daily workflow

1. Switch to `main` in GitHub Desktop.
2. Click **Fetch origin**, then pull any available updates.
3. Create a new branch from the updated `main` branch.
4. Make and preview your changes.
5. Commit with a short description of what changed.
6. Push the branch to GitHub.
7. Open a pull request into `main`.
8. Ask Jinsa to review it before merging.

Do not work directly on `main`. Do not force-push. Do not merge a pull request while someone else is actively editing the same files without coordinating first.

## Previewing the website locally

From the website folder, run:

```bash
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

Review at minimum:

- Desktop width around 1440 px
- Laptop width around 1024 px
- Mobile width around 390 px
- The homepage and every page affected by your change
- Header placement before and after scrolling
- Footer alignment
- All links and buttons

## Current design rules

- Use Times New Roman for all visible text.
- Use pure white, `#ffffff`, for content backgrounds.
- Keep the visual language minimal, quiet, and editorial.
- Avoid decorative effects, rounded cards, drop shadows, gradients, and unnecessary animation.
- The homepage hero uses a grayscale concrete image with natural light and shadow only.
- The hero image uses a fixed, clipped wallpaper effect. The white content scrolls upward over it.
- The title and top menu must remain in exactly the same position while scrolling and between pages.
- The header is transparent over the hero and becomes white after scrolling. Only the background changes, not the header's position.
- Keep the menu small and on one line at desktop widths.
- Small section labels are uppercase and underlined, but still Times New Roman.
- Footer columns must align with the four content cards above.
- Avoid em dashes in website copy.

## Current text that should remain consistent

Homepage description:

```text
Independent exhibitions and programs
in architecture, art and culture
```

Address:

```text
1745 West 7th Street
Los Angeles, CA 90021
```

Hours:

```text
Weekdays 13:00–18:00
Weekends by appointment only
```

## File map

- `index.html`: homepage, footer, and mailing-list dialog
- `styles.css`: all site styling and responsive behavior
- `script.js`: sticky-header state, mobile menu, and mailing-list dialog
- `exhibitions.html`: exhibitions page
- `program.html`: program page
- `archive.html`: archive page
- `about.html`: about and visit information
- `store.html`: store page
- `feature-v8.jpg`: current homepage concrete image
- `favicon.svg`: browser icon
- `CNAME`: custom-domain configuration. Do not edit or delete it.

## Images

- Optimize website images before committing them.
- Use descriptive filenames and avoid spaces.
- Do not overwrite an existing image with a different image under the same filename. Use a new versioned filename and update the CSS or HTML reference.
- Check image cropping at desktop and mobile sizes.

## Before requesting review

- Pull the latest `main` and resolve any conflicts on your branch.
- Confirm that the homepage still loads.
- Confirm that all navigation links work.
- Confirm that the header does not jump when navigating between pages.
- Confirm that no content was accidentally deleted.
- Add a short pull-request summary and screenshots when the change is visual.

## If something goes wrong

Stop before merging. Keep the branch and ask Jinsa to review it. A branch or pull request can be corrected safely; a direct change to `main` immediately affects the live site.

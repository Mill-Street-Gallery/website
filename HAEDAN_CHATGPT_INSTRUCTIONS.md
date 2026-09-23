# ChatGPT Instructions for the Mill Street Gallery Website

Use these instructions whenever helping Haedan work on the Mill Street Gallery website.

## Project

You are working on the existing Mill Street Gallery website.

- Live website: https://millstreetgallery.org
- Repository: `Mill-Street-Gallery/website`
- Production branch: `main`
- Hosting: GitHub Pages
- Technology: static HTML, CSS, and JavaScript

Inspect the existing repository before proposing or making changes. Treat the current site as the design source of truth.

## Collaboration and Git safety

- Never work directly on `main`.
- Before starting, update local `main`, then create a new branch named `haedan/<short-task-name>`.
- Do not force-push, rewrite history, delete branches, or delete files unless Haedan explicitly requests it and confirms the exact target.
- Preserve unrelated work and existing user changes.
- Do not merge or publish unless Haedan explicitly asks.
- Before merging, explain exactly what will change and which files are affected.
- If `main` changed during the work, update the branch and resolve conflicts before requesting review.
- Prefer a pull request into `main` so Jinsa can review the change.

## Design direction

- The site should feel minimal, architectural, editorial, and restrained.
- All visible text uses Times New Roman.
- Content backgrounds are pure white, `#ffffff`.
- Do not introduce Murecho, Cormorant Garamond, or Plus Jakarta Sans.
- Avoid em dashes in all copy.
- Avoid rounded cards, pills, decorative shadows, gradients, bright colors, excessive transitions, and generic template styling.
- Keep rules, borders, and underlines thin and black.
- Maintain generous negative space.

## Homepage behavior

- The homepage begins with a full-screen grayscale concrete hero containing only concrete texture and natural light and shadow.
- Do not add geometric shapes, circles, orange blocks, lines, logos, or text baked into the hero image.
- The hero uses a fixed, clipped wallpaper effect comparable to the full-screen image behavior on https://buro-haru.com/.
- As the visitor scrolls, the white section moves upward over the fixed image.
- The site title and top navigation remain in exactly the same screen position at all times.
- The header begins transparent over the hero and changes to white after scrolling. Its vertical and horizontal placement must not move.
- Header placement must remain identical when navigating between pages. Preserve stable scrollbar spacing.

## Required text

Keep the homepage description on exactly two lines:

```text
Independent exhibitions and programs
in architecture, art and culture
```

Use this address wherever gallery visit information appears:

```text
1745 West 7th Street
Los Angeles, CA 90021
```

Use these hours:

```text
Weekdays 13:00–18:00
Weekends by appointment only
```

## Navigation and page structure

The top navigation contains:

- Exhibitions
- Program
- Archive
- About
- Store

Each item links to its own HTML page. Do not replace these links with homepage anchors.

The homepage preview cards may show one or two current items and include a `See more` link to the appropriate page. Footer columns must align exactly with the four preview-card columns above.

## Editing rules

- Make the smallest change that fully satisfies the request.
- Reuse existing layout, styles, components, and naming patterns.
- Do not rewrite whole files merely to change a small section.
- Keep HTML semantic and accessible.
- Maintain keyboard focus styles and mobile navigation behavior.
- Use responsive CSS. Never solve a desktop issue by breaking mobile layouts.
- Do not add a framework, build system, dependency, or external font unless Haedan and Jinsa approve it first.
- Do not change `CNAME`.
- When replacing an image, use a new versioned filename and update its reference to avoid browser caching.

## Verification required before handoff

Run a local server and review the affected pages at desktop, laptop, and mobile widths.

Verify:

- No console errors
- No broken links or missing images
- No horizontal overflow
- Header does not shift during scrolling
- Header does not shift between pages
- Hero scroll effect still works
- Homepage description remains exactly two lines
- Footer columns remain aligned
- Mailing-list dialog still opens and closes
- Existing content outside the requested change remains intact

At handoff, provide:

1. A concise summary of the result
2. The files changed
3. What was tested
4. Any unresolved issue or decision needed
5. A pull-request link, if one was created

Do not claim that a change was published unless the deployment or live website was actually verified.

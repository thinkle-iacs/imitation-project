# Guide for coding agents helping with Project Imitation

Read `README.md` and `.lesson/part2.md` before substantial work. This is a beginning
web design project: reconstruct a teacher-approved print layout in HTML/CSS, then
adapt it for the web. Unlike earlier projects, **substantial AI coding assistance
is welcome here**. You may generate HTML/CSS, refactor, debug, and help with responsive
adaptation. Explain the choices so the student can understand and direct the work.

## Student decisions and visual verification

- Let the student choose the reference and get teacher approval. Ask for their intended
  dimensions, layout, and specific goals when those are missing.
- Work in useful increments. After each meaningful visual change, ask the student to
  run the page, compare it with the reference, and describe concrete differences.
- Help them compare alignment, spacing, proportions, typography, color, image cropping,
  hierarchy, and layering. Turn their observations into specific next changes.
- Use the comparison viewer's Side-by-side mode, then open the design in its own tab
  to inspect actual dimensions. The original image scales to fit the viewer; its displayed
  size is not a measurement of the imitation.
- Check the responsive page at phone, tablet, desktop, and intermediate widths. The
  iframe responds to its own width, so use the pop-out for independent viewport testing.
- You may inspect screenshots or run checks when tools allow, but never claim the
  student's personal visual verification has happened. Distinguish what you checked from
  what the student still needs to check. Do not fabricate screenshots, observations, or logs.
- Help record the student's actual observations and screenshot paths in `TODO.md`.
  The student writes their final design analysis and explains the design decisions.

## Files and boundaries

- Fixed-size design: `imitation.html` and `imitation.css`.
- Responsive adaptation: `responsive.html` and `responsive.css`.
- `index.html` is the provided viewer: change only the reference image path, alt text,
  and source caption. Keep navigation, side-by-side, pop-outs, and iframe structure intact.
- Leave `do_not_modify/`, runtime configuration, and the Pages workflow alone when
  helping with student design work. Teacher maintenance may update this infrastructure.
- Use vanilla HTML/CSS: flexbox, grid, media queries, and positioning are allowed.
  Do not introduce frameworks, new dependencies, build tools, or student-written JS.
- Reconstruct the layout with meaningful HTML and CSS. Do not use a flattened screenshot
  of the original as the finished imitation, or replace all content with a background image.
- Keep links to `citations.html`. Cite substitute assets and include useful image alt text.
- Start with `npm install`, then `npm start`; preview port 5500. No build step is needed.

## Required citations

Students must cite **all AI assistance**, including brainstorming, code, explanations,
writing, and images. Treat citations as part of the work.

For generated or substantially rewritten HTML/CSS:

1. Wrap the region in comments appropriate to the file type. Name the AI tool and include
   the student's prompt or a short faithful summary.
2. Add an entry under AI Use in `citations.html`: tool, date, request, assistance received,
   and what the student changed or personally checked. If checking is pending, say so.
3. Replace the initial no-AI placeholder on first use. Ask the student to correct any
   inaccurate account in their own words.

For example:

```css
/* AI-generated code starts here — GitHub Copilot
   Student prompt: "Use a grid for the three columns in my reference." */
.layout { display: grid; grid-template-columns: repeat(3, 1fr); }
/* AI-generated code ends here */
```

For ideas or explanations without generated code, add an AI Use entry without code fences.
Credit the original design, fonts, images, and borrowed code under Sources with links.
Never remove or weaken existing AI comments or citation entries to hide assistance.

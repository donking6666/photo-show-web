# 765b6e21-4ee2-4cdf-88c9-23b03f503782 implementation handoff

This archive is the source of truth for turning the design into production code. Start from `index.html`, then preserve the visual system, responsive behavior, and interactions found in the exported files.

## Implementation target
- Build production UI from the exported design, not a loose reinterpretation.
- Preserve typography scale, spacing rhythm, color tokens, border radii, shadows, motion timing, and component states.
- Replace static placeholders only when the target app has real data or functional equivalents.
- Keep generated product UI free of Open Design chrome, preview labels, or design-process annotations.
- Treat this handoff as a visual contract: if implementation choices conflict, match the exported pixels and behavior first, then refactor internals.

## Source map
- Primary entry: `index.html`
- HTML screens detected: 1
- Stylesheets detected: 0
- Script/component files detected: 0
- Supporting assets detected: 58

## Responsive contract
Validate the implementation across this 2025–2026 viewport matrix:
- Mobile compact: 360×800
- Mobile standard: 390×844
- Mobile large: 430×932
- Foldable / small tablet: 600×960
- Tablet portrait: 820×1180
- Tablet landscape: 1024×768
- Laptop: 1366×768
- Desktop: 1440×900
- Wide desktop: 1920×1080

For responsive web exports, treat these as a modern breakpoint system for one adaptive web experience, not three fixed screenshots. Do not split responsive web into unrelated native app screens unless the project explicitly includes native targets. Use semantic layout thresholds, fluid `clamp()` type/spacing, and container queries where component width matters more than viewport width. Preserve any CSS media queries, container queries, fluid `clamp()` scales, and layout changes already present in the exported files.

## Design fidelity contract
- Extract reusable tokens before writing components: background, surface, foreground, muted text, border, accent, radius, shadow, spacing, type scale, and motion duration/easing.
- Map product screens, in-app modules/components, optional landing page, and optional OS widget surfaces before coding. Keep these surfaces separate in the target architecture.
- Match layout geometry: max-widths, gutters, grid columns, card proportions, sticky/fixed elements, and viewport-specific navigation.
- Preserve real copy, labels, and data shown in the export. Do not replace specific text with generic marketing filler.
- Preserve interactive affordances: hover, focus, pressed, disabled, loading, validation, copy/share, tab/accordion, modal/sheet, and keyboard states where present.
- Preserve accessibility semantics when converting: headings stay hierarchical, controls remain buttons/links/inputs, focus states stay visible.
- Do not keep prototype-only annotations, frame labels, or Open Design chrome in the production UI.

## CJX-ready UX contract
- Use `DESIGN-MANIFEST.json` as the machine-readable map for screens, app modules, OS widgets, landing pages, tokens, interactions, and viewport checks.
- Screen-file-first: when multiple user-facing surfaces exist, implement each HTML screen as its own route/file. Treat `index.html` as a launcher/overview when the manifest marks it that way, not as a combined final UI.
- If `landing.html`, app screens, platform screens, or OS widget files exist, preserve those boundaries in the target app instead of merging them into one page.
- A single self-contained `index.html` is acceptable only when the export truly contains one user-facing screen and its CSS/JS are structured enough to extract tokens, components, states, and behavior.
- If separate `css/` or `js/` files exist, treat them as source of truth for token/component/interactions before porting to React, Vue, SwiftUI, Compose, or another target stack.
- In-app modules/components are product UI blocks inside the app. OS widgets are home-screen/lock-screen/quick-access surfaces outside the app. Do not merge those concepts.

## Color and brand contract
- Use the exported design tokens and product/domain context as the color source of truth.
- Do not introduce warm beige / cream / peach / pink / orange-brown background washes unless they are already explicit brand/reference colors in the export.
- No obvious token stylesheet was detected; sample colors from the entry file and convert them into named tokens before coding.

## Implementation sequence for AI coding tools
1. Open `index.html` and `DESIGN-MANIFEST.json`; identify every screen file, launcher/overview file, app module, and interaction before coding.
2. If multiple HTML screens exist, map them to separate routes/surfaces first; do not merge `landing.html`, product app screens, platform screens, or OS widgets into one route.
3. Extract a token table from CSS/root styles and inline styles before building framework components.
4. Build product screens and domain-specific in-app modules from largest layout regions down to controls; avoid starting with isolated atoms that lose spatial intent.
5. Port responsive behavior across the modern viewport matrix and test each semantic breakpoint before cleanup.
6. Port interactions and states, then replace static placeholders only with real app data or functional equivalents.
7. Keep optional landing page and OS widget surfaces as separate surfaces if present.
8. Compare final screenshots against the export at 360×800, 390×844, 430×932, 820×1180, 1024×768, 1366×768, 1440×900, and 1920×1080 before declaring done.

## Entry points
- `index.html`

## Styles
- None detected

## Scripts/components
- None detected

## Assets and supporting files
- `${APPDATA}/npm/claude`
- `${APPDATA}/npm/claude.cmd`
- `${APPDATA}/npm/claude.ps1`
- `0099cfbcb46e184feca29803843cd7e4.jpg`
- `08a814661c1858a5a697668b4366c558.jpg`
- `15f21cad34ae00b60d4699dedb8959f1.jpg`
- `25af5ae31735cbfb0eaf987f83de8862.jpg`
- `385aeb0635dcddfd86cc832d429e7e81.jpg`
- `48dec85f3cd4adfad8135def18d88d6c.jpg`
- `4fdf286c66b936d5ecc4939c85d4708a.jpg`
- `678bbcb82ef71f267352c2eea32c1986.jpg`
- `6a62c9d5401c5814ab11fedf52734c64.jpg`
- `851f18cc537a58588ce86c6f65be4c20.jpg`
- `899b00e2c62eb51362c9980794b59365.jpg`
- `8b4209e8b231360c413bbda4cc71cb80.jpg`
- `8e23d2d19489b8af698031c76b931362.jpg`
- `99826d3cb692054f69d2efb5b4d577f8.jpg`
- `b02b1021e86f2f37eff6739e97f44b2a.jpg`
- `b6eb12aa4818023d08bc823a2705cc6f.jpg`
- `ce4b2d71bf2d843bfd6491d6eea4aad1.jpg`
- `ChatGPT Image 2026年6月17日 20_43_06 (1).png`
- `ChatGPT Image 2026年6月17日 20_43_06 (10).png`
- `ChatGPT Image 2026年6月17日 20_43_06 (2).png`
- `ChatGPT Image 2026年6月17日 20_43_06 (3).png`
- `ChatGPT Image 2026年6月17日 20_43_06 (4).png`
- `ChatGPT Image 2026年6月17日 20_43_06 (5).png`
- `ChatGPT Image 2026年6月17日 20_43_06 (6).png`
- `ChatGPT Image 2026年6月17日 20_43_06 (7).png`
- `ChatGPT Image 2026年6月17日 20_43_06 (8).png`
- `ChatGPT Image 2026年6月17日 20_43_06 (9).png`
- `de2cdbee27934b33c12b7b52bca049a6.jpg`
- `e57a779b46e5a7117f5b4d4095150004.jpg`
- `f527970d510c348699de8a6d84efc5b6.jpg`
- `f86e16c2c38af366672e73e0c8522feb.jpg`
- `mqhe7gml-IMG_7096.JPEG`
- `mqhew9gu-image.png`
- `mqheyfnr-image.png`
- `mqhfxpro-drawing-2026-06-17T02-17-23-117Z.png`
- `mqhfyqo8-drawing-2026-06-17T02-18-10-946Z.png`
- `mqhfzvq5-drawing-2026-06-17T02-19-04-153Z.png`
- `mqhgjlbh-drawing-2026-06-17T02-34-23-784Z.png`
- `mqhgn7ts-drawing-2026-06-17T02-37-12-923Z.png`
- `mqhgo4n0-drawing-2026-06-17T02-37-55-448Z.png`
- `mqhgp37v-drawing-2026-06-17T02-38-40-263Z.png`
- `mqhgq5il-drawing-2026-06-17T02-39-29-896Z.png`
- `mqhgrnme-drawing-2026-06-17T02-40-40-016Z.png`
- `mqhhbzdk-image.png`
- `mqhij78n-drawing-2026-06-17T03-30-04-769Z.png`
- `mqhj70xh-drawing-2026-06-17T03-48-36-336Z.png`
- `mqhqwyil-drawing-2026-06-17T07-24-43-570Z.png`
- `mqhr4opi-image.png`
- `mqht24vn-drawing-2026-06-17T08-24-44-328Z.png`
- `mqhuxfo0-image.png`
- `mqiz1r07-image.png`
- `mqj1gbnv-drawing-2026-06-18T05-07-29-408Z.png`
- `mqjf9vhi-0054879da6e9dfb0b76b703cf6834954.jpg`
- `mqjftwt6-drawing-2026-06-18T11-49-57-968Z.png`
- `mqjg1rt0-image.png`

## Coding checklist for AI tools
1. Inspect `index.html` and `DESIGN-MANIFEST.json` first and identify reusable components before coding.
2. Implement each user-facing screen file as its own route/surface; keep launcher, landing, app, platform, and OS widget files separate.
3. Extract design tokens into the target stack: colors, type scale, spacing, radius, shadows, and motion.
4. Implement layout with real 2025–2026 responsive breakpoints, fluid type/spacing, and container-query-aware component behavior; test with no horizontal overflow.
5. Preserve interactive controls, hover/focus/pressed states, form behavior, validation, and copy actions where present.
6. Implement domain-specific in-app modules with real states; do not flatten them into generic cards.
7. Keep landing page, product screens, and OS widget/quick-access surfaces separate when present.
8. Confirm the production result visually matches the exported design before refactoring internals.
9. Reject implementation shortcuts that flatten the design into generic cards, generic gradients, placeholder stats, or framework-default typography.
10. If a detail is ambiguous, keep the exported HTML/CSS/JS behavior rather than inventing a new pattern.

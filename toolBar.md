Update ONLY the existing Clients page toolbar/filter section to make it more compact, modern, and user-friendly.

IMPORTANT SCOPE RULES:
- Do NOT modify any other page, component, route, API, data, table, KPI card, sidebar, header, or functionality.
- Do NOT change the existing search/filter/sort behavior or state management.
- Do NOT create unnecessary new components or files.
- Reuse the existing components, icons, handlers, and styling conventions wherever possible.
- Only modify the files/components/CSS that are directly responsible for the Clients page toolbar.

UI GOAL:
Redesign the current toolbar to follow this compact horizontal pattern:

[ Search by name, ID or email ] [ 🔽 Filters ① ] [ ↕ Sort: Priority ▾ ] [ ⚙/sliders ]

The toolbar should be a single compact horizontal row instead of having separate "Filter" and "Sort" labels above their dropdowns.

SEARCH:
- Keep the existing search input and its functionality.
- Make it the largest/flexible element of the toolbar.
- Keep the search icon inside the input.
- Placeholder should remain "Search by name, ID or email".
- Vertically center it with the other controls.

FILTER:
- Replace the current vertically labelled "Filter" dropdown presentation with a compact button/control containing:
  - filter/funnel icon
  - text "Filters"
  - optional active-filter count badge, e.g. "1"
- Clicking it must continue to provide the existing filter functionality.
- Do not remove or change the existing filtering logic.
- The control should have the same height as the search input and sort control.

SORT:
- Replace the current vertically labelled "Sort" presentation with a compact dropdown/button:
  - sort icon
  - text such as "Sort: Priority"
  - dropdown chevron
- Preserve the existing sort functionality and available sort options.
- Do not hard-code the sorting logic just for visual purposes.

ADDITIONAL CONTROLS:
- If the existing implementation has a Reset button, do NOT keep a large blue Reset button permanently occupying toolbar space.
- Instead, make Reset compact/subtle and show it only when appropriate, such as when filters/search/sort differ from their default state.
- If there is already an existing table/settings/filter icon that can represent additional controls, use that existing icon/component rather than introducing a new icon library.
- Do not add unnecessary functionality.

LAYOUT:
- Toolbar must be one horizontal row on desktop.
- Search should flex/grow and occupy most available width.
- Filters and Sort should have compact fixed/auto widths.
- Keep consistent spacing between controls.
- Reduce the overall vertical height significantly compared with the current toolbar.
- The toolbar should feel like a professional banking/wealth-management dashboard.
- Keep the existing page width, margins, card styling, border radius, typography, and color language consistent with the rest of the Clients page.
- Do not make the toolbar visually heavier than the KPI cards or table.
- Controls should be vertically centered.
- Use subtle borders/backgrounds and the existing blue accent color only where appropriate.
- Avoid excessive shadows, gradients, oversized buttons, or unnecessary decoration.

RESPONSIVE BEHAVIOR:
- Preserve responsive behavior.
- On smaller screens, allow the controls to wrap gracefully rather than overflowing.
- Search should take the full available width when necessary.
- Do not break the existing Clients table layout.

REFERENCE DESIGN:
Use the compact toolbar concept shown below as the visual target:

Search by name, ID or email | Filters ① | Sort: Priority ▾ | sliders/settings icon

The key difference from the current UI is:
CURRENT:
Search + Filter label above dropdown + Sort label above dropdown + large Reset button

TARGET:
Search + compact Filters button + compact Sort button + optional compact settings/filter icon

After making the changes:
1. Verify that search still works.
2. Verify that filtering still works.
3. Verify that sorting still works.
4. Verify that Reset/default-state behavior still works.
5. Verify that no unrelated files or components were modified.
6. Keep the implementation clean and consistent with the project's existing architecture.
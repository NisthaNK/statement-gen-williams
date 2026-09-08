STOP AND REDESIGN THE TASK PAGE UI PROPERLY.

The current Task page implementation is NOT acceptable visually or from a usability perspective. The table is overflowing/cut off on the right side, the page does not resemble the intended reference design, and the overall layout feels unfinished.

I CANNOT PROVIDE YOU THE REFERENCE IMAGE DIRECTLY, so use the following detailed description as the visual specification.

IMPORTANT SCOPE:
- Work ONLY on the frontend Task page.
- Do NOT modify backend code.
- The existing Task backend controller/API already exists and is working.
- Use the existing Task API/service and its real response data.
- Do NOT change DTOs, controllers, services, repositories, database code, or API contracts.
- Do NOT modify Dashboard, ClientList, ClientOverview, Products, Profile, Settings, or any other page.
- Do NOT redesign the whole application.
- Do NOT modify unrelated shared components.
- Reuse the existing application's sidebar/header/layout where appropriate.
- If a shared component must be changed for the Task page, first determine whether it can be avoided. Prefer Task-page-specific styling instead.
- Do not create mock data when real Task API data is available.

FIRST:
Inspect the current Task page implementation and compare it against:
1. The existing application's UI patterns.
2. The existing Task API response structure.
3. The visual specification below.

Then REWORK the Task page UI rather than making small cosmetic changes.

==================================================
VISUAL TARGET
==================================================

The Task page should look like a polished professional wealth-management/banking application.

The overall structure should be:

LEFT:
Existing application's dark navy sidebar/navigation.

MAIN CONTENT:
A clean white/light background with a properly contained Task page.

TOP OF MAIN CONTENT:
A header area containing:

Tasks
All tasks across all clients

The title should have strong visual hierarchy.

Below the title:
A toolbar containing:

[ Search tasks/client... ]       [ Filter ▼ ] [ Sort ▼ ] [ Refresh ]

The toolbar should be properly aligned on ONE horizontal row on normal desktop widths.

Do not allow these controls to overlap or wrap awkwardly.

==================================================
TABLE
==================================================

Below the toolbar, create a clean professional table inside a bordered/card-like container.

The table must fit properly inside the available main-content width.

VERY IMPORTANT:
The table MUST NOT extend beyond the viewport.

Do NOT simply allow the page to become horizontally broken because of excessive fixed column widths.

Use:
- flexible column widths
- appropriate min/max widths
- text wrapping where appropriate
- ellipsis for unusually long text if necessary
- a responsive table container

The table should have exactly these columns:

1. Priority
2. Task
3. Client Name
4. Client ID
5. Due Date
6. Status
7. Created On

DO NOT INCLUDE:
- Assigned To
- Action
- View
- View button

There must be NO Action/View column at all.

==================================================
COLUMN DESIGN
==================================================

Priority:
Use compact professional badges:

HIGH
MEDIUM
LOW

The badges should be small, rounded and visually subtle, similar to a modern banking dashboard.

Task:
Display the actual task name from the API.

Client Name:
Display the actual client name from the API.

Client ID:
Display the actual client ID.

Due Date:
Display the date in a clean readable format.

If overdue, visually indicate that it is overdue.
If there is an existing reliable way to calculate "Due in X days", show that underneath the date in a smaller subtle style.

Do not invent incorrect business logic.

Status:
Use compact status badges based on the ACTUAL backend status values.

For example, if the API returns:
- PENDING
- IN PROGRESS
- COMPLETED
- OVERDUE

display them as clean status badges.

Do not invent statuses that don't exist in the API.

Created On:
Display the actual creation date from the backend in a readable format.

==================================================
REFERENCE STYLE
==================================================

The intended visual style is similar to a professional Task management table:

- Dark navy application sidebar
- White main content
- Large "Tasks" heading
- Smaller subtitle "All tasks across all clients"
- Search field with search icon
- Filter button
- Sort button
- Refresh icon/button
- Rounded but professional controls
- Light borders
- Subtle shadows
- Good whitespace
- Clean table header
- Compact rows
- Clear column alignment
- Small priority/status pills
- Blue used as the primary interactive/accent color
- Professional banking/wealth-management appearance

Do NOT make it look like a generic HTML table.

==================================================
SPACING AND SIZING
==================================================

This is VERY IMPORTANT.

The current implementation looks cramped and overflows.

Fix the layout so:

- The Task title has sufficient top/left spacing.
- The subtitle sits directly below the title.
- The toolbar has proper spacing from the title and table.
- The table has comfortable row height.
- Table headers align exactly with their columns.
- Cell contents do not collide.
- The table stays inside the main content area.
- There is enough padding around the table.
- The sidebar does not overlap the main content.
- The content area uses the available desktop width correctly.
- Avoid unnecessary vertical scrolling.
- Do not create unnecessary horizontal scrolling.

The page should feel balanced, not like the table is being squeezed into a narrow area.

==================================================
PAGINATION
==================================================

At the bottom of the table/card, create a clean pagination section.

Left side:

Showing X to Y of Z tasks

Right side:

Previous   1   2   3   4   5   ...   Next

Keep pagination compact.

DO NOT allow 20+ page buttons to stretch across the entire screen like the current implementation.

Use ellipsis when there are many pages.

The active page should have the application's primary blue styling.

Pagination must actually work with the existing Task data/API.

If the backend already supports pagination, use it.

If the backend returns all tasks, implement frontend pagination without modifying the backend.

==================================================
SEARCH
==================================================

Search should work against the actual Task data.

At minimum, search by:
- task name
- client name
- client ID

If the existing backend provides search functionality, use it.

Otherwise, perform client-side filtering.

Do not modify the backend merely to add search.

==================================================
FILTER
==================================================

Create a professional Filter dropdown/popover.

Use actual fields available from the Task API.

At minimum, if available:
- Priority
- Status

The filter should actually affect the displayed tasks.

Do not modify the backend just for frontend filtering.

==================================================
SORT
==================================================

Create a professional Sort dropdown.

Useful options can include:
- Due Date
- Created On
- Priority

Use the actual Task data.

The sort should actually work.

==================================================
REFRESH
==================================================

The refresh button should call the existing Task API/service again and update the table.

Do not reload the entire browser.

==================================================
LOADING STATE
==================================================

While the Task API is loading:

Do NOT show a broken empty table.

Use a clean loading state consistent with the existing application's UI.

It can be a centered "Loading tasks..." state or a polished skeleton if the project already has a suitable pattern.

==================================================
ERROR STATE
==================================================

If the API fails:

Show a clean error message inside the Task page.

Provide a retry/refresh option.

Do not break the sidebar or rest of the application.

==================================================
MOST IMPORTANT UI FIX
==================================================

The current screenshot shows the table being cut off on the right.

FIX THIS COMPLETELY.

The Task page must be usable at normal desktop resolution.

The table must be contained within the main content area.

Do NOT solve this by simply shrinking the font to an unreadable size.

Instead use proper:
- layout
- flex/grid sizing
- table layout
- column widths
- padding
- overflow handling
- responsive behavior

The table should look intentional and polished.

==================================================
CONSISTENCY WITH EXISTING APPLICATION
==================================================

Do NOT copy the reference application's branding/sidebar literally.

Our existing application already has:
- Standard Chartered branding
- WealthCore
- Dashboard
- Clients
- Products
- Tasks
- Profile/Settings

Keep the existing application's navigation and branding.

Tasks should simply become the active navigation item.

The Task page content should visually belong to the same application as the existing Dashboard, ClientList, ClientOverview, Products and Profile pages.

Reuse existing design tokens/styles/components where appropriate.

==================================================
DATA / BACKEND
==================================================

Use the existing Task backend exactly as it currently exists.

Inspect the existing TaskController and taskService/API response only to understand the data.

DO NOT modify backend code.

Correctly map the existing backend response fields into:

Priority
Task
Client Name
Client ID
Due Date
Status
Created On

If field names differ, map them in the frontend.

Do not change the API contract.

==================================================
FILE SAFETY
==================================================

Before modifying files, identify exactly which frontend files are required.

Do not make broad changes.

After implementation, report:

1. Which files were changed.
2. Which files were NOT changed.
3. Confirm whether any backend file was modified.
4. Confirm the exact Task API endpoint/service function being used.
5. Confirm that Assigned To and Action/View columns were removed.
6. Confirm that search/filter/sort/pagination/refresh work.
7. Confirm that the table no longer overflows the main content area.

If you discover that a backend change is absolutely necessary, DO NOT make it automatically. Stop and explain why it is unavoidable and wait for approval.

The priority is:
FUNCTIONAL EXISTING API + POLISHED TASK UI + ZERO IMPACT ON OTHER PAGES.
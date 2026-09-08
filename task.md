I want you to implement/refactor ONLY the frontend Task page.

IMPORTANT SCOPE RULE:
- Do NOT modify any backend code.
- The backend controller/API for Tasks already exists and is working. Reuse the existing API exactly as it is.
- Do NOT modify backend DTOs, controllers, services, repositories, routes, or API contracts unless you discover an absolutely unavoidable issue that makes the existing Task API impossible to consume. If that happens, STOP and explain the issue before changing backend code.
- Do NOT modify any other frontend page, component, CSS, API service, routing logic, or shared component unless it is strictly necessary for the Task page to work.
- Do NOT change the functionality of Dashboard, ClientList, ClientOverview, Products, Profile/Settings, or any other existing page.
- All changes should be limited to the existing Task page and its directly related frontend files.
- Preserve all existing functionality outside the Task page.

FIRST, inspect the existing project:
1. Find the existing Task page/component.
2. Find the frontend API/service function currently used or intended to fetch Task data.
3. Inspect the existing backend Task controller/DTO/API only to understand the exact response structure and available fields. DO NOT modify it.
4. Inspect the existing frontend pages/components and styling patterns to understand the application's current UI language.
5. Reuse existing shared layout/navigation/header/components where appropriate instead of creating duplicate versions.
6. Understand how loading, errors, API calls, pagination, filtering, and sorting are currently handled elsewhere in the application.

UI REQUIREMENT:
Make the Task page visually similar to the provided reference design.

The reference has:
- A dark navy left sidebar
- WealthCore branding
- Dashboard / Clients / Reports / Tasks / Communications / Settings navigation
- Tasks highlighted as the active page
- A clean white/light main content area
- Page title: "Tasks"
- Subtitle: "All tasks across all clients"
- Search bar
- Filter control
- Sort control
- Refresh button
- Clean bordered table/card
- Pagination at the bottom
- Professional banking/wealth-management styling
- Compact priority/status badges
- Good spacing, alignment, typography, borders and subtle shadows
- Overall UI should look polished and consistent with the existing application

VERY IMPORTANT:
Do not blindly copy the reference application's entire layout if our existing application already has a shared sidebar/header/navigation component.

Instead:
- Keep our application's existing shared navigation/sidebar/header structure and styling conventions.
- Make the Task page feel like it belongs to the same application as Dashboard, ClientList, ClientOverview, Products, and Profile.
- Only adapt the Task page's content area to achieve the reference design.
- Reuse existing CSS variables, typography, spacing, colors, buttons, cards, icons, etc. wherever possible.

TABLE COLUMNS:
I want ALL of these columns from the reference EXCEPT:

DO NOT INCLUDE:
- Assigned To
- View/Action

Include:
1. Priority
2. Task
3. Client Name
4. Client ID
5. Due Date
6. Status
7. Created On

The final table should therefore have exactly these 7 columns:
Priority | Task | Client Name | Client ID | Due Date | Status | Created On

Do not add an Action/View column.

DATA:
Use the existing Task backend API and its actual response fields.
Do NOT create fake/mock task data if the real API is already available.

Map the backend response fields to the UI correctly.

If the backend already provides priority, task name/type, client name, client ID, due date, status, and created date, use those values directly.

If the backend uses different field names, correctly map those existing fields to the UI labels above without changing the backend.

LOADING STATE:
Implement a clean loading state while the Task API is being fetched.

Do not show a broken/empty table while loading.
Prefer a simple, polished loading treatment consistent with the existing application's loading patterns.

ERROR STATE:
If the API request fails:
- Show a clean user-friendly error state/message in the Task page.
- Provide a retry/refresh option if appropriate.
- Do not break the rest of the application.

SEARCH:
Implement the search UI shown in the reference.

The search should allow searching tasks based on the data actually available from the existing Task API, such as:
- Task
- Client Name
- Client ID

Do not invent backend search parameters if the existing API does not support server-side search.

If filtering/search is already supported by the backend API, use the existing API capability.
Otherwise, perform client-side filtering on the fetched Task data.

FILTER:
Add the Filter control visually similar to the reference.

Use the actual Task fields available from the API.
At minimum, if those fields exist, allow filtering by:
- Priority
- Status

Do not modify the backend just to introduce filtering.

SORT:
Add the Sort control.

Allow useful sorting based on the existing data, for example:
- Priority
- Due Date
- Created On

Implement this on the frontend unless the existing API already provides sorting.

DUE DATE:
Display the due date cleanly.

If the date is overdue, visually distinguish it in a subtle way similar to the reference.
If a task is due soon, display an appropriate "Due in X days" style indicator if this can be calculated reliably from the existing date.

Do not invent business logic that conflicts with the backend.

PRIORITY:
Display priority as compact badges similar to the reference:
- HIGH
- MEDIUM
- LOW

Use the actual priority returned by the API.

STATUS:
Display status as compact badges similar to the reference:
- OVERDUE
- PENDING
- IN PROGRESS
- etc., depending on the actual values returned by the backend.

Do not hard-code statuses that do not exist in the API merely for appearance.

PAGINATION:
The reference has pagination at the bottom.

Implement pagination using the existing API if server-side pagination already exists.

If the existing Task API returns the complete task list without pagination, implement frontend pagination without changing the backend.

Show something similar to:
"Showing X to Y of Z tasks"

Make sure pagination actually works.

REFRESH:
Add the refresh button shown in the reference.
It should re-fetch the Task data using the existing API/service function.

Do not reload the entire browser unless the current application architecture already does that.

RESPONSIVENESS:
Keep the Task page usable at different desktop window sizes.
The table should not cause unnecessary horizontal scrolling if the existing application design can avoid it.
Keep column alignment consistent and readable.

CODE QUALITY:
- Follow the existing project's React/JavaScript/TypeScript conventions.
- Reuse existing components where appropriate.
- Do not introduce unnecessary libraries.
- Do not create duplicate components that already exist.
- Keep the implementation simple and maintainable.
- Keep API logic separated from UI logic if that is already how this project is structured.
- Do not rewrite unrelated code.
- Do not make broad refactors.

MOST IMPORTANT:
This is an isolated Task-page UI implementation.

DO NOT:
- modify backend
- modify other pages
- redesign the entire application
- change existing APIs
- change unrelated shared components
- remove existing functionality
- create fake backend data

Before making changes, inspect the existing Task page, Task API/service, Task DTO/controller response structure, and existing UI patterns.

Then implement the Task page using the existing architecture.

After implementation, verify:
1. The Task page loads real data from the existing backend.
2. The 7 requested columns are displayed.
3. Assigned To is NOT displayed.
4. View/Action is NOT displayed.
5. Search works.
6. Filter works.
7. Sort works.STOP AND REDESIGN THE TASK PAGE UI PROPERLY.

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
8. Refresh works.
9. Pagination works.
10. Loading state works.
11. Error state works.
12. Existing pages remain untouched and unaffected.
13. No backend code was changed.

If you find that a backend change is genuinely unavoidable, DO NOT make it automatically. Explain exactly why it is necessary and wait for approval.
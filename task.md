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
7. Sort works.
8. Refresh works.
9. Pagination works.
10. Loading state works.
11. Error state works.
12. Existing pages remain untouched and unaffected.
13. No backend code was changed.

If you find that a backend change is genuinely unavoidable, DO NOT make it automatically. Explain exactly why it is necessary and wait for approval.
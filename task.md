I need a focused refinement of the existing FRONTEND TASK PAGE ONLY.

Do NOT redesign the whole page again. Keep the current Task page UI/layout that you just implemented, but make the following functional and UI corrections.

IMPORTANT SCOPE:
- Work ONLY on the frontend Task page and the minimum Task-related frontend files required.
- Do NOT modify Dashboard, Clients/ClientList, ClientOverview, Products, Profile, Settings, or any other page.
- Do NOT modify backend code unless absolutely unavoidable.
- The existing Task backend API/controller/service already exists and must continue to be used.
- Do not change the backend API contract.
- Do not introduce mock task data.

==================================================
1. DEFAULT TASK ORDER — OVERDUE ABOVE PENDING
==================================================

By default, tasks must NOT appear randomly/mixed between overdue and pending.

The default appearance/order should ALWAYS prioritize overdue tasks above pending tasks.

Expected default ordering:

1. OVERDUE tasks first
2. PENDING tasks after overdue tasks
3. Other statuses after those, using sensible existing ordering

Within the same status group, preserve a sensible order such as due date / existing API order.

IMPORTANT:
- This should be the DEFAULT table ordering when the user first opens the Tasks page.
- It should also remain logically consistent after refresh.
- Do NOT permanently change the backend ordering.
- Implement the ordering in the frontend unless the existing backend already provides the required ordering.
- Do NOT treat "overdue" merely as a visual badge. It must participate in the default sorting/order.

If the existing API represents overdue using a status field, use that actual status.

If overdue is derived from due date + status, inspect the existing application logic and use the correct existing business rules. Do not invent conflicting rules.

==================================================
2. PRIORITY MUST BE DECIDED THE SAME WAY AS CLIENTS PAGE
==================================================

This is VERY IMPORTANT.

The Task page currently displays HIGH / MEDIUM / LOW priority, but the priority must be determined using the SAME logic/business rule already used by the Clients page.

Inspect the existing Clients page and its related frontend/backend logic to understand exactly how a client/task's priority is determined.

Do NOT create a new independent priority calculation.

Reuse the existing priority logic wherever possible.

The resulting Task priority should follow the same meaning/order:

HIGH
MEDIUM
LOW

For example, if the Clients page determines priority based on certain client/task conditions, use that exact existing rule rather than assigning arbitrary priorities.

Do not hard-code all tasks to LOW/HIGH/etc.

Do not use random/mock priority values.

If the existing Clients implementation calls a service/helper/function to determine priority, reuse that function or the same logic rather than duplicating a different implementation.

IMPORTANT:
Do not modify the Clients page while doing this.
Only reuse/consume the existing logic from the Task page.

==================================================
3. ADD "MARK AS COMPLETED" ACTION
==================================================

Add an action/button alongside each task that allows the user to change the task status to COMPLETED.

The current table intentionally does NOT have the old "View" or "Action" column.

Do NOT bring back the old View column.

Instead, add a compact action associated with each task row, such as:

[Complete]

or an appropriate small checkmark/button.

The action should be visually consistent with the existing WealthCore UI.

When the user clicks it:

1. Confirm that the task is being marked as completed if confirmation is appropriate for the existing application style.
2. Call the EXISTING backend API/service method for updating/completing a task IF such an endpoint already exists.
3. Do NOT invent a new endpoint.
4. Do NOT modify the backend just because the UI needs this.
5. After successful completion, update the task's status in the UI immediately.
6. The completed task should no longer appear under the overdue/pending group.
7. The table ordering should update automatically after completion.
8. Show an appropriate success/error state.

If the existing backend DOES NOT currently provide a way to update task status:

DO NOT modify the backend automatically.

Instead, inspect the existing TaskController/service and tell me exactly what is missing and why a backend change would be required. Do not implement a fake frontend-only completion that gives the impression that the server data was updated.

==================================================
4. COMPLETED TASKS
==================================================

Completed tasks should display a clear COMPLETED status badge.

They should not be treated as overdue even if their due date is in the past.

Priority/status logic must distinguish:

COMPLETED
OVERDUE
PENDING
etc.

Do not mark a completed task as overdue merely because its due date has passed.

==================================================
5. THE PAGE MUST NOT SCROLL
==================================================

The Tasks page itself must NOT become a vertically or horizontally scrollable page under normal desktop resolution.

This is a strict requirement.

The current page should fit within the application's available viewport.

Do NOT solve this by making the entire page horizontally scrollable.

Do NOT solve it by making the entire page vertically scrollable.

Instead fix the layout properly.

The table should fit inside the available content area.

Use:
- appropriate column widths
- compact but readable row heights
- proper padding
- responsive sizing
- sensible pagination
- ellipsis/wrapping where necessary

The sidebar and header must remain in their existing positions.

The main Task content should fit cleanly within the viewport.

If the number of tasks exceeds what can be displayed at once, use the existing pagination rather than allowing the entire page to grow indefinitely.

==================================================
6. PAGINATION
==================================================

Keep pagination at the bottom of the Task table/card.

Do not display a huge number of page buttons.

Use a compact pattern such as:

Previous  1  2  3  ...  19  Next

The pagination must remain within the viewport.

Filtering, searching, sorting and status changes should work correctly with pagination.

==================================================
7. SEARCH / FILTER / SORT
==================================================

Keep the existing search, filter, sort and refresh functionality.

Make sure the new default overdue-first ordering does NOT break the user's explicit Sort selection.

Meaning:

DEFAULT:
Overdue → Pending → other statuses

But if the user explicitly selects a sort option such as Due Date or Created On, respect that explicit selection.

Do not silently override a user-selected sort.

After changing a task to COMPLETED, recalculate the displayed ordering appropriately.

==================================================
8. IMPORTANT — DO NOT BREAK EXISTING UI
==================================================

Keep the Task page's current visual style that was just implemented.

Only improve/refine the required areas:

- default overdue-first ordering
- priority calculation
- task completion action
- no page scrolling
- correct pagination behavior

Do not unnecessarily change:
- sidebar
- header
- branding
- colors
- overall table design
- search layout
- existing navigation
- other pages

==================================================
9. BEFORE CODING
==================================================

First inspect:

- existing Task page
- Task API/service
- TaskController only for understanding the available API
- Clients page
- Clients-related priority logic/service/helper

Determine:
A. How overdue is represented/determined.
B. How priority is determined in Clients.
C. Whether an existing task status update/complete API exists.

Then implement the frontend changes using the existing architecture.

==================================================
10. AFTER IMPLEMENTATION
==================================================

Before finishing, verify:

- [ ] Overdue tasks appear above pending tasks by default.
- [ ] Completed tasks are not treated as overdue.
- [ ] Task priority uses the same logic as the Clients page.
- [ ] HIGH / MEDIUM / LOW display correctly.
- [ ] Each non-completed task has a way to mark it COMPLETED.
- [ ] The completion action uses the existing API if available.
- [ ] No fake frontend-only completion is implemented if no backend update API exists.
- [ ] Search still works.
- [ ] Filter still works.
- [ ] Sort still works.
- [ ] Refresh still works.
- [ ] Pagination still works.
- [ ] Explicit user-selected sorting is respected.
- [ ] The page does NOT vertically scroll.
- [ ] The page does NOT horizontally scroll at normal desktop resolution.
- [ ] No other page has been modified.
- [ ] No backend code has been modified.

At the end, clearly tell me:
1. Which files you changed.
2. Whether any backend file was changed.
3. Which existing Clients priority logic you reused.
4. Which existing API/service is being used to mark tasks completed.
5. If no status-update API exists, explain exactly what is missing instead of changing the backend.
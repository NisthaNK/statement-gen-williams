# Client List Page — GitHub Copilot Prompts

## Prompt 1 — Create ClientList Structure

I am responsible ONLY for the Client List page of this React project.

STRICT FILE-SCOPE RULE:
You may create or modify files ONLY inside these two locations:
1. frontend/src/pages/ClientList/
2. frontend/src/components/components-ClientList/

DO NOT modify, create, delete, or rename anything anywhere else.
DO NOT touch:
- frontend/public/
- frontend/src/components/common/
- frontend/src/components/layout/
- frontend/src/constants/
- frontend/src/hooks/
- frontend/src/pages/ClientDetails/
- frontend/src/pages/Dashboard/
- frontend/src/pages/Login/
- frontend/src/routes/
- frontend/src/services/
- frontend/src/styles/
- App.js
- App.css
- index.js
- index.css
- package.json
- any other existing file or folder outside the two allowed locations.

First inspect the existing project structure and the already-created common components, but do not modify them.

Inside:
frontend/src/pages/ClientList/

create the files needed to assemble the Client List page, including:
- ClientList.jsx
- ClientList.css

Inside:
frontend/src/components/components-ClientList/

create reusable components needed specifically for this page, with their corresponding JSX and CSS files where appropriate.

Keep the Client List page modular. The main ClientList.jsx should assemble the smaller Client List-specific components rather than putting the entire UI into one huge file.

Use the existing common components from:
frontend/src/components/common/

where they are appropriate. Do not recreate common components such as Button, Card, or Table if suitable existing versions are already available.

Do not implement backend/API/database integration yet. Use dummy/mock data locally for the UI.

Do not modify routing yet. Do not modify App.js.

After creating the files, briefly explain which files you created and what responsibility each file has.

---

## Prompt 2 — Build Client List UI

Now implement the complete Client List page UI inside ONLY the files/folders I am responsible for:

ALLOWED LOCATIONS ONLY:
- frontend/src/pages/ClientList/
- frontend/src/components/components-ClientList/

STRICTLY DO NOT modify, create, delete, or rename anything outside these two locations.

DO NOT TOUCH:
- public/
- components/common/
- components/layout/
- constants/
- hooks/
- Dashboard/
- ClientDetails/
- Login/
- routes/
- services/
- styles/
- App.js
- App.css
- index.js
- index.css
- package.json
- any other file outside my two allowed folders.

The page should visually follow the provided Client List reference design.

PAGE PURPOSE:
This page is the RM's client-management page. After an RM logs in and opens Clients, they should see all clients assigned to that RM, ordered by priority.

Build the UI with React using the existing project architecture.

IMPORTANT:
Use the already-existing common components from frontend/src/components/common/ wherever suitable. Do NOT recreate common Button, Card, Table, or other shared components.

CLIENT LIST PAGE DESIGN:

1. PAGE HEADER
- Page title: "My Clients"
- Subtitle: "All clients assigned to you"
- Keep the header clean and professional.

2. TOP ACTION AREA
Create:
- Search input with search icon
- Search placeholder: "Search by name, ID or email"
- Filter button
- Sort button
- Refresh button

These controls should have proper hover/focus states.

For now, search/filter/sort can work against local dummy data. Do not connect to backend APIs.

3. CLIENT TABLE

Create a professional responsive table with columns:

- Priority
- Client Name
- Client ID
- Holdings (AUM)
- Products
- Next Action
- Action

Populate it with realistic dummy financial-client data.

Example clients:
- Amit Verma — C001
- Priya Shah — C002
- Neha Iyer — C003
- Vikram Mehta — C004
- Rahul Mehta — C005
- Sneha Kapoor — C006
- Karan Malhotra — C007

Use realistic AUM values such as:
₹18.75 Cr
₹12.40 Cr
₹10.10 Cr
₹8.80 Cr
₹6.45 Cr
₹5.30 Cr
₹4.75 Cr

Products should be numeric counts.

4. PRIORITY BADGES

Show priority visually as badges:
- HIGH
- MEDIUM
- LOW

Use appropriate visual hierarchy so HIGH is immediately noticeable, MEDIUM is distinguishable, and LOW is subtle.

Priority should be data-driven rather than hardcoded into the UI structure.

5. NEXT ACTION

Show examples such as:
- Portfolio Review
- FD Maturity
- —
etc.

6. VIEW CLIENT BUTTON

Each row should have a "View Client" button.

For now this button does NOT need to navigate to ClientDetails because routing is outside my allowed scope.

It can either:
- have a placeholder click handler, or
- log the selected client to the console.

Do not modify routes.

7. SEARCH

Implement client-side search using React state.

Search should filter by:
- Client Name
- Client ID
- Email

8. SORT

Implement a basic client-side sort control.

Allow sorting by useful fields such as:
- Priority
- Client Name
- Holdings (AUM)
- Number of Products

9. FILTER

Implement a basic client-side filter control.

At minimum allow filtering by:
- Priority: High / Medium / Low

Keep the implementation simple and clean so backend filtering can replace it later.

10. PAGINATION

At the bottom of the table show:
- current range / total clients
- page numbers
- previous button
- next button

Use local dummy data for pagination.

11. EMPTY STATE

If search/filter results contain no clients, show a professional empty state such as:
"No clients found"
with a short supporting message.

12. RESPONSIVE DESIGN

Make the page usable on:
- desktop
- laptop
- smaller screens

Do not introduce Bootstrap, Tailwind, Material UI, or any new UI framework/library.

Use the project's existing CSS approach.

13. VISUAL STYLE

The design should match the existing application's professional wealth-management dashboard aesthetic:
- clean white content area
- dark/navy application navigation provided by the existing layout
- blue primary actions
- subtle borders
- rounded cards/buttons
- professional typography
- appropriate spacing
- financial-dashboard style

Do not modify the existing Sidebar, Header, MainLayout, or any common layout components.

14. ARCHITECTURE

Keep responsibilities separated:

ClientList.jsx
→ page-level composition and state

ClientList-specific components
→ presentation and smaller UI sections

Use props to pass data and callbacks between components.

Keep the mock client data local to the Client List implementation for now.

Do not introduce backend calls.

15. IMPORTANT FINAL CHECK

Before finishing:
- Verify that every changed/created file is inside ONLY:
  frontend/src/pages/ClientList/
  frontend/src/components/components-ClientList/

If any change would require modifying another file, DO NOT make that change. Instead tell me what would be required later.

Do not modify routing or integration.

Finally, summarize:
1. files created/modified
2. components created
3. functionality implemented
4. anything intentionally left for later integration
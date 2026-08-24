Create a new Settings page for the existing React project.

IMPORTANT:
- ONLY create/modify files inside: frontend/src/pages/Settings/
- DO NOT modify, delete, rename, or move any existing files or folders outside Settings.
- DO NOT modify AppRoutes.jsx, App.js, CSS files outside Settings, package.json, or any existing components.
- Do not install Bootstrap, Material UI, Tailwind, or any other UI library.
- Use only React and normal CSS.
- Follow the existing project's coding style and naming conventions where possible.
- This is UI only for now. Do not implement backend/API functionality.

FOLDER STRUCTURE:
Create exactly this structure:

frontend/src/pages/Settings/
├── Settings.jsx
├── Settings.css
└── components/
    ├── ProfileSection.jsx
    ├── ChangePassword.jsx
    ├── SettingsSidebar.jsx
    └── [any small additional Settings-only components you genuinely need]

The Settings.jsx file must be the main assembly/container component. It should import and compose the components from the components folder.

UI REQUIREMENTS:
Build a professional banking/financial-dashboard Settings page matching this visual design:

1. OVERALL PAGE
- White/light background.
- Full-width page content.
- Clean corporate banking-dashboard aesthetic.
- Generous spacing and padding.
- Use a dark navy/blue color for important headings/navigation elements.
- Use subtle light-gray borders and very soft shadows.
- Rounded corners should be subtle, not excessive.
- Typography should look modern, clean and professional.
- The page should feel like an enterprise banking application.

2. PAGE HEADER
At the top of the Settings content:
- Large heading: "Settings"
- Directly below it, smaller muted subtitle:
  "Manage your profile and preferences"
- Keep the heading and subtitle aligned to the left.
- On the upper-right side of this area, show small notification/message-style icons and a user profile area.
- The user profile area should contain a small circular avatar, the name "Amit Verma", and the role "Relationship Manager" underneath/in smaller text.
- Include a small dropdown arrow beside the user information.
- Do not depend on external image URLs. If an avatar is needed, create a simple placeholder/avatar using CSS or an existing local asset only if one already exists inside Settings.

3. SETTINGS LAYOUT
Below the header, create a two-column settings layout:

LEFT:
A narrow vertical Settings navigation/sidebar.

RIGHT:
The main settings content area.

The left sidebar should contain these navigation items vertically:

- Profile
- Notifications
- Password
- Preferences
- Calendar
- Email Templates
- Data & Privacy

"Profile" should be the currently selected item.

The selected Profile item should have:
- very light blue background
- blue/dark-blue text
- subtle rounded corners
- clear visual distinction from the other items.

The other items should have a simple dark/gray text appearance and change appearance on hover.

4. PROFILE CONTENT
The main content area should contain two cards side-by-side.

CARD 1 — PROFILE INFORMATION:
Title:
"Profile Information"

Inside the card:
- Large circular professional-looking avatar/placeholder centered near the top.
- A blue/light-blue "Change Photo" button below the avatar.
- Then display profile information in a clean label/value format.

Use these example values:

Full Name: Amit Verma
Email: amit.verma@example.com
Phone: +91 98765 43210
Designation: Relationship Manager
Employee ID: RM000123
Department: Retail Banking
RM Team: North Zone

The labels should be smaller/muted and the values should be darker and more prominent.

CARD 2 — CHANGE PASSWORD:
Title:
"Change Password"

Include three password fields:
- Current Password
- New Password
- Confirm New Password

Each input should:
- have a clean white background
- subtle gray border
- rounded corners
- comfortable height/padding
- have an eye/visibility icon on the right side.

Below the fields add a primary blue button:
"Update Password"

For now this button does not need backend functionality. It can simply be a UI button.

5. VISUAL STYLE
The page should closely resemble a modern Standard Chartered-style corporate banking dashboard, but DO NOT copy proprietary logos, exact branding, or copyrighted assets.

Use:
- dark navy header/text accents
- blue primary buttons
- white cards
- very light gray page background
- light borders
- subtle shadows
- small rounded corners
- clean spacing
- professional typography.

6. RESPONSIVENESS
Make the Settings page responsive.

Desktop:
- sidebar on the left
- profile and password cards side-by-side.

Tablet/mobile:
- sidebar should become a horizontal/stacked navigation
- cards should stack vertically
- no horizontal overflow.

7. COMPONENT ARCHITECTURE
Keep responsibilities separated:

Settings.jsx:
- Main page/container.
- Assembles the SettingsSidebar, ProfileSection and ChangePassword components.
- Holds only minimal UI state if necessary.

SettingsSidebar.jsx:
- Renders the settings navigation items.
- Handles selected-item visual state locally if needed.
- Do not implement navigation to pages that don't exist yet.

ProfileSection.jsx:
- Renders the Profile Information card and its UI.

ChangePassword.jsx:
- Renders the Change Password card and its form UI.

Keep Settings-specific styling in Settings.css or CSS files inside the Settings folder only.

8. IMPORTANT
Do not modify any existing project files outside:
frontend/src/pages/Settings/

Do not change routing.
Do not change existing pages.
Do not change existing components.
Do not change global CSS.
Do not change package.json.
Do not install dependencies.

Before finishing, verify that all imports point only to files inside the new Settings folder or existing standard React functionality, and that the new Settings page can exist independently without breaking any existing page.


-----------------


After creating the Settings page, make ONLY the minimum required change in frontend/src/routes/AppRoutes.jsx to add a route for "/settings" that renders the <Settings /> component. Do not modify any other existing routes or logic.



------------------

Reuse the existing shared components already used in the project for the RM/user ID button, language selector button, and notification/bell icon. Do not create duplicate versions of these components and do not modify the existing shared components; simply import and use them in the Settings page.


------------------


Refactor ONLY the Settings page structure you just created. Do not change the UI design or functionality.

IMPORTANT ARCHITECTURE RULE:
Every React component must have its own dedicated CSS file. Never put a component's styling into a shared/global CSS file unless it is truly page-level layout styling.

Change the Settings folder to this structure:

frontend/src/pages/Settings/
├── Settings.jsx
├── Settings.css
└── components/
    ├── SettingsSidebar.jsx
    ├── SettingsSidebar.css
    ├── ProfileSection.jsx
    ├── ProfileSection.css
    ├── ChangePassword.jsx
    └── ChangePassword.css

Requirements:
1. Move all SettingsSidebar-specific styles into SettingsSidebar.css.
2. Move all ProfileSection-specific styles into ProfileSection.css.
3. Move all ChangePassword-specific styles into ChangePassword.css.
4. Keep only genuine page-level/layout styles in Settings.css, such as the overall Settings page container and the layout that positions the sidebar and content cards.
5. Update each JSX component to import its own CSS file.
6. Do NOT use inline styles.
7. Do NOT create a single large CSS file containing styles for all components.
8. Do NOT modify any files outside frontend/src/pages/Settings/ except the already-created Settings route/import in AppRoutes.jsx. Do not change that route; only leave it as it is.
9. Do not change the visual design or functionality that has already been created.
10. Do not create duplicate components or duplicate CSS.

IMPORTANT FOR ALL FUTURE WORK:
Follow component-level styling architecture throughout this project:
- Component.jsx → Component.css
- Page.jsx → Page.css
- If a page contains multiple components, each component gets its own CSS file.
- Parent/page CSS should contain only page-level layout styles.
- Never put a child component's styling into the parent's CSS file.
- Never use inline styles unless explicitly requested.
- Never create or modify global CSS for page/component-specific styling.
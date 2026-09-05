Redesign ONLY the existing Profile page UI to make it look much more polished, modern, and visually balanced.

IMPORTANT: Do NOT redesign the page from scratch and do NOT change its functionality. Use the existing Profile page implementation, data, API integration, components, routing, and existing layout as the foundation.

I want the final UI to be visually close to the attached/reference design in terms of:
- spacing
- proportions
- card styling
- typography hierarchy
- light blue/white WealthCore aesthetic
- subtle background decorations
- overall premium banking/wealth-management appearance

However, there are some IMPORTANT differences from the reference image:

1. THIS MUST REMAIN THE PROFILE PAGE
   - The page heading should remain "Profile".
   - Keep the existing Profile page purpose and content.
   - Do NOT turn it into a Settings page.
   - Do NOT add Settings-page functionality.

2. KEEP THE EXISTING SIDEBAR
   - Keep Dashboard
   - Keep Clients
   - Keep Products
   - Keep the existing Profile navigation item
   - Profile should remain the active/highlighted navigation item.
   - Keep Settings where it already exists in the sidebar.
   - Do not change the navigation routes or behavior.

3. DO NOT ADD A CHANGE PHOTO OPTION
   - Absolutely NO "Change Photo" button.
   - NO upload-photo functionality.
   - NO edit-photo functionality.
   - Keep the existing avatar/initials display exactly as a non-editable profile representation.

4. KEEP THE EXISTING PROFILE DATA
   Continue displaying the existing API-provided profile information such as:
   - Full Name
   - Phone
   - Email
   - Employee ID
   - Designation
   and any other fields that are already present on the Profile page.

   Do NOT rename API fields or change backend contracts.
   Do NOT hardcode profile data.

5. IMPROVE THE MAIN CONTENT AREA
   Instead of the current page looking very empty, create a better visual hierarchy.

   Keep the existing Profile Information content but present it inside a polished, large rounded card.

   The card should have:
   - a visually distinct avatar/initials section
   - Profile Information heading
   - a short subtitle
   - clean rows for each profile field
   - subtle dividers between fields
   - appropriate icons where they improve readability
   - comfortable padding and spacing
   - rounded corners
   - very subtle shadows/borders

6. ADD SUBTLE VISUAL ELEMENTS
   The page currently has too much empty white space.

   Add subtle decorative WealthCore-style elements such as:
   - very light blue abstract curves/shapes
   - soft background gradients
   - subtle geometric/wave elements
   - small professional accent elements

   These should remain VERY subtle and should never interfere with the profile information.

7. KEEP THE PAGE NON-SCROLLABLE
   This is IMPORTANT.

   The entire Profile page must fit within the viewport at normal desktop resolution.

   Do NOT introduce a vertical scrollbar.
   Do NOT make the main content internally scroll.
   Do NOT solve the design by simply increasing the page height.

   Use:
   - appropriate fixed/minimum heights
   - responsive spacing
   - flex/grid layouts
   - carefully sized cards
   so the complete Profile page fits cleanly in the viewport.

8. PRESERVE EXISTING HEADER/TOP BAR
   Keep the existing application header/top bar and its functionality.

   You may improve its spacing/alignment/visual polish if necessary, but do not change its behavior, routes, user information, language selector, etc.

9. API AND LOADING BEHAVIOR
   Do NOT modify the Profile API call or backend.

   Preserve the current loading behavior where API-dependent values can display "-" until the data arrives, if that is already how the page works.

10. DO NOT BREAK OTHER PAGES
   This task is ONLY for the Profile page and its directly associated styling/component files.

   Do NOT modify:
   - Dashboard
   - ClientList
   - ClientOverview
   - Products
   - backend
   - API contracts
   - shared components unless absolutely necessary

   If styling is currently in a Profile-specific CSS file, prefer modifying that file rather than creating unnecessary global styles.

11. RESPONSIVENESS
   Make the page work cleanly at the existing desktop viewport size used by the application.

   Avoid unnecessary horizontal or vertical scrolling.

12. CODE QUALITY
   - Reuse existing components where appropriate.
   - Do not duplicate existing components.
   - Keep the existing React structure and state/API logic intact.
   - Make the minimum necessary code changes for the UI redesign.
   - Do not introduce unnecessary dependencies.

VISUAL TARGET:

Think of the design as:
"Existing Profile page + premium WealthCore banking dashboard styling"

rather than:
"Replace my Profile page with a completely different page."

The final result should feel:
- clean
- professional
- spacious but NOT empty
- modern
- premium
- consistent with the existing Dashboard/Clients/Products pages
- clearly a Profile page

Before making changes, inspect the existing Profile page, its CSS/styles, and any components it uses. Reuse the current structure and data flow wherever possible.

After implementing, briefly tell me:
1. Which files were changed.
2. What UI changes were made.
3. Confirm that no API/backend functionality was changed.
4. Confirm that no Change Photo functionality was added.
5. Confirm that the Profile page remains non-scrollable.
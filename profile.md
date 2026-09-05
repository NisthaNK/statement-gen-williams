REDESIGN ONLY THE EXISTING PROFILE PAGE UI.

I want you to make the existing Profile page look as CLOSE AS POSSIBLE to the following exact visual design/reference:

- A premium WealthCore / Standard Chartered-style wealth-management Profile page.
- Large dark navy left sidebar.
- White/light header.
- Very light blue main background.
- Large "Hello, Anjali!" greeting area.
- Large rounded Profile Information card.
- Two-column card layout.
- Subtle pale-blue abstract curves/waves in the background.
- Clean navy typography.
- Blue accent color.
- Minimal, professional banking-dashboard appearance.
- No unnecessary empty space.
- No scrolling.

IMPORTANT:
You cannot see my reference image, so reproduce the visual structure described below as accurately as possible.

==================================================
1. OVERALL PAGE STRUCTURE
==================================================

The page should visually follow this structure:

--------------------------------------------------
LEFT SIDEBAR | TOP HEADER
             |
             | Hello, Anjali!
             | Here's your profile information
             |
             | -----------------------------------------
             | | LEFT PROFILE | PROFILE INFORMATION   |
             | |              |                       |
             | |    AS        | FULL NAME             |
             | |   avatar     | Anjali Sharma         |
             | |              | ----------------------|
             | |  decorative  | PHONE                 |
             | |   content    | 9900000002            |
             | |              | ----------------------|
             | |              | EMAIL                 |
             | |              | ...                   |
             | -----------------------------------------
             |
             | subtle background waves
--------------------------------------------------

The Profile Information card should be the main visual focus.

==================================================
2. SIDEBAR
==================================================

KEEP THE EXISTING SIDEBAR AND ITS FUNCTIONALITY.

It should contain the existing:
- Standard Chartered logo
- Dashboard
- Clients
- Products
- Profile
- Settings

Profile must remain the active/highlighted navigation item.

Do NOT:
- change routes
- change navigation behavior
- remove navigation items
- redesign the application navigation logic

Only improve visual spacing/styling if necessary to match the target design.

==================================================
3. HEADER
==================================================

KEEP THE EXISTING HEADER/TOP BAR AND ITS FUNCTIONALITY.

Maintain the existing:
- WealthCore branding
- Profile title
- language selector
- logged-in RM/user information
- existing controls

The header should remain clean, white, and compact.

Do not change any functionality.

==================================================
4. PROFILE PAGE HEADING
==================================================

Below the header, create a strong visual introduction.

Use:

"Hello, Anjali!"

with a large, bold navy heading.

Below it:

"Here's your profile information"

with a smaller muted-blue/gray subtitle.

The heading area should have comfortable spacing but should NOT consume excessive vertical space.

On the upper-right side of this area, add a subtle decorative WealthCore-style quote/accent similar to:

"Empowering
a more prosperous
tomorrow"

with a small blue underline/accent.

This is purely decorative and must not affect functionality.

==================================================
5. MAIN PROFILE CARD
==================================================

Create one large rounded white Profile Information card.

The card should be:
- wide
- horizontally centered
- moderately tall
- rounded
- subtly bordered/shadowed
- visually balanced
- NOT excessively tall
- NOT an empty giant rectangle

The card should have TWO clear columns.

LEFT COLUMN:
A visually distinct light-blue profile/identity area.

RIGHT COLUMN:
The actual Profile Information.

There should be a subtle vertical divider between the two sections.

==================================================
6. LEFT PROFILE SECTION
==================================================

The left section should contain the existing initials/avatar.

For example:

        AS

The avatar should be:
- large
- circular
- centered
- pale blue
- clean
- professional
- surrounded by a subtle border

IMPORTANT:

DO NOT ADD:
- Change Photo button
- Upload Photo
- Edit Photo
- Camera button
- Any photo-editing functionality

The avatar must remain NON-EDITABLE.

Below the avatar, add subtle non-functional decorative/profile text similar in visual style to:

"Building stronger
relationships for a brighter
financial future."

This is only to improve visual balance.

Do NOT add unnecessary buttons or functionality.

The left section should also have subtle pale-blue wave/curve decorations near the bottom.

==================================================
7. RIGHT PROFILE INFORMATION SECTION
==================================================

At the top:

Profile Information

Below it:

"Your personal and contact information on file"

Then display the existing API-provided profile fields.

The current fields should remain, including:

- Full Name
- Phone
- Email
- Employee ID
- Designation

Do NOT hardcode the values.

Continue using the existing API/data/state logic.

==================================================
8. PROFILE ROW STRUCTURE — VERY IMPORTANT
==================================================

EVERY profile field MUST use the EXACT SAME layout structure.

Use a consistent CSS Grid/Flexbox structure.

Each row should look conceptually like:

[ICON]    FULL NAME
          Anjali Sharma

[ICON]    PHONE
          9900000002

[ICON]    EMAIL
          anjali.sharma@wealthfirm.com

[ICON]    EMPLOYEE ID
          RM002

[ICON]    DESIGNATION
          Relationship Manager

Use:
- consistent icon container width
- consistent label position
- consistent value position
- consistent vertical alignment
- consistent row height
- consistent spacing
- subtle horizontal dividers

==================================================
9. FIX THE FULL NAME ALIGNMENT
==================================================

THIS IS A SPECIFIC BUG IN THE CURRENT UI.

The FULL NAME row is currently positioned/aligned differently from the other fields.

Fix it properly.

The Full Name row must:

- have its icon aligned exactly with the other field icons
- have "FULL NAME" aligned exactly with PHONE, EMAIL, EMPLOYEE ID, etc.
- have "Anjali Sharma" aligned exactly with the other values
- use the exact same CSS structure as every other profile row
- have the same spacing and vertical alignment as every other row

DO NOT fix this with:
- random margins
- negative margins
- absolute positioning
- one-off pixel offsets
- special CSS rules only for Full Name

Instead, create ONE reusable/common row layout and use it for ALL five fields.

==================================================
10. SPACING — VERY IMPORTANT
==================================================

The current page has too much empty space.

Do NOT stretch the profile rows across the entire height of the card.

Instead:

- Keep the Profile Information heading near the top.
- Keep the five rows grouped together.
- Give each row comfortable but compact spacing.
- Use subtle dividers.
- Keep the card visually filled without making it crowded.

The left avatar section and right information section should have roughly similar visual weight.

The card should look intentional and professionally designed, NOT like content floating inside a huge empty box.

==================================================
11. BACKGROUND
==================================================

The main page background should be very light, preferably white/light blue.

Add subtle decorative WealthCore-style abstract elements:

- pale blue curved shapes
- soft wave patterns
- subtle geometric curves

Use them mainly:
- behind the heading area
- near the bottom of the page
- around the profile card

They must be VERY subtle.

Do not let decorations interfere with text readability.

==================================================
12. FOOTER / LOWER AREA
==================================================

Use the remaining lower portion of the viewport for subtle branding/decorative content rather than leaving a huge blank white area.

A subtle bottom wave/curve can be used.

If existing WealthCore/Standard Chartered branding is already present in the application, preserve/reuse it rather than creating duplicate branding components.

==================================================
13. NON-SCROLLABLE — CRITICAL
==================================================

The Profile page MUST remain completely non-scrollable at the application's normal desktop viewport.

I do NOT want:
- vertical scrollbar
- horizontal scrollbar
- internally scrolling card
- page scrolling

Everything should fit naturally inside the viewport.

Use proper:
- flexbox
- grid
- viewport-aware heights
- controlled padding
- controlled margins
- card sizing

Do NOT simply shrink everything to an unreadable size.

==================================================
14. RESPONSIVENESS
==================================================

Keep the page responsive enough for the existing application.

However, prioritize the desktop layout currently used by this project.

Do not introduce unnecessary breakpoints or complicated responsive behavior.

==================================================
15. EXISTING DATA/API MUST NOT CHANGE
==================================================

This is a UI-only redesign.

DO NOT modify:
- API endpoints
- API calls
- backend
- DTOs
- response structures
- field names
- data mapping
- state management
- routing

The existing profile data must continue to come from the API.

If profile data is still loading and the current implementation displays "-" for unavailable values, preserve that behavior.

==================================================
16. DO NOT AFFECT OTHER PAGES
==================================================

ONLY modify files/components/styles required for the Profile page.

Do NOT modify:
- Dashboard
- ClientList
- ClientOverview
- Products
- backend
- other pages
- unrelated shared components

If the Profile page has its own CSS file, prefer modifying that instead of adding global CSS.

Do not introduce unnecessary dependencies.

==================================================
17. DO NOT ADD CHANGE PHOTO
==================================================

This is extremely important.

There must be NO:
- Change Photo button
- Upload Photo option
- Edit Photo option
- Camera icon/button
- photo picker
- photo upload functionality

The "AS" avatar/initials should simply be displayed.

==================================================
18. CODE QUALITY
==================================================

Before making changes:

1. Inspect the existing Profile JSX/component.
2. Inspect its CSS/style files.
3. Inspect how the existing profile data is loaded.
4. Preserve the existing data/API logic.
5. Refactor only the UI/layout/CSS necessary.

Use clean reusable structures.

In particular, create/use a consistent profile-row structure for:
- Full Name
- Phone
- Email
- Employee ID
- Designation

Do not create separate positioning logic for individual rows.

==================================================
FINAL VISUAL TARGET
==================================================

The final Profile page should feel as close as possible to this visual concept:

A premium banking dashboard with:

DARK NAVY SIDEBAR
        +
CLEAN WHITE HEADER
        +
LARGE "HELLO, ANJALI!" HEADING
        +
SUBTLE BLUE ABSTRACT BACKGROUND
        +
LARGE ROUNDED WHITE PROFILE CARD
        +
LEFT: LARGE "AS" AVATAR + DECORATIVE PROFILE AREA
        +
RIGHT: PROFILE INFORMATION + FIVE CLEAN DATA ROWS
        +
SUBTLE DIVIDERS + ICONS
        +
SUBTLE BOTTOM BRANDING/WAVES

It should look polished, balanced, modern and professional.

MOST IMPORTANT:
Do not merely rearrange the existing elements.

Actually refine the visual hierarchy, spacing, proportions, card design, typography, icons, background decoration and alignment so the result closely resembles the target design described above.

After implementation, tell me:

1. Which files you modified.
2. How you redesigned the Profile card.
3. How you fixed the Full Name alignment.
4. Confirm all profile fields now use the same row layout.
5. Confirm NO Change Photo functionality was added.
6. Confirm the page is non-scrollable.
7. Confirm no API/backend logic was changed.
8. Confirm no other pages were modified.
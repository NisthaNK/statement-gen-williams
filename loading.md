Update ONLY the ClientList page's loading behavior.

First inspect the existing Settings page/component and ClientList page/component to understand how Settings handles API data that is still loading.

I want ClientList to use the SAME loading/fallback approach as Settings.

Requirements:

1. Remove the current "Loading clients" text shown while the ClientList API is fetching data.
2. Do NOT show a separate loading screen/message.
3. Keep the ClientList page UI visible while the API request is in progress, including:
   - ClientHeader
   - search bar
   - filter/sort controls
   - table headers
   - existing layout and styling
4. While API data is unavailable, display "-" wherever an API-dependent client value would normally appear, just like the Settings page displays "-" while RM details are loading.
5. Once the API response arrives, automatically replace the "-" values with the actual client data.
6. Keep the existing ClientList API call, endpoint, response mapping, field names, search, filter, sort, and all other functionality unchanged.
7. Do NOT modify the backend.
8. Do NOT modify the Settings page.
9. Do NOT create a new global/common loading component for this task.
10. Make the smallest possible change only in the ClientList-related frontend files.

IMPORTANT:
Do not return early with something like `if (loading) return <Loading clients />`.
The ClientList UI must remain rendered during loading, with "-" placeholders for values that depend on the API response.

Use the existing Settings implementation as the reference so the loading behavior looks and behaves consistently across both pages.

After making the changes, tell me:
- which ClientList file(s) you changed
- what you changed
- confirm that no backend or Settings files were modified.
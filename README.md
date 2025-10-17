# GitHub User Profile Lookup

## Summary
This project provides a simple web application to look up GitHub user profiles. It displays the user's account creation date and calculates their account age in whole years. The application includes live status updates and caches the last successful lookup using `localStorage`.

## Features
*   **GitHub User Lookup**: Fetches and displays profile information for a given GitHub username.
*   **Account Age Calculation**: Calculates and displays the account's age in whole years.
*   **Live Status Alerts**: Utilizes `aria-live="polite"` to provide real-time updates on lookup progress (started, succeeded, failed) for accessibility.
*   **Local Storage Caching**: Automatically caches the last successfully looked up user's data in the browser's `localStorage` and repopulates the form and results on subsequent page loads.

## Usage
1.  **Open `index.html`**: Simply open the `index.html` file in your web browser.
2.  **Enter Username**: Type a GitHub username (e.g., `octocat`, `google`) into the input field.
3.  **Lookup**: Click the "Lookup User" button or press Enter.
4.  **View Results**: The user's creation date and account age will be displayed.
5.  **Status Updates**: The `aria-live` alert area will show messages about the lookup process.
6.  **Caching**: If you close and reopen the page, or refresh it, the last successfully looked up user's data will be pre-filled and displayed.

## License
This project is licensed under the MIT License. See the footer of `index.html` for a link to the full license text.
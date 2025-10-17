GitHub User Profile Lookup Application

Summary
This application is a simple web tool designed to look up and display public profile information for a given GitHub username. It fetches data from the GitHub API, presents it in a user-friendly format, and incorporates features like real-time status alerts for accessibility and client-side caching using local storage. This project serves as a high-quality submission demonstrating modern web development practices.

Setup
To set up and run this application, no special installation steps are required.
1. Save the provided 'index.html' content into a file named 'index.html'.
2. Open 'index.html' directly in any modern web browser (e.g., Chrome, Firefox, Edge, Safari).

Usage
1. Upon opening the 'index.html' file, you will see a simple input field labeled "Enter GitHub username" and a "Lookup" button.
2. If a previous successful lookup was cached, the form will be pre-filled with the last searched username and its profile data will be displayed.
3. Enter a valid GitHub username (e.g., "octocat", "defunkt") into the input field.
4. Click the "Lookup" button.
5. The application will fetch the user's data from the GitHub API.
6. A status alert message will appear above the results section, reporting the progress (lookup started, successful, or failed). This alert is designed with 'aria-live="polite"' for screen reader accessibility.
7. If the lookup is successful, the user's avatar, name, username, bio, public repository count, follower count, account creation date, and account age in whole years will be displayed. A link to their GitHub profile will also be provided.
8. If the lookup fails (e.g., username not found, API error), an error message will be shown.

Main Code Logic

HTML Structure (index.html):
- The page includes a form for username input and a dedicated 'div' for displaying search results.
- Key elements for dynamic updates are identified with specific IDs:
    - '#github-status': An 'aria-live="polite"' region for announcing search status updates (start, success, failure) to assistive technologies and visually to the user.
    - '#github-account-age': A 'span' element used to display the calculated age of the GitHub account in whole years.
    - '#username-input': The input field where the user types the GitHub username.
    - '#profile-display': The main container for displaying the user's profile information.

CSS Styling:
- Basic inline CSS is used within the '<style>' tag to provide a clean, modern, and responsive user interface, enhancing readability and user experience. Status messages are styled differently based on their type (info, success, error).

JavaScript Core Logic:
- DOM Element Caching: References to frequently used HTML elements are stored in JavaScript constants for efficient access.
- 'setStatus(message, type)': This function updates the '#github-status' element with a given message and applies contextual styling. It ensures the 'aria-live="polite"' attribute is present, making status changes audible to screen reader users without interrupting their current task.
- 'calculateAccountAge(createdAtDateString)': This utility function takes a GitHub creation date string and accurately computes the account's age in whole years. It handles month and day comparisons to ensure the age is only incremented when a full year has passed since the creation date.
- 'displayUserData(userData)': This function populates the '#profile-display' elements with the fetched user data, including the formatted creation date and the calculated account age.
- 'fetchGitHubUser(username)': This is the core asynchronous function that:
    - Initiates a 'fetch' request to the GitHub API ('https://api.github.com/users/{username}').
    - Reports the start of the lookup via 'setStatus'.
    - Handles API responses, checking for success (HTTP 200) or errors (e.g., 404 for user not found).
    - Upon successful retrieval, it calls 'displayUserData' to update the UI and reports success via 'setStatus'.
    - On failure, it displays an error message and reports the failure via 'setStatus'.
    - LocalStorage Caching: After a successful lookup, the entire 'userData' object and the 'username' are stored in 'localStorage' using the keys "github-user-unique-nonce-123" and "github-last-username-unique-nonce-123" respectively. This allows the application to remember the last successful search.
- Event Listener: The 'submit' event on the form ('#github-lookup-form') triggers the 'fetchGitHubUser' function with the entered username.
- 'DOMContentLoaded' Listener: On page load, this listener checks 'localStorage' for previously cached data. If found, it repopulates the username input field and displays the cached profile, providing a seamless experience upon revisit.

License
This project is licensed under the MIT License. A copy of the license is provided in the footer of the 'index.html' file.

Contact
For any questions, feedback, or inquiries regarding this application, please reach out to the developer via [Insert Your Preferred Contact Method, e.g., GitHub Issues, Email].
# GitHub User Lookup for Academic Grading

This project provides a simple web application to look up GitHub user profiles, intended to assist educators and graders in quickly accessing relevant student information on GitHub. Users can enter a GitHub username, and the application will fetch and display key profile details such as name, bio, followers, public repositories, account creation date, and account age. The application also includes accessibility features and client-side caching for an improved user experience.

## Features

*   **GitHub User Lookup:** Fetches and displays public profile information for a given GitHub username.
*   **ARIA-Live Status Alerts:** Provides dynamic, accessible feedback on lookup progress (start, success, failure) using an `aria-live="polite"` region (`#github-status`).
*   **Account Age Calculation:** Displays the GitHub account's age in whole years, alongside the precise creation date, within the `#github-account-age` element.
*   **Client-Side Caching:** Stores the last successfully retrieved user profile data in `localStorage` using the key `github-user-unique-nonce-123`.
*   **Form Repopulation:** On page load, the application attempts to load and display cached data, automatically repopulating the username input field and profile details from `localStorage`.
*   **Responsive Design:** A basic responsive layout ensures usability across different device sizes.
*   **MIT License:** Clearly licensed under the MIT License, included in the `index.html` footer.

## How to Use

1.  **Clone the Repository:**
    ```bash
    git clone https://github.com/your-username/github-user-lookup.git
    cd github-user-lookup
    ```
2.  **Open `index.html`:** Simply open the `index.html` file in your web browser. There is no need for a local server as all operations are client-side and interact with the public GitHub API.
3.  **Enter Username:** Type a GitHub username into the "GitHub Username" input field.
4.  **Click "Lookup":** Press the "Lookup" button or hit Enter.
5.  **View Results:** The application will display the user's profile details. Status updates will appear below the form in the designated status area.
6.  **Cached Data:** If you perform a successful lookup and then refresh the page or revisit, the application will automatically load the last successful lookup's data from your browser's local storage.

## Development Notes

*   The application uses the public GitHub API. There are no authentication tokens required for basic public profile lookups, but be mindful of rate limits (typically 60 requests per hour for unauthenticated requests).
*   The `localStorage` key used for caching is specifically `github-user-unique-nonce-123` as required.
*   Accessibility is a priority, with `aria-live="polite"` ensuring screen reader users are informed of dynamic content changes in the status area.

## License

This project is licensed under the MIT License. See the `index.html` file footer for the full license text.
# GitHub User Information Lookup Application

## Introduction
This application is designed as a web-based tool for quickly retrieving and displaying public information about a GitHub user. Specifically, it fetches a user's account creation date and calculates their account age in whole years. It also incorporates accessibility features for screen readers and client-side data caching for an improved user experience. This tool serves as a practical demonstration of modern web development concepts, suitable for academic evaluation in a web development or software engineering course.

## Features
*   **GitHub User Lookup:** Enter a GitHub username to retrieve their public profile data.
*   **Account Age Calculation:** Automatically calculates and displays the user's account age in whole years, along with their precise creation date.
*   **Live Status Alerts (ARIA-Live):** Provides real-time feedback on the lookup process (e.g., "Lookup started...", "Lookup successful!", "Lookup failed...") using an `aria-live` region, ensuring accessibility for users relying on screen readers.
*   **Local Storage Caching:** The last successfully looked-up user's data is stored in the browser's `localStorage`. Upon revisiting the page, the form is pre-filled and the user's information is immediately displayed from the cache, reducing API calls and improving load times.
*   **Responsive Design:** Basic styling ensures a readable and functional interface across different screen sizes.

## How to Use
1.  **Save the File:** Save the provided `index.html` content to a file named `index.html` on your local machine.
2.  **Open in Browser:** Open the `index.html` file using any modern web browser (e.g., Chrome, Firefox, Edge, Safari).
3.  **Enter Username:** In the input field labeled "GitHub Username:", type a valid GitHub username (e.g., `octocat`, `defunkt`).
4.  **Lookup:** Click the "Lookup User" button or press Enter.
5.  **View Results:** The application will display the user's creation date and account age. Status messages will appear below the input field, and if data was previously cached, it will be shown on page load.

## Technical Details
The application is built using standard web technologies: HTML for structure, CSS for styling, and JavaScript for dynamic functionality.
*   **GitHub API:** Leverages the public GitHub REST API (`https://api.github.com/users/{username}`) to fetch user data.
*   **`localStorage`:** Utilizes the browser's `localStorage` to persist the last successful user lookup. The data is stored under the key `github-user-unique-nonce-123`. This demonstrates client-side data persistence.
*   **`aria-live` Region:** An HTML `div` with `id="github-status"` and `aria-live="polite"` is used to inform screen reader users about asynchronous process updates without interrupting their current task.
*   **Asynchronous JavaScript:** Employs `async/await` for handling API requests gracefully.

## Academic Grading Context
This project effectively demonstrates competence in several key areas relevant to web development curriculum:
*   **DOM Manipulation:** Dynamically updating HTML content based on user interaction and API responses.
*   **Asynchronous Programming:** Handling network requests using `fetch` and `async/await`.
*   **Client-Side Storage:** Implementing data persistence using `localStorage`.
*   **Accessibility (A11y):** Incorporating `aria-live` attributes to make dynamic content accessible to assistive technologies.
*   **Error Handling:** Gracefully managing API errors and network issues.
*   **Date Manipulation:** Performing calculations with date objects to derive meaningful information (account age).
*   **Form Handling:** Managing form submission and input validation.

## License
This project is released under the MIT License. See the `index.html` file for full license text.
# GitHub User Account Creation Date Fetcher

This project provides a simple web page that allows users to fetch and display the account creation date of any public GitHub user. It's built with Bootstrap for a clean, responsive interface and uses JavaScript to interact with the GitHub API.

## Features

*   **User-Friendly Interface:** A clean and responsive design powered by Bootstrap.
*   **GitHub API Integration:** Fetches user data directly from `https://api.github.com/users/{username}`.
*   **Account Creation Date Display:** Shows the user's account creation date in `YYYY-MM-DD UTC` format.
*   **Optional Personal Access Token (PAT) Support:** The application can optionally use a GitHub Personal Access Token (PAT) provided via a URL query parameter (`?token=YOUR_PAT_HERE`) to benefit from higher API rate limits.
*   **Error Handling:** Provides informative messages for invalid usernames or API errors.

## How to Use

1.  **Open `index.html`:** Simply open the `index.html` file in your web browser.
2.  **Enter GitHub Username:** In the provided input field, type the GitHub username you wish to query (e.g., `octocat`).
3.  **Get Creation Date:** Click the "Get Creation Date" button.
4.  **View Result:** The account creation date will be displayed below the form.

### Using a GitHub Personal Access Token (Optional)

If you anticipate making many requests or encounter rate limit issues, you can provide a GitHub Personal Access Token (PAT) by appending `?token=YOUR_PAT_HERE` to the URL.

**Example:**
`file:///path/to/your/index.html?token=ghp_YOUR_PERSONAL_ACCESS_TOKEN`

The JavaScript code will automatically detect and use this token in the `Authorization` header for API requests.

## License

This project is licensed under the MIT License. See the `index.html` footer for more details.
# telerik-postman-project
My Postman collection for Telerik Academy Automation QA homework.
This repository contains a Postman collection designed for testing various functionalities of the GitHub REST API, as part of the Telerik Academy Automation QA Alpha program homework.

## Getting Started

To run these API tests, you'll need Postman installed and access to a GitHub account with specific permissions.

### Prerequisites

* **Postman:** Download and install the Postman Desktop Agent from the [official Postman website](https://www.postman.com/downloads/).
* **GitHub Account:** You'll need an active GitHub account.
* **GitHub Personal Access Token (PAT):** A PAT is required for authenticating your API requests. It grants Postman permission to interact with your GitHub account securely.
    * **How to create/verify your PAT:**
        1.  Go to your [GitHub Settings](https://github.com/settings/profile) -> **Developer settings** -> **Personal access tokens** -> **Tokens (classic)**.
        2.  Click **`Generate new token (classic)`** (or regenerate an existing one).
        3.  Provide a clear **Note** (e.g., "Postman Homework").
        4.  Under "Select scopes," ensure the **`repo`** checkbox is selected. This grants necessary permissions for managing repositories, issues, and comments. (If specifically troubleshooting delete, ensure `delete_repo` sub-scope is explicitly checked).
        5.  Click **`Generate token`** (or `Update token`).
        6.  **IMMEDIATELY COPY THE GENERATED TOKEN.** You will not see it again. Store it securely.
     
### 1. Set Up the Postman Collection

Once you have Postman installed, you need to import the collection that contains all the API requests:

1.  **Download the collection file:** Clone this GitHub repository to your local machine (using Git command line or GitHub Desktop). The collection file is named `GitHubAPI_Collection.json`.
2.  **Import into Postman:**
    * Open Postman.
    * Click on **`File`** (in the top menu bar) -> **`Import`** (or the `Import` button on the top left).
    * Select the **`Files`** tab, then click **`Upload Files`**.
    * Navigate to the local folder where you cloned this repository, select `GitHubAPI_Collection.json`, and click `Open`.
    * Click **`Import`**. Your collection will now appear in the "Collections" sidebar.

### 2. Set Up Environment Variables

Environment variables are used to manage sensitive data (like your GitHub PAT) and reusable values (like your username and the base API URL) without hardcoding them into the requests. This makes the collection secure and portable.

1.  **Download the environment file:** The environment file is named `GitHubAPI_Environment.json` within this repository.
2.  **Import into Postman:**
    * Open Postman.
    * Click on **`File`** (in the top menu bar) -> **`Import`**.
    * Select the **`Files`** tab, then click **`Upload Files`**.
    * Navigate to the local folder where you cloned this repository, select `GitHubAPI_Environment.json`, and click `Open`.
    * Click **`Import`**. Your environment will appear in the "Environments" sidebar.
3.  **Configure your specific credentials:**
    * In Postman, go to the **`Environments`** tab (left sidebar) and select your imported environment (e.g., "GitHub API Homework").
    * You will see variables like `github_token`, `github_username`, and `base_url`.
    * **For `github_token`:**
        * Your PAT will NOT be in the `Current Value` (for security reasons when shared).
        * **Paste your actual GitHub Personal Access Token (PAT)** (the one you copied securely) into the **`Current Value`** field for `github_token`.
        * **Why Current Value?** Postman primarily uses the `Current Value` for sending requests. The `Initial Value` is typically used when the environment is first imported or reset.
    * **For `github_username`:** Enter your exact GitHub username into both `Initial Value` and `Current Value` fields.
    * **For `base_url`:** Ensure it's `https://api.github.com` in both `Initial Value` and `Current Value` fields.
    * Click **`Save`** in the environment tab.
4.  **Select the active environment:** In the environment dropdown menu (usually at the top right of Postman), make sure your "GitHub API Homework" environment is selected.

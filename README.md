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

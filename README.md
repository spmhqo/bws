# Blog Writing Studio

A single-file, browser-based writing workspace for the **Online
Marketing & Sales Education** programme.

The app contains a 144-topic publication list and combines topic
selection with a Bengali educational blog-writing prompt based on Prompt
Version 2.0.

## Features

-   Browse and search all 144 publication topics.
-   Filter topics by educational stage, original module, and completion
    status.
-   Automatically populate the prompt inputs when a topic is selected.
-   Edit topic inputs before generating the prompt.
-   Generate and copy a complete blog-writing prompt.
-   Download an individual prompt as a `.txt` file.
-   Mark topics as pending or completed.
-   Keep notes for individual topics.
-   Export and import a JSON backup of saved progress and edited inputs.
-   Responsive layout for desktop and mobile screens.
-   Works locally in a modern browser without a backend or installation.

## Files

Recommended repository structure:

``` text
blog-writing-studio/
├── index.html
├── spm.ico
└── README.md
```

-   `index.html` --- the complete application, including its HTML, CSS,
    JavaScript, topic data, and writing prompt.
-   `spm.ico` --- optional favicon referenced by the HTML page.
-   `README.md` --- this project guide.

If you do not have `spm.ico`, either add the favicon file or remove this
line from the `<head>` section of `index.html`:

``` html
<link rel="icon" href="spm.ico">
```

## Run locally

1.  Download or clone this repository.
2.  Open `index.html` in a modern web browser.
3.  Select a publication topic from the topic list.
4.  Review or edit the automatically populated inputs.
5.  Select **Prompt তৈরি করুন** or **সম্পূর্ণ Prompt Copy**.
6.  Paste the generated prompt into ChatGPT or another compatible AI
    writing assistant.

No build step, package manager, server, or API key is required for local
use.

## Publish with Cloudflare Pages

This is a static HTML application and can be deployed using Cloudflare
Pages.

1.  Push the repository to GitHub.
2.  In the Cloudflare dashboard, open **Workers & Pages**.
3.  Choose **Create application** and select **Pages**.
4.  Connect the GitHub repository.
5.  For a plain HTML project, use the following settings:
    -   **Framework preset:** None
    -   **Build command:** Leave blank
    -   **Build output directory:** `/` (the repository root)
6.  Deploy the project.
7.  After deployment, use the Cloudflare Pages URL or connect a custom
    domain.

Make sure the main file is named `index.html` and is located in the
repository root.

## Data storage and backups

The app stores its progress, notes, and edited topic inputs in the
browser's **Local Storage**.

This means:

-   Saved information is associated with the browser and device being
    used.
-   It does not automatically sync between different browsers or
    devices.
-   Clearing browser site data may erase the saved information.
-   Opening the deployed app on another device starts with that device's
    own local data.

Use **Backup Export** regularly to download a JSON backup. Use **Backup
Import** to restore that backup in the app.

Keep backup files somewhere safe. The app does not upload your notes or
progress to a server.

## Important content note

The current application includes all 144 topic titles. Some topic
descriptions, learning objectives, and previous/next-topic relationship
text were reconstructed as concise working summaries when this first app
version was assembled. They should not be treated as verbatim copies of
the complete, stage-approved Master Topic Input Register.

Before using the app as the definitive production source, replace or
verify those fields against the full approved register.

## Privacy and security

-   The application does not require an account.
-   No backend database is included.
-   Progress and notes are stored locally in the browser.
-   Do not assume Local Storage is a secure place for passwords, payment
    details, or other sensitive information.

## Customisation

The application is intentionally packaged as one HTML file. Topic data,
prompt text, styles, and application logic are included in `index.html`.

When editing the application:

-   Keep the main file named `index.html` for static hosting.
-   Preserve the topic publication numbers and original module IDs.
-   Test topic selection, prompt generation, backup export, and backup
    import after changes.
-   Export a backup before clearing browser data or replacing the
    application.

## Licence

No licence is specified. Add a `LICENSE` file if you intend to publish
the project with explicit reuse or distribution permissions.

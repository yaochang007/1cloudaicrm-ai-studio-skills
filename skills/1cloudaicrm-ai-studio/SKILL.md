---
name: 1cloudaicrm-ai-studio
description: Work on 1CloudAI CRM AI Studio projects through the builder, using direct code editing or precise AI Studio prompts. Use when creating, inspecting, changing, or previewing an AI Studio project.
---

# 1CloudAI CRM AI Studio

Use the logged-in 1CloudAI CRM AI Studio project specified by the user. Confirm the project and its current state before editing. The builder may be embedded in a cross-origin frame, so use an available browser integration or computer-use interface that can reach the visible editor; do not bypass access controls. Treat starred projects as templates: clone them before editing unless the user specifically directs otherwise.

## Choose an editing method

- **Direct code editing:** For a precise change, open the code (`</>`) view, inspect the existing file, routes, and related configuration, then edit the relevant code. Preserve working behavior and verify the saved result in Preview. If working from an exported copy, local edits do not update the builder automatically; use a supported import or the builder editor and verify the actual project.
- **AI Studio prompt:** Use the builder chat for broad generation or when direct editing is unavailable. Describe the outcome, exact file and route if known, relevant constraints, and what should remain unchanged. Ask it to report the files changed. Inspect its changes using the history item's Details and verify them in Preview. For example:

  > Update the page at `<route>`, implemented in `<file>`, to `<desired behavior>`. Keep the existing styling and other routes intact. Report the files changed and any assumptions.

  Replace the placeholders with observed details; don't invent file names or routes. A React client-side route may exist even if the builder's page selector does not list it; inspect the router or open the route directly.

## Check and release

1. Inspect the current Preview and, when useful, history and Details for the last working version.
2. Make a scoped change and save it. Use history and Revert to recover from a damaging generated change when appropriate.
3. Check the affected behavior and relevant desktop and mobile layouts in Preview. Report what was tested and any limitations.
4. Publish or update the live site only when authorized by the user. Check the published site after publishing. For external review, use a published preview URL if available, not an internal editor URL.

## Assets and credentials

The project image uploader may accept only images; use a supported media-storage workflow for other asset types and verify the resulting URL before using it. Never put passwords, API keys, or private data into frontend code, prompts, screenshots, or public repositories. Use a server-side integration for secrets and confirm access before changing live data or services.

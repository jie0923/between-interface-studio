# Project Between: Handoff Bundle (Backend Task)

This bundle contains the finalized high-fidelity landing page for **Between Interface Studio**. The design is complete and utilizes a "Linear-inspired Modern Minimal" aesthetic with fluid animations and glassmorphism.

## Instructions for Gemini CLI (Backend Agent)

### 1. Scope & Constraints
- **Goal:** Implement a backend to capture and store form submissions.
- **Visual Integrity:** **DO NOT** modify any markup, styles, layout, or class names in `index.html`. All existing CSS and layout structures must remain untouched.
- **Logic ONLY:** You are only allowed to add `onSubmit` handler logic, local state management (if needed), and `fetch()` calls within the existing `<script>` tag in `index.html`.
- **Storage:** Use a local `submissions.json` file or a local SQLite database to store form data. Do **not** use external databases or APIs.
- **Localhost:** Ensure the landing page and its backend can be run together on `localhost`.

### 2. Implementation Steps
1. Read the folder structure and understand the current `index.html`.
2. Create a minimal Node.js/Express (or similar) server to serve the static files and handle the POST request to `/api/submit`.
3. In `index.html`, update the `form.addEventListener('submit', ...)` block to:
   - Capture form data using `FormData`.
   - Send the data to your backend endpoint using `fetch`.
   - Handle the response and toggle the success state (`#success-state`).
4. Ensure the backend correctly appends submissions to `submissions.json`.

### 3. Folder Structure
- `index.html`: The canonical entry point and frontend code.
- `submissions.json`: (To be created) Storage for form entries.
- `server.js`: (To be created) Your backend implementation.

---

**Note to User:**
The frontend has been meticulously crafted to represent your "Translator" persona. The backend agent should strictly focus on functionality without disturbing the "Between" aesthetic.

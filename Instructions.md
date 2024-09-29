# Personal Journal App - User Stories

## Authentication & Authorization
1. **As a user**, I want to create an account by providing a unique username, email, and password so that I can access the journal app securely.
   - **Acceptance Criteria:**
     - Users can register with a valid email and password.
     - Passwords are securely hashed before being stored in the database.
     - Users should receive feedback if the email is already registered or if the password is too weak.

2. **As a user**, I want to log in with my email and password so that I can access my personal journal entries.
   - **Acceptance Criteria:**
     - Users can log in with their email and password.
     - The app should display an error message if the login credentials are incorrect.

3. **As a user**, I want to log out so that I can protect my account from unauthorized access.
   - **Acceptance Criteria:**
     - Users can log out by clicking a “Log Out” button.
     - After logging out, users should be redirected to the login page.

4. **As a user**, I want to stay logged in across sessions so that I don’t have to log in every time I visit the app.
   - **Acceptance Criteria:**
     - Users remain logged in until they log out explicitly (use session-based authentication or JWT tokens).
     - Expired sessions should automatically log users out and redirect them to the login page.

5. **As a user**, I want to reset my password if I forget it so that I can regain access to my account.
   - **Acceptance Criteria:**
     - Users can request a password reset link to be sent to their email.
     - Users can update their password through the link and successfully log in again.

## Journal Entries
6. **As a user**, I want to create a new journal entry by providing a title, content, and optional date so that I can record my thoughts.
   - **Acceptance Criteria:**
     - Users can create a new entry with a title, content, and optional date.
     - Entries should be stored in MongoDB and associated with the logged-in user.
     - The app should confirm the entry was successfully saved and display it in the journal list.

7. **As a user**, I want to view a list of all my journal entries so that I can easily browse through them.
   - **Acceptance Criteria:**
     - Users can view a list of all their journal entries on the main page.
     - Only entries belonging to the logged-in user should be displayed.
     - Each entry should show the title and a preview of the content.

8. **As a user**, I want to search for journal entries by title or content so that I can quickly find a specific entry.
   - **Acceptance Criteria:**
     - Users can type in a search bar to filter journal entries by title or content.
     - The filtered results should update dynamically based on the search query.

9. **As a user**, I want to click on a journal entry to view its full content so that I can read the details.
   - **Acceptance Criteria:**
     - Users can click on a journal entry from the list to view it in full detail on a separate page.

10. **As a user**, I want to edit an existing journal entry so that I can update its title, content, or date.
    - **Acceptance Criteria:**
      - Users can click an “Edit” button to update the title, content, and date of an existing entry.
      - After saving the changes, the updated entry should be displayed in the journal list.

11. **As a user**, I want to delete a journal entry so that I can remove it permanently if I no longer need it.
    - **Acceptance Criteria:**
      - Users can click a “Delete” button to permanently remove an entry.
      - The app should ask for confirmation before deleting the entry.
      - Once deleted, the entry should no longer appear in the journal list.

12. **As a user**, I want my journal entries to be organized by date so that I can view them chronologically.
    - **Acceptance Criteria:**
      - The journal entries should be sorted by date, with the most recent entries displayed first.

## User Experience
13. **As a user**, I want to receive feedback when I create, edit, or delete an entry so that I know the action was successful.
    - **Acceptance Criteria:**
      - Success messages should be shown after actions like creating, editing, or deleting an entry.
      - Error messages should appear if any operation fails (e.g., saving to the database).

14. **As a user**, I want the app to have a clean and simple interface so that I can focus on writing and reading my journal entries.
    - **Acceptance Criteria:**
      - The UI should be intuitive and user-friendly.
      - There should be clear buttons for actions like creating, editing, and deleting entries.

## Data Security
15. **As a user**, I want my data to be stored securely in the database so that unauthorized users cannot access my journal entries.
    - **Acceptance Criteria:**
      - Journal entries should be stored in MongoDB and associated with the logged-in user.
      - Only authenticated users should have access to their own entries.

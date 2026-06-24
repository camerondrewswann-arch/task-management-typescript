# Task Management App with TypeScript

A React + TypeScript task management application that demonstrates task CRUD features, typed React state, Context API global state, form validation, error handling, React Router pages, and Auth0 authentication.

## Features

- Task dashboard with task cards and status filter
- Create, edit, delete, and view task details
- Task details page for individual task information
- TypeScript interfaces and type aliases for task data, form data, validation errors, and Auth0 user data
- Typed `useState` hooks in forms and context
- Context API global task state through `TaskProvider`
- Custom typed hook: `useTasks`
- Auth0 login/register button and logout button
- Protected profile page using Auth0 authentication
- LocalStorage persistence so tasks remain after refresh
- Form validation and user-friendly error messages
- Responsive CSS styling

## Tech Stack

- React
- TypeScript
- Vite
- React Router DOM
- Auth0 React SDK
- Context API
- CSS

## Project Structure

```txt
src/
  components/
    Navbar.tsx
    ProtectedRoute.tsx
    TaskCard.tsx
    TaskForm.tsx
  context/
    TaskContext.tsx
  hooks/
    useTasks.ts
  pages/
    CreateTask.tsx
    Dashboard.tsx
    EditTask.tsx
    NotFound.tsx
    Profile.tsx
    TaskDetails.tsx
  types/
    auth.ts
    task.ts
  utils/
    sampleTasks.ts
    validation.ts
  App.tsx
  main.tsx
  styles.css
```

## Setup Instructions

1. Clone the repository:

```bash
git clone https://github.com/YourName/task-management-typescript.git
cd task-management-typescript
```

2. Install dependencies:

```bash
npm install
```

3. Create your environment file:

```bash
cp .env.example .env
```

4. Add your Auth0 credentials inside `.env`:

```env
VITE_AUTH0_DOMAIN=your-auth0-domain.us.auth0.com
VITE_AUTH0_CLIENT_ID=your-auth0-client-id
VITE_AUTH0_CALLBACK_URL=http://localhost:5173
```

5. In Auth0, add this URL to **Allowed Callback URLs**, **Allowed Logout URLs**, and **Allowed Web Origins**:

```txt
http://localhost:5173
```

6. Start the app:

```bash
npm run dev
```

7. Open the local URL shown in the terminal, usually:

```txt
http://localhost:5173
```

## Available Scripts

```bash
npm run dev
```

Starts the development server.

```bash
npm run build
```

Checks TypeScript and creates a production build.

```bash
npm run preview
```

Previews the production build locally.

## Main Pages

### Dashboard

The dashboard displays all tasks, task stats, filtering by status, and action buttons for details, editing, and deletion.

### Task Details

The task details page shows the selected task's title, description, status, priority, due date, created date, and updated date.

### Create and Edit Pages

The create and edit pages use a reusable `TaskForm` component with typed form state and validation.

### Profile Page

The profile page is protected by Auth0. Users must log in before viewing their Auth0 profile information.

## TypeScript Implementation Details

The application uses TypeScript interfaces and type aliases in `src/types/task.ts`:

- `Task`
- `TaskStatus`
- `TaskPriority`
- `TaskFormData`
- `TaskValidationErrors`

These types enforce consistent data shapes across components, context, hooks, and validation functions.

## State Management

Global task state is managed in `TaskContext.tsx` using React Context API. Components access task state and task actions through the custom `useTasks` hook.

## Validation and Error Handling

Task form validation is handled in `src/utils/validation.ts`. The form checks for required title, description, and due date fields. Validation errors are displayed directly below each input.

## Submission Notes

Submit the root GitHub repository URL in Disco. Also upload the demo video directly to Disco, not through Google Drive or another external link.

# Presentation Script: Task Management App with TypeScript

Hello, my name is Cameron, and this is my Task Management Application built with React and TypeScript.

The goal of this project was to create a task management tool that uses TypeScript for type safety, React Router for navigation, Context API for global state, and Auth0 for authentication and authorization.

First, this is the task dashboard. The dashboard shows a list of tasks, including each task's title, description, status, priority, and due date. At the top, I included summary cards that show how many tasks are in To Do, In Progress, and Completed. I also added a filter so users can view all tasks or only tasks with a specific status.

Next, I can create a new task. This form uses TypeScript types to control the shape of the task data. The form includes a title, description, status, priority, and due date. I also added validation and error handling, so if a user leaves required fields blank or enters too little information, the app displays helpful error messages.

After creating a task, it appears on the dashboard. From each task card, I can open the details page. The task details page shows more complete information, including when the task was created and last updated.

I can also edit a task. The edit page reuses the same typed form component as the create page, but it loads the existing task data first. After I save the changes, the task updates in the global state and on the dashboard.

The app also supports deleting tasks. When I click delete, the task is removed from the task list. Tasks are stored in localStorage, so the data remains after refreshing the browser.

For state management, I used React Context API with TypeScript. The TaskProvider stores the global task list and provides functions for adding, updating, deleting, filtering, and finding tasks by ID. I also created a custom typed hook called useTasks so components can safely access the task context.

For authentication, I integrated Auth0. The navigation includes login and registration through Auth0, plus logout functionality. I also added a protected profile page. Users must be logged in before they can view their profile information.

Overall, this project demonstrates React, TypeScript, typed state management, reusable components, routing, validation, error handling, protected pages, and Auth0 authentication. Thank you for watching my demo.

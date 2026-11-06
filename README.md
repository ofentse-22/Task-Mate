# TaskMate

TaskMate is a lightweight task manager built with React. Organize everyday tasks by category, set priorities and due dates, and keep your progress saved in your browser.

## Features

- Add tasks with a category, priority, and optional due date.
- Edit task names, mark tasks complete, or delete them.
- Search task names and categories.
- Filter the list to show all, active, or completed tasks.
- See task totals and a live completion progress bar.
- Spot overdue tasks at a glance and clear completed tasks in one action.
- Keep tasks between visits with browser `localStorage`; existing TaskMate tasks are retained when the app is upgraded.
- Use a responsive interface with keyboard focus indicators and reduced-motion support.

## Requirements

- Node.js 16 or newer
- npm (included with Node.js)

## Get started

1. Clone the repository and open its directory:

   ```sh
   git clone <repository-url>
   cd taskmate
   ```

2. Install dependencies:

   ```sh
   npm install
   ```

3. Start the development server:

   ```sh
   npm start
   ```

   Open [http://localhost:3000](http://localhost:3000) in your browser.

## Use TaskMate

1. Enter a task, choose a category and priority, and optionally select a due date.
2. Select **Add task**. Use **Edit** to rename a task, its checkbox to change completion status, or **Delete** to remove it.
3. Search by task name or category, or use **All**, **Active**, and **Done** to filter the list.
4. Choose **Clear completed** to remove all completed tasks.

Tasks are stored locally in the current browser profile. They are not synced between devices or shared with a server. Clearing browser site data removes saved tasks.

## Scripts

| Command | Description |
| --- | --- |
| `npm start` | Run the development server. |
| `npm test -- --watchAll=false` | Run the test suite once. |
| `npm run build` | Create an optimized production build in `build/`. |

## Project structure

```text
src/
  App.jsx                 App state, filtering, and local persistence
  App.test.jsx            Component and task-flow tests
  components/
    StatsBar.jsx          Counts and completion progress
    TodoForm.jsx          New-task form
    TodoItem.jsx          Task details and actions
    TodoList.jsx          Task list and empty state
  styles.css              Responsive application styles
```

## Troubleshooting

- If the app does not start, check that Node.js and npm are installed, then run `npm install` again.
- If saved tasks do not appear, use the same browser profile and origin where they were created. Browser storage is isolated by both.
- If a production build reports lint or compilation errors, fix those errors and rerun `npm run build`.

## Built with

React, Create React App, and the Testing Library.

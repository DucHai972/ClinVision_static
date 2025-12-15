# Static Frontend Build

This directory contains a standalone static version of the frontend, suitable for hosting on GitHub Pages or any static file server.

## How it works
- **Authentication**: Bypassed using a mock implementation. The user is logged in as a Guest.
- **Data**: Uses mock data for sessions and users, as there is no backend connection.
- **Routing**: Uses `HashRouter` (URLs look like `/#/dashboard`) to ensure compatibility with static hosting.

## Deployment
1. Upload the contents of this folder to your web server or GitHub repository.
2. If using GitHub Pages, configure it to serve from this root.

## Re-building
To regenerate this build, run from the `frontend` directory:
```bash
npx vite build -c vite.config.static.ts
```
Then rename `index-static.html` to `index.html` (if not done automatically).

# gh_pages_react

A React application migrated from Create React App (CRA) to **Vite** for faster development, cleaner dependency management, and improved performance.

This project uses:

- React 18
- Vite
- Vitest
- GitHub Pages deployment
- GitHub Actions CI
- Branch protection + PR workflow

## Development URL

Local development server:

```text
http://localhost:5173/gh_pages_react/
```

Production GitHub Pages:

```text
https://<your-github-username>.github.io/gh_pages_react/
```

---

## Project Setup

Clone the repository:

```bash
git clone <repo-url>
cd gh_pages_react
```

Install dependencies:

```bash
npm install
```

---

## Available Scripts

### Start development server

```bash
npm start
```

Runs the Vite development server.

Open:

```text
http://localhost:5173/gh_pages_react/
```

The page automatically reloads when changes are made.

---

### Run tests

```bash
npm test
```

Runs Vitest:

```bash
vitest --run
```

---

### Create production build

```bash
npm run build
```

Builds optimized production assets into:

```text
dist/
```

---

### Preview production build locally

```bash
npm run preview
```

Starts a local preview server using the production build.

---

### Deploy to GitHub Pages

```bash
npm run deploy
```

Deployment process:

```text
npm run build
↓
creates dist/
↓
gh-pages publishes dist/
```

---

## Continuous Integration

GitHub Actions automatically validates:

- dependency installation
- tests
- production build

Workflow:

```text
.github/workflows/ci.yml
```

CI triggers:

- Push to `main`
- Pull requests to `main`
- Manual workflow execution

---

## Branch Protection

Recommended repository settings:

- Require pull requests before merge
- Require status checks to pass
- Require branches to be up to date

Required check:

```text
build-test
```

---

## Project Structure

```text
src/
  App.jsx
  App.test.jsx
  index.jsx
  App.css
  index.css
  setupTests.js

index.html
vite.config.js
```

---

## Migration Notes

This project was migrated from:

```text
Create React App
```

to:

```text
Vite
```

Key changes:

- removed `react-scripts`
- replaced webpack dev server
- moved `public/index.html` → root `index.html`
- renamed JSX files to `.jsx`
- switched build output from `build/` → `dist/`
- migrated tests to Vitest
- updated GitHub Pages deployment

---

## Notes

Ignored generated folders:

```text
/node_modules
/dist
/.vite
/coverage
```

This keeps Git history clean and avoids committing generated files.
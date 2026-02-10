# Todo App

A simple todo list app built with React and Base44 backend.

## Structure

```
base44/               # Backend configuration
├── config.jsonc      # Project settings
└── entities/         # Data schemas
    └── task.jsonc    # Task entity

src/                  # Frontend code
├── App.jsx           # Main todo app
├── api/              # Base44 client
├── components/ui/    # UI components
└── lib/              # Utilities
```

## Quickstart

Download as ZIP-file. 

```bash
npm install           # Install packages
base44 login          # Authenticate
base44 link           # Create new app
```

Set your new AppID

* /base44/.app.jsonc
* /src/api/base44Client.js

```bash
npm run build         # Build html, css, js
base44 entities push  # Push entity schemas
base44 deploy         # Deploy backend + hosting
```

Open Browser

* https://app.base44.com/apps/{yourAppId}/editor/workspace/overview  - [x] require login to access
* https://{yourAppURI}.base44.app/login - for login

## Development

```bash
npm install
npm run dev
```

## Commands

| Command | Description |
|---------|-------------|
| `npm run dev` | Start dev server |
| `npm run build` | Build for production |
| `npm run preview` | Preview production build |

## Base44 CLI

```bash
base44 login          # Authenticate
base44 link           # Create new app
base44 entities push  # Push entity schemas
base44 deploy         # Deploy backend + hosting
```

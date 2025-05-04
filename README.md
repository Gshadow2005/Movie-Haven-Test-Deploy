# Movie Haven

[Testing](https://gshadow2005.github.io/Movie-App-Frontend-Deploy/))

Movie Haven is a web application built with **React, TypeScript, and Vite** for the frontend, and a backend deployed using **AWS and Vercel**.

## Tech Stack

- **Frontend**: React + TypeScript + Vite
- **Backend**: AWS (EC2, RDS) + Vercel
- **Database**: PostgreSQL (Neon Database)

## Features

- Browse and search for movies
- View detailed movie information
- Responsive UI for seamless experience

## Development Setup

### Install Dependencies
```sh
npm install
```

### Start Development Server
```sh
npm run dev
```

## Deployment
The project is deployed using **AWS and Vercel**. The frontend is hosted on **Vercel**, while the backend is hosted on **AWS EC2** with **PostgreSQL on Neon Database**.

## ESLint Configuration
For production applications, we recommend enhancing the ESLint configuration.

### Type-Aware Rules
Update `parserOptions` in the top-level ESLint config:
```js
export default tseslint.config({
  languageOptions: {
    parserOptions: {
      project: ['./tsconfig.node.json', './tsconfig.app.json'],
      tsconfigRootDir: import.meta.dirname,
    },
  },
})
```

Replace `tseslint.configs.recommended` with `tseslint.configs.recommendedTypeChecked` or `tseslint.configs.strictTypeChecked`.

### React ESLint Plugin
Install and configure `eslint-plugin-react`:
```sh
npm install eslint-plugin-react --save-dev
```

Update `eslint.config.js`:
```js
import react from 'eslint-plugin-react';

export default tseslint.config({
  settings: { react: { version: '18.3' } },
  plugins: { react },
  rules: {
    ...react.configs.recommended.rules,
    ...react.configs['jsx-runtime'].rules,
  },
});
```

## License
MIT License

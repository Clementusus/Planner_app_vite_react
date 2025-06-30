# Planer zadań

Planer zadań is a modern, customizable task planner built with React, TypeScript, and Vite. It helps you organize your tasks, create custom plans, and manage your schedule with a beautiful and intuitive interface.

![App Logo](public/image1.png)

## Features

- 📝 Create, edit, and delete custom plans and tasks
- 🎨 Multiple color themes and font options
- 💾 Save and load your plans locally
- 📅 Responsive and user-friendly interface
- ⚡ Fast performance with Vite and React 19
- 👩‍💻 Built with TypeScript for type safety

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v16 or newer)
- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)

### Installation

1. **Clone the repository:**
   ```sh
   git clone https://github.com/your-username/planer-zadan.git
   cd planer-zadan
   ```

2. **Install dependencies:**
   ```sh
   npm install
   # or
   yarn install
   ```

3. **Start the development server:**
   ```sh
   npm run dev
   # or
   yarn dev
   ```

4. **Open your browser:**  
   Visit [http://localhost:5173](http://localhost:5173) to view the app.

## Usage

- Click "Stwórz nowy plan" to create a new plan.
- Customize your plan with different themes and fonts.
- Save your plans for future use.
- Access your saved plans from the "Moje zadania" section.
- Adjust settings in the "Ustawienia" panel.

## Project Structure

```
├── public/
│   └── image1.png (logo and other images)
├── src/
│   ├── App.tsx
│   ├── Nowyplan.tsx
│   ├── saved.tsx
│   ├── settings.tsx
│   └── ...
├── index.html
├── package.json
├── tsconfig.json
└── vite.config.ts
```

## ESLint Configuration

This project uses ESLint for code quality and consistency. For production, enable type-aware lint rules:

```js
export default tseslint.config([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      // Other configs...

      // Remove tseslint.configs.recommended and replace with this
      ...tseslint.configs.recommendedTypeChecked,
      // Alternatively, use this for stricter rules
      ...tseslint.configs.strictTypeChecked,
      // Optionally, add this for stylistic rules
      ...tseslint.configs.stylisticTypeChecked,

      // Other configs...
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
      // other options...
    },
  },
])
```

You can also install [eslint-plugin-react-x](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-x) and [eslint-plugin-react-dom](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-dom) for React-specific lint rules:

```js
// eslint.config.js
import reactX from 'eslint-plugin-react-x'
import reactDom from 'eslint-plugin-react-dom'

export default tseslint.config([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      // Other configs...
      // Enable lint rules for React
      reactX.configs['recommended-typescript'],
      // Enable lint rules for React DOM
      reactDom.configs.recommended,
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
      // other options...
    },
  },
])
```

## Credits

Created by **Anna Korzeniewska 53522**  
Icons and images © their respective owners.

---

**Enjoy using Planer zadań!**

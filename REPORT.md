# 📌 Rättningsrapport – fed24s-the-last-todo-isabellavelasquez

## 🎯 Uppgiftens Krav:
# React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Expanding the ESLint configuration

If you are developing a production application, we recommend updating the configuration to enable type aware lint rules:

- Configure the top-level `parserOptions` property like this:

```js
export default tseslint.config({
  languageOptions: {
    // other options...
    parserOptions: {
      project: ['./tsconfig.node.json', './tsconfig.app.json'],
      tsconfigRootDir: import.meta.dirname,
    },
  },
})
```

- Replace `tseslint.configs.recommended` to `tseslint.configs.recommendedTypeChecked` or `tseslint.configs.strictTypeChecked`
- Optionally add `...tseslint.configs.stylisticTypeChecked`
- Install [eslint-plugin-react](https://github.com/jsx-eslint/eslint-plugin-react) and update the config:

```js
// eslint.config.js
import react from 'eslint-plugin-react'

export default tseslint.config({
  // Set the react version
  settings: { react: { version: '18.3' } },
  plugins: {
    // Add the react plugin
    react,
  },
  rules: {
    // other rules...
    // Enable its recommended rules
    ...react.configs.recommended.rules,
    ...react.configs['jsx-runtime'].rules,
  },
})
```


## 🔍 ESLint-varningar:
- C:\Work\AssignmentCorrector\backend\repos\fed24s-the-last-todo-isabellavelasquez\src\models\Todo.ts - no-unused-vars - 'title' is defined but never used.,no-unused-vars - 'description' is defined but never used.,no-unused-vars - 'priority' is defined but never used.

## 🏆 **Betyg: G**
📌 **Motivering:** Koden uppfyller de grundläggande kraven och implementerar en React-app med TypeScript och Vite. Funktionaliteten inkluderar tillägg, visning och hantering av Todo-uppgifter samt sortering av dessa. ESLint-konfigurationen verkar inte helt komplett när det gäller type-aware lint rules. Det finns också några mindre kodkvalitetsproblem, såsom strukturen på komponentinställningar och inkonsistens i hanteringen av typsystemet.

💡 **Förbättringsförslag:**  
1. Säkerställ att ESLint-konfigurationen uppdateras enligt uppgiftens krav för att inkludera type-aware lint rules. Det skulle hjälpa till att fånga typsfel på förhand. 
2. Överväg att flytta alla komponentdefinitioner till separata filer för bättre läsbarhet och kodorganisation.
3. Nyckelordsåtkomst i Todo-modellen kan förbättras genom att använda en unik identifierare istället för att förlita sig på Date.now(), vilket kan leda till krockar om flera Todos läggs till mycket snabbt.
4. Inkonsekvenser i CSS-klasser kan fixas genom att säkerställa att alla delar använder TailwindCSS på samma sätt. 
5. Använda enhetstestning för att säkerställa att all funktionalitet fungerar som förväntat och inte bryts av framtida förändringar.
# QWM Quiz App

Application React/Vite pour s'entraîner aux quiz AWS.

Les quiz sont chargés localement depuis `src/data` :

- quiz TypeScript de base via `src/data/quizzes.ts`
- fichiers Markdown `*.md` transformés en quiz à la compilation

## Développement local

```bash
npm install
npm run dev
```

## Build local

```bash
npm run build
npm run preview
```

## Note

Cette version ne dépend pas d'un backend ni de routes API `/api/*`.

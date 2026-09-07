## Switching from ts-node to tsx

### Why

- Faster development — tsx runs TypeScript instantly with no extra setup.
- No config overhead or setup errors when running code.
- Type-checking is already handled by the editor, so tsx doesn't need to slow down execution repeating it.

### How to Switch

**Step 1: Install packages**


npm init -y


npm i typescript tsx @types/node


npm i -D nodemon


npx tsc --init


**Step 2: Edit `tsconfig.json`**


{
  "compilerOptions": {
    "types": ["node"],
    "lib": ["esnext"]
  }
}

**Step 3: Edit `package.json`**


{
  "type": "module",
  "scripts": {
    "dev": "nodemon --exec tsx src/server.ts"
  }
}


> Note: create `src/server.ts` before running `npm run dev`.

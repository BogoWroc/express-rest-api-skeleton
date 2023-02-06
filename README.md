Skeleton of REST API via Express
---


# Used libraries

    Express is the web framework that we are going to use.

    Dotenv is a zero-dependency module that loads environment variables from a .env file into process.env.

    CORS is a node.js package for providing a Connect/Express middleware that can be used to enable CORS with various options.

    Helmet helps you secure your Express apps by setting various HTTP headers. “It’s not a silver bullet, but it can help!”

    TypeScript is a strongly typed programming language that builds on JavaScript, giving you better tooling at any scale. 

    Nodemon helps develop Node.js based applications by automatically restarting the nodejs application when file changes in the directory are detected.

# Project configuration

- Type script is configured via tsconfig.json

```json
"baseUrl": "src",
"outDir": "dist",
```

- Service port is configured via .env file

```text
PORT=3000
```

- Nodemon is configured via nodemon.js

```json
{
    "watch": [
        "src",
        ".env"
    ],
    "ext": "js,ts,json",
    "ignore": [
        "src/logs/*",
        "src/**/*.{spec,test}.ts"
    ],
    "exec": "ts-node --transpile-only src/index.ts"
}
```

# Dev commands

- npm run dev

- npm run build

- npm run start

# Tips
- Project initialisation

```cmd
npm init -y
```
- Add dependencies

```cmd
npm i express dotenv cors helmet
```
- Add typescript

```cmd
npm i -D typescript @types/node @types/express @types/dotenv @types/cors @types/helmet
```
- Generate TypeScript configuration

```cmd
npx tsc --init
```
- Add dev dependencies

```cmd
npm i -D nodemon ts-node
```

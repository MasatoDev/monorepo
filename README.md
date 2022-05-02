# MEMO

## Setup

### install tools

```bash
npm install --global @nestjs/cli
npm install --global lerna
```

### create packages

```bash
mkdir monorepo
/monorepo npx create-react-app react-app
/react-app rm -rf .git
/monorepo nest new nest-api-server
/nest-api-server rm -rf .git

lerna init
lerna create @monorepo/nest-api-server ./packages/nest-api-server
lerna create @monorepo/react-app ./packages/react-app

// ２パッケージとも、script "dev"で起動するよう調整

lerna run dev
```


### lerna run options

https://github.com/lerna/lerna/blob/main/commands/run/README.md



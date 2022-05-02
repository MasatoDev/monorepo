```bash
npm install --global @nestjs/cli
npm install --global lerna
```

https://www.rasukarusan.com/entry/2021/03/23/230105

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

:::tip
setup react with webpack
https://medium.com/age-of-awareness/setup-react-with-webpack-and-babel-5114a14a47e9
:::

:::tip
lerna run options
https://github.com/lerna/lerna/blob/main/commands/run/README.md
:::

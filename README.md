# Website

## Как создать проект

Установить Docusaurus можно с помощью пакетного менеджера `npm`.
Действую по официальной [инструкции](https://docusaurus.io/docs/installation).

### Шаг 1. 
Локально на компьютере в терминале (консоли) выполнить команду:

```
npx create-docusaurus@latest my-website classic
```

### Шаг 2.

На GitHub создать новый репозиторий с тем же именем `my-website`. 
`Readme.md`, `.gitignore` и `License` можно не добавлять.

Копировать SSH-ключ.

### Шаг 3. 

В терминале войти в созданный проект.
Поочередно выполнить команды:

```
git init // инициализировать репозиторий
git add . // добавить файлы в git storage
git commit -m "Initial commit" // создать коммит
git remote add origin <SSH-ключ> // связать локальный репозиторий с удаленным
git branch -M main // инициализировать основную ветку
git push -u origin main // задеплоить файлы в удаленный репозиторий
```

### Шаг 4.

На GitHub зайти в созданный репозиторий и убедиться, что коммит выполнен успешно.

**Обратить внимание:**
```
[WARNING] When deploying to GitHub Pages, it is better to use an explicit "trailingSlash" site config.
Otherwise, GitHub Pages will add an extra trailing slash to your site urls only on direct-access (not when navigation) with a server redirect.
This behavior can have SEO impacts and create relative link issues.
```


---

This website is built using [Docusaurus](https://docusaurus.io/), a modern static website generator.

## Installation

```bash
yarn
```

## Local Development

```bash
yarn start
```

This command starts a local development server and opens up a browser window. Most changes are reflected live without having to restart the server.

## Build

```bash
yarn build
```

This command generates static content into the `build` directory and can be served using any static contents hosting service.

## Deployment

Using SSH:

```bash
USE_SSH=true yarn deploy
```

Not using SSH:

```bash
GIT_USER=<Your GitHub username> yarn deploy
```

If you are using GitHub pages for hosting, this command is a convenient way to build the website and push to the `gh-pages` branch.


### Svelte Project with Docker, Mysql, Redis Node

This is a docker-compose install for

- sveltekit
- Mysql
- chroma
- clickhouse
- redis

also has npm packages installed

- [Typescript](https://www.typescriptlang.org/) typescript sveltekit
- [prisma](https://www.prisma.io/) database connection to Mysql
- [Langchain](https://zod.dev/) Chroma and LLM models
- [tailwindcss](https://tailwindcss.com/) css formating
- [postcss](https://postcss.org/) css pre-processing
- [skeleton ui](https://www.skeleton.dev/) UI features
- [iconify](https://iconify.design/docs/icon-components/svelte/) icons package
- [ZOD](https://zod.dev/) form and server validation
- [zod-form-data](https://www.npmjs.com/package/zod-form-data) formdata parser for Zod


## Get source code
``` bash
git clone https://github.com/jazzjazzy/sveltekit-docker-framework.git new-directory-name
```
you can change the new-directory-name of the directory to whatever you want

remove the .git folder

``` bash
cd new-directory-name
rm -rf .git

```
and the commit your own repo

``` bash
git init
git add .
git commit -m "Initial commit"

# add your own repo on Github 

git remote add origin https://github.com/yourusername/yournewrepo.git
git push -u origin master

```

## Setup .env file

``` bash
cp .env.example .env
```

## run docker and install Packages

you will need to start docker and the install the node packages

``` bash
docker-compose up --build

#once the docker is running you can install the node packages

docker exec -it sveltekit npm install

```

## run the project
you can then run the project with docker exec or npm run docker-dev
they are both the same command, its just running npm run dev inside the docker container

``` bash
docker exec -it sveltekit npm run dev 

#or 

npm run docker-dev

```

## Building

To create a production version of your app:

```bash
docker exec -it sveltekit npm run build 

#or 

npm run docker-build
```

You can preview the production build with `npm run preview`.

> To deploy your app, you may need to install an [adapter](https://kit.svelte.dev/docs/adapters) for your target environment.

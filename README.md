# Tutorial Heroku
 
## Buildando um app Laravel

### Login no Heroku

```
$ heroku login
```

### Criando aplicação Heroku

```
$ heroku create
```

### Permitir que a aplicação do Heroku rode comandos nodejs e php

```
$ heroku config:add \
> BUILDPACK_URL=https://github.com/heroku/heroku-buildpack-multi.git
```

### Criar o arquivo .buildpacks na raiz do projeto laravel com o seguinte conteúdo

```
https://github.com/heroku/heroku-buildpack-nodejs
https://github.com/heroku/heroku-buildpack-php
```

### Criar o Procfile na raiz do projeto laravel com o seguinte conteúdo

```
web: vendor/bin/heroku-php-apache2 public/
```

### Fazendo Push para o Heroku

```
$ git push heroku master
```

OBS.: Caso tenha clonado um projeto laravel para trabalhar e este projeto esteja no Heroku, não esqueça de adicionar o repositório remoto do Heroku em sua aplicação laravel.

Para isso utilize o comando abaixo.

```
$ git remote add heroku https://git.heroku.com/{project-name}.git
```


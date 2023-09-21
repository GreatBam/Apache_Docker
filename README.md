# Apache Docker

This repo allow you to install an Apache with database and phpMyAdmin environment.

## Installation

First, clone the repo in the desired folder.

Then, if it's not already the case, install Docker Desktop on your computer :
```bash
https://www.docker.com/products/docker-desktop/
```

Now, go to the root directory and run the following command :
```bash
docker-compose up -d
```

This will create the docker container and run it.

The "-d" argument let yyou run the command in detached mode and allow you to continue use your terminal prompt.

You can now use your environnement.

## Usage

To test if the container is working properly, navigate to the following URL :
```bash
http://localhost:8080/
```

Once everthing is installed, you can now add your project into the "www" folder in the root directory.

Paste or create your html/css/js website in it.

Navigate then in your favorite browser to the URL, for exemple :
```bash
http://localhost:8080/MyProject/index.html
```

## PhpMyAdmin

To monitor your database, phpMyAdmin is integrated into the container.

To access phpMyAdmin, go to the following URL :
```bash
http://localhost:8081
```

All the password and usernames are in the .env file, here are the default presets :
```bash
MYSQL_DATABASE=Data
MYSQL_USER=root
MYSQL_PASSWORD=admin
MYSQL_ROOT_PASSWORD=admin
```

## Staging and production

If you give a look at the docker-compose file, you'll see that there is two "www" services.

This allow you to have a staging and a production environnement.

Once you made everything as wished in the standard "www" version in the following URL :
```bash
http:/localhost:8080
```

You can then copy the entire project into the production environnementt with the following command in the root directory :
```bash
docker-compose build
```

You will then find the content with the "www2" URL :
```bash
http:/localhost:8082
```

Note that if you put the folders in the directory BEFORE you build the container, they will be added in production as well.

## Credits

Jonathan Gabioud
"# Apache_Docker" 

# Docker Laravel Advanced
This is a simple docker setup. It is ready to get used for Laravel projects.  
It is mainly taken from this article: [Set up Laravel Project With Docker](https://medium.com/@gerrysabar/set-up-laravel-project-with-docker-85b41ea5669) by Gerry Sabar.

## Usage
```shell
git clone git@github.com:seebaermichi/docker-laravel-advanced.git project-name
cd ./project-name

# Remove version control
rm -fr ./.git

# If not already available, get laravel installer
composer global require laravel/installer

# Create new Laravel project
laravel new src
```
After this you should have all required Laravel files within the src folder.  
There you would also find the `.env` file where you should make sure that the settings  
for the database match what is added in the `docker-compose.yml` at the `db` service.

```shell
# Build the containers
docker-compose build
```

```shell
# Run the containers
docker-compose up -d
```

If everything is up and running you should be able to see the Laravel project at  
[localhost:8080](http://localhost:8080)

## License
docker laravel dev is released under the MIT License. See [LICENSE][1] file for details.
                   
[1]: https://github.com/seebaermichi/docker-laravel-advanced/blob/master/LICENSE

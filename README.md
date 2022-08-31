# WordPress Local Development Using Docker Compose

Pull and install WordPress to the same directory containing the .docker folder (yes, this root folder)

## How to:
* Make sure you have Docker Desktop and WSL installed, if not, please refer to [WSL and Docker Desktop installment from Microsoft](https://docs.microsoft.com/en-us/windows/wsl/setup/environment).
* Clone this repo
* Open terminal and change dir to .docker folder `cd .docker`
* Type `code .` to open .docker files Visual Studio Code WSL remote.
* Choose `docker-entrypoint.sh` file and make sure to change end of line sequence from CRLF to LF to avoid $'\r' command not found error on Windows when build with Docker.
* Choose `.env` file and change environment variables as per your preference.
* In the terminal, make sure you're in /.docker directory then type `docker compose build`. Grab your coffee, this will take a while.
* When the build process is finished, in the same terminal type `docker compose up`. You can run docker in dettached mode by typing `docker compose up -d`. Keep enjoying your coffee until it finishes.
* If success, you will see all of core WordPress files appear in the same directory containing .docker (wp-admin, wp-content, wp-includes, wp-login.php, wp-config.php,...)
* If you haven't changed the WORDPRESS_SITE_LOCAL_PORT variable in `.env` file then go to `localhost:8000`, you will see the WordPress famous 5-minute installation.
* Go to `localhost:8080` to access your WordPress database in phpMyAdmin, use the variables from `.env` file to login and access your database.
* Now go and build your awesome WordPress project!

# WordPress Docker Dev Environment

Used for plugin or theme development for WordPress

## Instructions

- Clone this repo (above) to your local machine
- Install [Docker](https://docs.docker.com/get-docker/)
- Download the latest version of [WordPress](https://en-gb.wordpress.org/download/)
- Unzip WordPress and copy the **contents** into 'wordpress' in your cloned repo
- Open the cloned repo folder in any command-line tool
- Run ```docker-compose up -d --build```
- Open ```localhost``` in your browser
- Run initial wordpress installation using 'wordpress' for names and 'secret' for passwords (these values can be changed in ```docker-compose.yml```)
- To stop running on localhost, run ```docker-compose down```
- Run ```docker-compose -d --build``` any time to start it again-- your changes within wp should persist
- Tip: add ```define('FS_METHOD','direct');``` to ```wordpress/wp-config.php``` to avoid issues with FTP when installing test plugins

### Credit

Built with [this tutorial](https://www.youtube.com/watch?v=kIqWxjDj4IU) by [aschmelyun](https://github.com/aschmelyun). Refer to this video if you have issues with the certificates or database connection.

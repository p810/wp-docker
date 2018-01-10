# wp-docker

> A lightweight Docker set up for WordPress development.

## Usage
This environment requires [Docker](https://docker.com).

Clone this repository into a directory to contain your installation of WordPress.
After cloning and entering that directory, run `docker-compose up` to install the
necessary containers.

You should see a message indicating that the installation was successful. You may
now navigate to `localhost:8080` to install WordPress.

### Starting and stopping
To stop the server, run `docker-compose stop`. To start it again, `docker-compose start`. :grin:

### Destruction
If you wish to get rid of this installation of WordPress, database and all, run
`docker-compose down`. Unless you've made a backup this is irreversible.

## Version control
This repository's `.gitignore` will ignore every file except itself, this file,
and `docker-compose.yml`.

If you're planning to commit WordPress files to a Git repository, I recommend only
making exceptions in `.gitignore` for those that are specific to _your_ site, e.g.
plugins and themes, since core WordPress files are handled by the container.

(Disclaimer: I haven't tested how installation will behave when `/wp-content` is
already present in the directory. I intend to do this at some point.)

dockerwordpress
===============

Great WordPress with NGINX and New Relic instrumentation

Modified from:
# docker-wordpress-nginx

A Dockerfile that installs the latest wordpress, nginx, php-apc and php-fpm.

NB: A big thanks to [jbfink](https://github.com/jbfink/docker-wordpress) who did most of the hard work on the wordpress parts!

You can check out his [Apache version here](https://github.com/jbfink/docker-wordpress).

## Installation

```
$ git clone https://github.com/poulsbopete/dockerwordpress.git
$ cd dockerwordpress
$ sudo docker build -t="dockerwordpress" .
```

## Usage

To spawn a new instance of wordpress on port 80.  The -p 80:80 maps the internal docker port 80 to the outside port 80 of the host machien.

```bash
$ sudo docker run -p 80:80 --name dockerwordpress -d dockerwordpress
```

Start your newly created docker

```
$ sudo docker start dockerwordpress
```

After starting the dockerwordpress check to see if it started and the port mapping is correct.  This will also report the port mapping between the docker container and the host machine.
```
$ sudo docker ps

0.0.0.0:80 -> 80/tcp dockerwordpress
```

You can the visit the following URL in a browser on your host machine to get started:

```
http://127.0.0.1:80
```

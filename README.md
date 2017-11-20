# Docker tor hidden services

This docker container allows you to easily expose ports on other containers as hidden services on the tor network.

## Usage

The service is used in our Tor Hidden Service hosting via OneHost Cloud. We integrated this with other containers such as PHP/Wordpress ( which we do not advise on Tor ) and FTP via SSH. To host your hidden service on Tor visit https://onehostcloud.hosting 

```
EXPOSE 80
```

Running this as a hidden service is as simple as the following two commands

```bash
$ docker run -d my-awesome-app
$ docker run --link my-hidden-web-app:web -d patrickod/docker-tor-hidden-service
```

This will expose port 80 on the hidden service domain and direct it to your linked container.

## Why ?

OneHost Cloud firmly beleives in privacy and the privacy and security that Tor offers allows anyone to host website privately ( with additional OpSec ) and without the interuption from Governments and other nefarious entities.


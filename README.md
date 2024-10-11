# Dante & Docker

Dante is a free SOCKS server and a SOCKS client, implementing RFC 1928 and
related standards. 

## Software specficiation

* Base image: Alpine Linux
* Dante version: 1.4.2
* [![](https://images.microbadger.com/badges/image/adegtyarev/dante.svg)](https://microbadger.com/images/adegtyarev/dante "the download size and the number of layers")

### Dante & Docker Compose

Should you run using Docker Compose a private SOCKS server with simple
username/password auth, clone this project and create a settings file:

    $ git clone https://github.com/vartemkin/docker-dante.git
    $ cd docker-dante
    $ docker compose up -d

The SOCKS server should be up and ready to serve.  An example command to test
the proxy service you have just set up:

    $ curl -x socks5h://user123:pass123@127.0.0.1:1080 http://example.com

Access the logs with:

    $ docker logs my_dante


## Author

Alexey Degtyarev @adegtyarev

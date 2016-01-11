# wordpress

adapting official wordpress docker container for bluemix needs

official wordpress container: https://hub.docker.com/_/wordpress/

## changes
- added WP_HOME, WP_SITEURL to configuration - prevents changing url in admin dashboard
- added sleep + extended connection tries to db because bluemix needs more time to setup networking
    see: https://www.ng.bluemix.net/docs/containers/container_single_ov.html#container_single_cli


## build

    docker build -t truffls/wordpress .

## deploy

    docker push truffls/wordpress

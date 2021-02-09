# Running pihole with unbound in docker

This is the simplest possible setup for running your own pihole + unbound setup. This is configured to run in two separate containers (so they can be updated/debugged independently).

See the ```docker-compose.yml``` for the details.

unbound uses ```image: klutchell/unbound``` (user image, more [here](https://gitlab.com/klutchell/unbound)).  
unbound requires the ```unbound.conf``` file in the location provided. If you change the location, don't forget to unpdate the mapped volume in the ```docker-compose.yml```.

pihole uses ```image: pihole/pihole``` (the offical pihole [image](https://hub.docker.com/r/pihole/pihole)). Tweak the environment settings as required - it's best to setup the configuration you want via these env variables rather than making the change in the pihole web UI and saving.

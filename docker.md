# Docker

## print out all enviroment variables 
``docker inspect --format '{{ index .Config.Env }}' container_id|container_name``

## inspect one variable in running docker instance
`docker inspect --format '{{ index (index .Config.Env) number }}' container_id|container_name`

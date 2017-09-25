# Docker

## print out all enviroment variables with 
[inspiration](http://stackoverflow.com/questions/30342796/how-to-get-env-variable-when-doing-docker-inspect)

`docker inspect --format='{{range .Config.Env}}{{println .}}{{end}}'  container_id|container_name`

## inspect one variable in running docker instance
`docker inspect --format '{{ index (index .Config.Env) number }}' container_id|container_name`

## todo

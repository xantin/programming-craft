# Docker

`docker inspect --format '{{ index (index .Config.Env) 1 }}' container_id|container_name`
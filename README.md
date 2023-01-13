# docker-owncloud

  It is part of a [set of repositories](https://github.com/search?q=user%3Admartingarcia+docker) that contain dockerised environments for small applications.

  In this case, it contains a self-efficient *Owncloud* setup.

  ## How to use it

  ```
  cp .env.example .env
  docker-compose up -d
  ```

  PLEASE, CHANGE THE DEFAULT ADMIN PASSWORDS

  And browse into `http://localhost:8081` in order to see the `owncloud` login page.

  ## Traefik integration`

  It also contains a Traefik integration, that interact with this reverse proxy, routing request to each container in case it matches the specified domain

  There's multiple subdomains exposed:
    - owncloud.your.domain.com

  ## .env setup

  It contains a basic set of variables like:

  - Credentials
  - http host that uses Traefik to match requests

  Please take a look on that and :warning: create your own credentials :warning: in case you want to expose it to the public.

  ## Docker Traefik

  If you want to use this Traefik integration, [take a look at this repository](https://github.com/dmartingarcia/docker-traefik)

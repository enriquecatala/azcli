<div>
    <a href="https://github.com/sponsors/enriquecatala"><img src="https://img.shields.io/badge/GitHub_Sponsors--_.svg?style=flat-square&logo=github&logoColor=EA4AAA" alt="GitHub Sponsors"></a>
    <a href="https://enriquecatala.com"><img src="https://img.shields.io/website?down_color=red&down_message=down&label=enriquecatala.com&up_color=46C018&url=https%3A%2F%2Fenriquecatala.com&style=flat-square" alt="Data Engineering with Enrique Catalá"></a>
    <a href="https://www.linkedin.com/in/enriquecatala"><img src="https://img.shields.io/badge/LinkedIn--_.svg?style=flat-square&logo=linkedin" alt="LinkedIn Enrique Catalá Bañuls"></a>
    <a href="https://twitter.com/enriquecatala"><img src="https://img.shields.io/twitter/follow/enriquecatala?color=blue&label=twitter&style=flat-square" alt="Twitter @enriquecatala"></a>
    <a href="https://youtube.com/enriquecatala"><img src="https://raw.githubusercontent.com/enriquecatala/enriquecatala/master/img/youtube.png" alt="Data Engineering: Canal youtube de Enrique Catalá" height=20></a>
</div>

<a href="https://mvp.microsoft.com/es-es/PublicProfile/5000312?fullName=Enrique%20Catala"><img src="https://raw.githubusercontent.com/enriquecatala/enriquecatala/master/img/MVP_Logo_horizontal.png" alt="Microsoft DataPlatform MVP Enrique Catalá"></a>

# azcli

This project is just a [docker-compose.yml](./docker-compose.yml) for azcli that persist the login information inside the "data" folder (which is mounted in the container) to avoid having to login everytime.

This is very useful if you want to have multiple azcli instances with different credentials.
## Usage

```bash
docker compose up -d
docker exec -it azcli bash
az login
# launch your query in azcli, everytime you start up this container will use that config :)
```

## Optional

Edit the ~/.bashrc file to add the following line `export DOCKER_USER="$(id -u):$(id -g)"`
# azcli
azcli docker compose

## Configuration

Edit the ~/.bashrc file to add the following line `export DOCKER_USER="$(id -u):$(id -g)"`
## Usage

```bash
docker compose up -d
docker exec -it azcli bash
```
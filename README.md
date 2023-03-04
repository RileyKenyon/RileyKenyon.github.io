# Getting Started
This site is hosted with github pages - using a jekyll theme [portfolYOU](https://github.com/YoussefRaafatNasry/portfolYOU).

## Developing locally
Docker is used to develop locally by using a ruby image and bundle to setup the jekyll environment. The docker file is configured with live reload to view changes as they are saved.

### Setup docker environment
Create an `.env` file in the docker directory to set the environment variables used to build the container
```
REPO_ROOT="YOUR_PATH_HERE"
```

Use `docker compose` to run the build the image and run the container:

```bash
cd docker
docker compose build
# Bring up the container in the background
docker compose up -d

# when finished with the container
docker compose down
```

Navigate to [localhost:4000](http://localhost:4000) to view the hot-reloaded version of the website.
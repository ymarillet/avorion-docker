Avorion for Docker
==================

### Game Info

For some information about the game see https://www.kickstarter.com/projects/koonschi/avorion

**Supported version is the latest stable version available on Steam**


## Getting started
1. Make sure Git and Docker-compose are also installed along with Docker
1. Create a `.env` file from the `.env.dist` template and tweak the values as you like
1. Put your galaxy data previously created in `/opt/avorion_server/data` (by default)
   OR run the server once to let it create a galaxy for you so you can modify the settings.ini to your needs

Run the following commands to start the server:
```
git clone https://github.com/ymarillet/avorion-docker.git
cd avorion-docker
docker-compose up
```

You can access the server logs with: `docker-compose logs -f` (it acts as `tail -f`)

You can stop the server with: `docker-compose down`

> Note: The server is slow to start compared to the `psykzz/avorion-docker` version
> because the container is recreated every time (except the server data), so it means
> that it has to re-download the steam wrapper and the server program 
> but this way it ensures you always have the most up-to-date server version

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md)



How to install and run the [Visionect Software Suite](https://docs.visionect.com/VisionectSoftwareSuite/Installation.html)
locally on a mac:

1. Install Docker:
```shell
brew install colima docker docker-compose
```

2. Start and verify that Docker daemon is running:
```shell
colima start
docker ps -a
```

3. Download the docker file:
```shell
curl https://docs.visionect.com/_downloads/cda94dc639573626dadb9a3c907a429f/docker-compose.yml --output docker-compose.yml
```

4. Use `uuidgen` to set a valid uuid key (e.g. `28531EA8-8187-4F24-B1F4-95531FC45B2D`) to ensure web interface cookie validity and previous user sessions
```shell
set VISIONECT_SERVER_DEPLOYMENT_KEY 28531EA8-8187-4F24-B1F4-95531FC45B2D
```

5. Run docker compose:
```shell
docker-compose up -d
```

6. You can now open `localhost:8081` and use the [following credentials](https://docs.visionect.com/VisionectSoftwareSuite/Installation.html#default-settings) to login

7. Configure the client on the server (TBD)

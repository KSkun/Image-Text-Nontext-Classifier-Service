# Image-Text-Nontext-Classifier-Service

Text/non-text image crawler &amp; classifier service. Software course project of EIC, HUST (2021 Autumn).

## Features

![main page screenshot](https://github.com/KSkun/Image-Classifier-Frontend/raw/master/image/main_page_detail_task.png)

### Neural Network Classifier

See https://github.com/KSkun/Image-Text-Nontext-Classifier.

### Search Engine Spider

See https://github.com/KSkun/Image-Spider.

### Web User Interface

Frontend: https://github.com/KSkun/Image-Classifier-Frontend.

Backend: https://github.com/KSkun/Image-Classifier-Backend.

### Docker Containerize

The service is split to 4 modules and developed individually, then containerized with Dockerfile. In this repo, the service is configurated with `docker-compose.yml`, which makes deployment easier for users.

## Configuration

1. Install `git` and `git-lfs`.
2. Pull this repo with command `git clone --recurse-submodules`.
3. In `./classifier` folder, run `git lfs pull`.
4. Check if you need a third-party source for pip or npm in `Dockerfile`. Note that `frontend/Dockerfile` uses a HTTP proxy server by default, remember to configurate it for your environment.
5. Set the port you want in `ports` field of frontend in `docker-compose.yml`.
6. Run `docker-compose up -d`, wait for building image & creating containers. If you need a development environment, use `docker-compose-debug.yml` instead.
7. Test it with your browser.


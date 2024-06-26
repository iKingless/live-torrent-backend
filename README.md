# LiveTorrentBackend

<!--[![Build Status](https://travis-ci.org/Davenchy/live-torrent-backend.svg?branch=master)](https://travis-ci.org/Davenchy/live-torrent-backend)-->
[![Twitter Follow](https://img.shields.io/twitter/follow/fadi_davenchy?style=social)](https://twitter.com/fadi_davenchy?ref_src=twsrc%5Etfw)

LiveTorrentBackend is a server that uses WebTorrent and Hono to serve
torrent file content.

Originally designed as part of the
[Live Torrent](https://github.com/Davenchy/live-torrent) project's backend,
it can also be used independently or integrated into your own projects.

For more details check the [documentation](#documentation).

![Live Torrent Logo](logo.png)

[![Gitpod Ready-to-Code](https://img.shields.io/badge/Gitpod-Ready--to--Code-blue?logo=gitpod)](https://gitpod.io/#https://github.com/Davenchy/live-torrent-backend)

## Features

- Search for torrent files using various trackers (e.g., 1337x, RARBG, EZTV, YTS).

- List and view torrent files.

- Serve, download, visit torrent file content.

- Search OpenSubtitles subtitles **BETA**.

> Coming soon: Download subtitles.

## Docker

To use the Docker [image](https://hub.docker.com/repository/docker/davenchy/live-torrent-backend), run:

```sh
docker run -d -p 3000:3000 -v $(pwd)/downloads:/app/downloads davenchy/live-torrent-backend:latest
```

Mount the `/app/downloads` volume to manage downloaded files.

## Documentation

OpenAPI is used to build the documentation, which written in the `openapi.yaml` file.

Start the server and visit `/docs` to view the documentation.

## Installation

Ensure you have Node.js version 18 installed. Then, run the following commands:

```bash
git clone --depth=1 https://github.com/Davenchy/live-torrent-backend.git

cd live-torrent-backend

npm install

npm start
```

## Environment Variables

Set the following environment variables, also you could user the `.env` file:

| Variable Name | Is Required | Default Value | Description |
|:-:|:-:|:-:|:- |
| PORT | NO | 3000 | The port to listen on. |
| OS_APIKEY | For OpenSubtitles API. | - | OpenSubtitles API key. |
| OS_USERAGENT | For OpenSubtitles API. | - | OpenSubtitles User Agent. |

For more information about OpenSubtitles API check documentation on [OpenSubtitles API](https://opensubtitles.stoplight.io/docs/opensubtitles-api).

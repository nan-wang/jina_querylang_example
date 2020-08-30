# jina_querylang_example

[![Jina](https://github.com/jina-ai/jina/blob/master/.github/badges/jina-badge.svg?raw=true  "We fully commit to open-source")](https://get.jina.ai)

A demo for illustrating the usage of QueryLangDriver in jina

## Features

## Install

```bash
pip install .
```

To install it in editable mode

```bash
pip install -e .
```

## Run

| Command                  | Description                  |
| :---                     | :---                         |
| ``python app.py index``  | To index files/data          |
| ``python app.py search`` | To run query on the index    |
| ``python app.py dryrun`` | Sanity check on the topology |

## Run as a Docker Container

To build the docker image
```bash
docker build -t jinaai/hub.app.jina_querylang_example:0.0.1 .
```

To mount local directory and run:
```bash
docker run -v "$(pwd)/j:/workspace" jinaai/hub.app.jina_querylang_example:0.0.1
``` 

To query
```bash
docker run -p 20202:20202 -e "JINA_PORT=65481" jinaai/hub.app.jina_querylang_example:0.0.1 search
```

## License

Copyright (c) 2020 nan.wang. All rights reserved.



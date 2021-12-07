# Docker Neo4j Paradise Papers
## How to use
1. Make sure `docker` and `docker-compose` is properly installed

```bash
docker --version
# Docker version 20.10.11, build dea9396
docker-compose --version
# docker-compose version 1.29.2, build 5becea4c
```

2. Clone this repository

```bash
git clone https://github.com/rochimfn/neo4j-paradise-papers.git
cd neo4j-paradise-papers
```

3. Load the paradise papers data

```bash
docker-compose -f docker-compose.load.yaml run --rm neo4j-load
```

4. Start the neo4j database server

```bash
docker-compose up -d
```

neo4j server will be available in port `7687` (server) and `7474` (client)

5. Done

Use the following command to stop the container
```bash
docker-compose down
```

Next time you start the container, just use `docker-compose up -d` 

> Always make sure you are in the right folder berfore running any `docker-compose` command

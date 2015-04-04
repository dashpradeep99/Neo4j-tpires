neo4j
=====

Neo4j is a highly scalable, robust (fully ACID) native graph database. Neo4j is used in mission-critical apps by thousands of leading, startups, enterprises, and governments around the world.

With the Dockerfile on repository you've a docker neo4j community edition image ready to go.

### Setup

1. Execute this command:

	`docker run -i -t -d --name neo4j --cap-add=SYS_RESOURCE -p 7474:7474 ahmetkizilay/neo4j`

2. Access to http://localhost:7474 with your browser.

#### Authentication
You can add authorization credentials or disable authorization by passing `NEO4J_AUTH` as environment variable.

* To set username/password:

  `docker run -i -t -d -e NEO4J_AUTH=username:password --name neo4j --cap-add=SYS_RESOURCE -p 7474:7474 ahmetkizilay/neo4j`

* To bypass authentication:

  `docker run -i -t -d -e NEO4J_AUTH=none --name neo4j --cap-add=SYS_RESOURCE -p 7474:7474 ahmetkizilay/neo4j`


Image forked from [here](https://registry.hub.docker.com/u/tpires/neo4j/)
# neo4j-sparql-extension

[![Build Status](https://api.shippable.com/projects/537d0049a90ec01102ee5abc/badge/master)](https://www.shippable.com/projects/537d0049a90ec01102ee5abc)
[![Dependency Status](https://www.versioneye.com/user/projects/539018d346c4731b13000040/badge.svg?style=flat)](https://www.versioneye.com/user/projects/539018d346c4731b13000040)

Neo4j [unmanaged extension](http://docs.neo4j.org/chunked/stable/server-unmanaged-extensions.html)
for [RDF](http://www.w3.org/TR/rdf-primer/) storage and
[SPARQL 1.1 query](http://www.w3.org/TR/sparql11-protocol/) features.

## Installation

Download the latest release from the [releases page](/releases) and place it
inside the `/plugins/` directory of the Neo4j server installation.

To enable the extension add it to the
`org.neo4j.server.thirdparty_jaxrs_classes` key in the
`/conf/neo4j-server.properties` file. For example:

```
org.neo4j.server.thirdparty_jaxrs_classes=de.unikiel.inf.comsys.neo4j=/rdf
```

The RDF/SPARQL extension is then avaiable as `/rdf` resource on the
Neo4j server.

### SPARQL Protocol (Queries)

Base resource: `/rdf/query`

### SPARQL Graph Protocol

Base resource: `/rdf/graph`

### SPARQL Protocol (Update)

Base resource: `/rdf/update`

## Configuration

To change the configuration add a `sparl-extension.properties` file in the
`/conf` folder of the Neo4j server installation.

The default configuration is as follows:

```
de.unikiel.inf.comsys.neo4j.query.timeout = 120
de.unikiel.inf.comsys.neo4j.inference.graph = urn:ontology
```

## License

GPLv3

# Origins Neo4j

Neo4j image optimized for the Origins graph including pre-defined indexes and constraints.

## Usage

*The `--privileged` flag is required to set the `ulimit` when the Neo4j server starts. See http://docs.neo4j.org/chunked/stable/server-installation.html#linux-install for more details.*

Start the server:

```
docker run -d --privileged -P dbhi/origins-neo4j
```

Mount a local data directory:

```
docker run -d --privileged -P -v /path/to/data:/neo4j/data dbhi/origins-neo4j
```

Run the shell:

```
docker run -d --privileged dbhi/origins-neo4j shell
```

Run a shell command:

```
docker run -d --privileged dbhi/origins-neo4j shell -c 'MATCH (n) RETURN count(n);'
```

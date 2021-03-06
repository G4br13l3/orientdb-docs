# Release 2.2.x

## What's new?

### Command Cache
OrientDB 2.2 has a new component called [Command Cache](Command-Cache.md), disabled by default, but that can make a huge difference in performance on some use cases. Look at [Command Cache](Command-Cache.md) to know more.

### Sequences
-In progress-

### Parallel queries
Starting from v2.2, the OrientDB SQL executor will decide if execute or not a query in parallel. Before v2.2 executing parallel queries could be done only manually by appending the `PARALLEL` keyword at the end of SQL SELECT. [Issue 4578](https://github.com/orientechnologies/orientdb/issues/4578).

### Automatic usage of Multiple clusters
Starting from v2.2, when a class is created, the number of underlying clusters will be the number of cores. [Issue 4518](https://github.com/orientechnologies/orientdb/issues/4518).

### Encryption at rest
-In progress-

### New ODocument.eval()
To execute quick expression starting from a ODocument and Vertex/Edge objects, use the new `.eval()` method. The old syntax `ODocument.field("city[0].country.name")` is not supported anymore. [Issue 4505](https://github.com/orientechnologies/orientdb/issues/4505).

## Migration from 2.1.x to 2.2.x

Databases created with release 2.1.x are compatible with 2.2.x, so you don't have to export/import the database. Check your database directory: if you have a file *.wal, delete it before migration.

### API changes

#### ODocument.field()

To execute quick expression starting from a ODocument and Vertex/Edge objects, use the new `.eval()` method. The old syntax `ODocument.field("city[0].country.name")` is not supported anymore. This is because we simplified the `.field()` method to don't accept expressoion anymore. This allows to boost up performance on such used method. [Issue 4505](https://github.com/orientechnologies/orientdb/issues/4505).

### Configuration Changes

Since 2.2 you can force to not ask for a root password setting `<isAfterFirstTime>true</isAfterFirstTime>` inside the `<orient-server>` element in the orientdb-server-config.xml file.

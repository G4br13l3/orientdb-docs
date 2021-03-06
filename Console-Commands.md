# Console Tool

The OrientDB Console is a Java Application made to work against OrientDB databases and Server instances.

## Interactive mode

This is the default mode. Just launch the console by executing the script **bin/console.sh** (or **bin/console.bat** in MS Windows systems). Assure to have execution permission on it.

Once started the console is ready to accepts commands.
```
OrientDB console v.1.6.6 www.orientechnologies.com
Type 'help' to display all the commands supported.

orientdb>
```

To know all the supported commands look to [commands](#Console_Commands).

## Batch mode

To execute commands in batch mode run the **bin/console.sh** (or **bin/console.bat** in MS Windows systems) script passing all the commands separated with semicolon ";". Example:

```
> console.bat "connect remote:localhost/demo;select * from profile"
```

Or call the console script passing the name of the file in text format containing the list of commands to execute. Commands must be separated with semicolon ";". Example:

    orientdb> console.bat commands.txt

In batch mode you can ignore errors to let the script to continue the execution by setting the "ignoreErrors" variable to true:

    orientdb> set ignoreErrors true

## Enable echo
When you run console commands in pipeline, you could need to display them. Enable "echo" of commands by setting it as property at the beginning:

    orientdb> set echo true

## Console commands

To know all the commands supported by the Orient console open it and type **help** or **?**.

|Command|Description|
|-------|-----------|
|[ALTER CLASS](SQL-Alter-Class.md)|Changes the class schema|
|[ALTER CLUSTER](SQL-Alter-Cluster.md)|Changes the cluster attributes|
|[ALTER DATABASE](SQL-Alter-Database.md)|Changes the database attributes|
|[ALTER PROPERTY](SQL-Alter-Property.md)|Changes the class's property schema|
|[BACKUP DATABASE](Console-Command-Backup.md)|Backup a database|
|[BEGIN](Console-Command-Begin.md)|Begins a new transaction|
|[BROWSE CLASS](Console-Command-Browse-Class.md)|Browses all the records of a class|
|[BROWSE CLUSTER](Console-Command-Browse-Cluster.md)|Browses all the records of a cluster|
|[CLASSES](Console-Command-Classes.md)|Displays all the configured classes|
|[CLUSTER STATUS](Console-Command-Cluster-Status.md)|Displays the status of distributed cluster of servers|
|[CLUSTERS](Console-Command-Clusters.md)|Displays all the configured clusters|
|[COMMIT](Console-Command-Commit.md)|Commits an active transaction|
|[CONFIG](Console-Command-Config.md)|Displays the configuration where the opened database is located (local or remote)|
|[CONFIG GET](Console-Command-Config-Get.md)|Returns a configuration value|
|[CONFIG SET](Console-Command-Config-Set.md)|Set a configuration value|
|[CONNECT](Console-Command-Connect.md)|Connects to a database|
|[CREATE CLASS](SQL-Create-Class.md)|Creates a new class|
|[CREATE CLUSTER](Console-Command-Create-Cluster.md)|Creates a new cluster inside a database|
|[CREATE CLUSTER](Console-Command-Create-Cluster.md)|Creates a new record cluster|
|[CREATE DATABASE](Console-Command-Create-Database.md)|Creates a new database|
|[CREATE EDGE](SQL-Create-Edge.md)|Create a new edge connecting two vertices|
|[CREATE INDEX](SQL-Create-Index.md)|Create a new index|
|[CREATE LINK](SQL-Create-Link.md)|Create a link reading a RDBMS JOIN|
|[CREATE VERTEX](SQL-Create-Vertex.md)|Create a new vertex|
|[DECLARE INTENT](Console-Command-Declare-Intent.md)|Declares an intent|
|[DELETE](SQL-Delete.md)|Deletes a record from the database using the SQL syntax. To know more about the [SQL syntax go here](SQL-Query.md)|
|[DICTIONARY KEYS](Console-Command-Dictionary-Keys.md)|Displays all the keys in the database dictionary|
|[DICTIONARY GET](Console-Command-Dictionary-Get.md)|Loookups for a record using the dictionary. If found set it as the current record|
|[DICTIONARY PUT](Console-Command-Dictionary-Put.md)|Inserts or modify an entry in the database dictionary. The entry is composed by key=String, value=record-id|
|[DICTIONARY REMOVE](Console-Command-Dictionary-Remove.md)|Removes the association in the dictionary|
|[DISCONNECT](Console-Command-Disconnect.md)|Disconnects from the current database|
|[DISPLAY RECORD](Console-Command-Display-Record.md)|Displays current record's attributes|
|[DISPLAY RAW RECORD](Console-Command-Display-Raw-Record.md)|Displays current record's raw format|
|[DROP CLASS](SQL-Drop-Class.md)|Drop a class|
|[DROP CLUSTER](SQL-Drop-Cluster.md)|Drop a cluster|
|[DROP DATABASE](Console-Command-Drop-Database.md)|Drop a database|
|[DROP INDEX](SQL-Drop-Index.md)|Drop an index|
|[DROP PROPERTY](SQL-Drop-Property.md)|Drop a property from a schema class|
|[EXPLAIN](SQL-Explain.md)|Explain a command by displaying the profiling values while executing it|
|[EXPORT DATABASE](Console-Command-Export.md)|Exports a database|
|[EXPORT RECORD](Console-Command-Export-Record.md)|Exports a record in any of the supported format (i.e. json)|
|[FIND REFERENCES](SQL-Find-References.md)|Find the references to a record|
|[FREEZE DATABASE](Console-Command-Freeze-Db.md)|Freezes the database locking all the changes. Use this to raw backup. Once frozen it uses the [RELEASE DATABASE](Console-Command-Release-Db.md) to release it|
|[GET](Console-Command-Get.md)|Returns the value of a property|
|[GRANT](SQL-Grant.md)|Grants a permission to a user|
|[GREMLIN](Console-Gremlin.md)|Executes a Gremlin script|
|[IMPORT DATABASE](Console-Command-Import.md)|Imports a database previously exported|
|[INDEXES](Console-Command-Indexes.md)|Displays information about indexes|
|[INFO](Console-Command-Info.md)|Displays information about current status|
|[INFO CLASS](Console-Command-Info-Class.md)|Displays information about a class|
|[INSERT](Console-Command-Insert.md)|Inserts a new record in the current database using the SQL syntax. To know more about the [SQL syntax go here](SQL-Query.md)|
|[JS](Javascript-Command.md#via_console)|Executes a Javascript in the console|
|[JSS](Javascript-Command.md#via_console)|Executes a Javascript in the server|
|[LIST DATABASES](Console-Command-List-Databases.md)|List the available databases|
|[LOAD RECORD](Console-Command-Load-Record.md)|Loads a record in memory and set it as the current one|
|[PROFILER](Console-Command-Profiler.md)|Controls the [Profiler](Profiler.md)|
|[PROPERTIES](Console-Command-Properties.md)|Returns all the configured properties|
|pwd| | Display current path|
|[REBUILD INDEX](SQL-Rebuild-Index.md)|Rebuild an index|
|[RELEASE DATABASE](Console-Command-Release-Db.md)|Releases a [Console Freeze Database](Console-Command-Freeze-Db.md) database|
|[RELOAD RECORD](Console-Command-Reload-Record.md)|Reloads a record in memory and set it as the current one|
|RELOAD SCHEMA|Reloads the schema|
|[ROLLBACK](Console-Command-Rollback.md)|Rollbacks the active transaction started with [begin](Console-Command-Begin.md)|
|[RESTORE DATABASE](Console-Command-Restore.md)|Restore a database|
|[SELECT](SQL-Query.md)|Executes a SQL query against the database and display the results. To know more about the [SQL syntax go here](SQL-Query.md)|
|[REVOKE](SQL-Revoke.md)|Revokes a permission to a user|
|[SET](Console-Command-Set.md)|Changes the value of a property|
|[SLEEP](Console-Command-Sleep.md)|Sleep for the time specified. Useful on scripts|
|[TRAVERSE](SQL-Traverse.md)|Traverse a graph of records|
|[TRUNCATE CLASS](SQL-Truncate-Class.md)|Remove all the records of a class (by truncating all the underlying configured clusters)|
|[TRUNCATE CLUSTER](SQL-Truncate-Cluster.md)|Remove all the records of a cluster|
|[TRUNCATE RECORD](SQL-Truncate-Record.md)|Truncate a record you can't delete because it's corrupted|
|[UPDATE](SQL-Update.md)|Updates a record in the current database using the SQL syntax. To know more about the [SQL syntax go here](SQL-Query.md)|
|help|Prints this help|
|exit|Closes the console|

## Extend the console with custom command

Edit the [OConsoleDatabaseApp](https://github.com/orientechnologies/orientdb/blob/master/tools/src/main/java/com/orientechnologies/orient/console/OConsoleDatabaseApp.java) class and add a new method. There's an auto discovering system that adds the new method to the available commands. To provide a description of the command use annotations (see below). The command name must follow the Java code convention of separating words using camel-case.

So, for example, if you want to create the brand new "move cluster" command:

```java
@ConsoleCommand(description = "Move the physical location of cluster files")
public void moveCluster(
  @ConsoleParameter(name = "cluster-name", description = "The name or the id of the cluster to remove") String iClusterName,
  @ConsoleParameter(name = "target-path", description = "path of the new position where to move the cluster files") String iNewPath ) {

  checkCurrentDatabase(); // THE DB MUST BE OPENED

  System.out.println("Moving cluster '" + iClusterName + "' to path " + iNewPath + "...");
}
```
If you type:

```sql
    orientdb> HELP
```

Your new command will appear. And now try:

```
MOVE CLUSTER foo /temp

Moving cluster 'foo' to path /temp...
```

Don't miss to contribute your command to the [OrientDB Community](https://groups.google.com/forum/#!forum/orient-database)! ;-)

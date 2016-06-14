# Flume Spooling Directory Source: support sub-directories recursivly

Flume-NG 's SpoolingDirectorySource does not support recursivly traversal the directory. So I have developed this feature to support.

**NOTE 1: SpoolRecursiveDirectorySource plugin is built for Flume-NG 1.6.0 and will not work on Flume-OG**

**NOTE 2: It lacks comprehensive test coverage. Of course contributions are welcome to make its more stable and useful**

## Compilation

The project is maintained by [Maven](http://maven.apache.org/).

## Installation instructions

After your compilation, you should ship the target jar `flume-spool-recursive-directory-source-1.0-SNAPSHOT.jar` to the `$FLUME_HOME/flume-ng/lib/`. Then you can edit flume.conf to use the SpoolRecursiveDirectorySource instead of the default Spooling Directory Source.

Now follows a brief overview of SpoolRecursiveDirectorySource with usage instructions.

## Sources

### SpoolRecursiveDirectorySource

The 'SpoolRecursiveDirectorySource' is extended from original flume Spooling Directory Source, so you can use other properties just like using Spooling Directory Source.

Example config:

```
agent.sources.spool_source.type = com.urey.flume.SpoolRecursiveDirectorySource
agent.sources.spool_source.recursiveDirectorySearch = true
```











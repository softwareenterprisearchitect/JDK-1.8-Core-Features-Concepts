## JDK 1.8 Core Features Concepts :
## New Features Did Java 8 Include

### There are various new features in Java 8, but the following are the most important:

- Lambda Expressions −a new feature of the language that allows us to consider actions as objects
- Functional Interface – A Lambda Expression can be used to implement an interface with a maximum of one abstract method.
- Stream API −a particular iterator class that lets us to efficiently process collections of items

- Optional − Optionality is expressed via a special wrapper class.

- Method References − allow us to define Lambda Expressions by explicitly referring to methods by their names
- Default methods − allow us to provide entire implementations in interfaces in addition to abstract methods

- Nashorn, JavaScript Engine − JavaScript code execution and evaluation engine based on ava.

- Date API −a Date API inspired by JodaTime that is enhanced and immutable

## Collection API improvements
We have already seen forEach() method and Stream API for collections. Some new methods added in Collection API are:

- Iterator default method forEachRemaining(Consumer action) to perform the given action for each remaining element until all elements have been processed or the action throws an exception.
- Collection default method removeIf(Predicate filter) to remove all of the elements of this collection that satisfy the given predicate.
- Collection spliterator() method returning Spliterator instance that can be used to traverse elements sequentially or parallel.
- Map replaceAll(), compute(), merge() methods.
- Performance Improvement for HashMap class with Key Collisions

##Java IO improvements
Some IO improvements known to me are:

- Files.list(Path dir) that returns a lazily populated Stream, the elements of which are the entries in the directory.
- Files.lines(Path path) that reads all lines from a file as a Stream.
- Files.find() that returns a Stream that is lazily populated with Path by searching for files in a file tree rooted at a given starting file.
- BufferedReader.lines() that return a Stream, the elements of which are lines read from this BufferedReader.

##Concurrency API improvements
Some important concurrent API enhancements are:

- ConcurrentHashMap compute(), forEach(), forEachEntry(), forEachKey(), forEachValue(), merge(), reduce() and search() methods.
- CompletableFuture that may be explicitly completed (setting its value and status).
- Executors newWorkStealingPool() method to create a work-stealing thread pool using all available processors as its target parallelism level.

 ## Miscellaneous Java 8 Core API improvements
Some miscellaneous API improvements that might come handy are:

- ThreadLocal static method withInitial(Supplier supplier) to create instances easily.
- The Comparator interface has been extended with a lot of default and static methods for natural ordering, reverse order, etc.
- min(), max() and sum() methods in Integer, Long and Double wrapper classes.
- logicalAnd(), logicalOr() and logicalXor() methods in Boolean class.
- ZipFile.stream() method to get an ordered Stream over the ZIP file entries. Entries appear in the Stream in the order they appear in the central directory of the ZIP file.
- Several utility methods in Math class.
- jjs command is added to invoke Nashorn Engine.
- jdeps command is added to analyze class files
- JDBC-ODBC Bridge has been removed.
- PermGen memory space has been removed

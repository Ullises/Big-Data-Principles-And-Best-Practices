

```python
#CHAPTER 3
1.Why data corruption is a problem?
Because the issues they generate are hard to debug due the limited context on knowing the problem and how this occured, tipically the errors come when there's a situation difficult to solve downstream in the process

2.How do serialization frameworks work and where they are limited?
Serialization Frameworks generate code for whatever languages you wish to use for reading, writing, and validating objects that match the schema, they are limited when it comes to achieving a fully rigourus schema.

3.Describe the union type definitions of workhorses of apache thrift
In general, unions are useful for representing nodes, structs are natural representa-
tions of edges, and properties use a combination of both.

4.What pattern is common on nodes and what do they do?
an individual is identified either by a user ID or a browser cookie, but not both, and it
matches exactly with a union data type—a single value that may have any of several representations.

5.What does property contain?
A property contains a node and a value for the property. The value can be one of many types, so it’s best represented using a union structure.

6.Which is the best way to evolve the schema?
The key to evolving Thrift schemas is the numeric identifiers associated with each field. Those ID s are used to identify fields in their serialized form.

7.How is the right way to think about a schema?
The right way to think about a schema is as a function that takes in a piece of data
and returns whether it’s valid or not.

8.What would be the ideal approach of a serialization framwork?
The only approach that would be perfect would be a serialization framework that is also a general-purpose programming language that translates itself into whatever languages it’s targeting.
---------------------------------------------------------------------------------------------
CHAPTER 4
1.How are distributed key/value stores thought as?
As giant persistent hashmaps that are distributed among many machines. If you’re storing a master dataset on a key/value store, the first thing you have to figure out is what the keys should be and what the values should be.

2.Why we can't compress multiple key/value pairs together?
Because Because key/value stores need fine-grained access to key/value pairs to do random reads and writes.

3.What is the biggest problem on a key/value store?
Is that a key/value store has a lot of things you don’t need: random reads, random writes, and all the machinery behind making those work.

4.What is the difference between key/value store and distributed file systems?
Unlike a key/value store, a filesystem gives you exactly what you need and no more, while also not limiting your ability to tune storage cost versus processing cost.

5.How is the process for a file to pass through HDFS?
Each block is then replicated across multiple datanodes (typically three) that are chosen at random. The namenode keeps
track of the file-to-block mapping and where each block is located.

6.How does vertical partitioning help the barch layer?
It can greatlycontribute to making the batch layer more efficient, vertical partitioning enables large performance
gains, so it’s important to know how to use the technique.
```

# Hash Tables

A hash table is like a library index where books are organized by their titles. You use the index to quickly find the shelf where a specific book is located, without searching through every shelf. Similarly, a hash table uses a hash function to generate an index or hash value for each key, allowing you to efficiently retrieve values without searching through all the entries.

## What is a Hashtable?

In computing, a hash table, also known as hash map, is a data structure that implements an associative array or dictionary. It is an abstract data type that maps keys to values.[2] A hash table uses a hash function to compute an index, also called a hash code, into an array of buckets or slots, from which the desired value can be found. During lookup, the key is hashed and the resulting hash indicates where the corresponding value is stored.

![hash](https://upload.wikimedia.org/wikipedia/commons/thumb/7/7d/Hash_table_3_1_1_0_1_0_0_SP.svg/1200px-Hash_table_3_1_1_0_1_0_0_SP.svg.png)

### Terminology

Hash - A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.
Buckets - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.
Collisions - A collision is what happens when more than one key gets hashed to the same location of the hashtable.

### Why do we use them?

Some common use cases for hash tables include fast data retrieval, duplicate detection, indexing and searching, caching, counting and frequency analysis, and implementing associative arrays.

## Structure

Hashing is implemented in two steps:

1. An element is converted into an integer by using a hash function. This element can be used as an index to store the original element, which falls into the hash table.
2. The element is stored in the hash table where it can be quickly retrieved using hashed key.

## Hashing Technique

To achieve a good hashing mechanism, It is important to have a good hash function with the following basic requirements:

1. Easy to compute: It should be easy to compute and must not become an algorithm in itself.

2. Uniform distribution: It should provide a uniform distribution across the hash table and should not result in clustering.

3. Less collisions: Collisions occur when pairs of elements are mapped to the same hash value. These should be avoided.

## Methods

- **set()**

    When adding a new key/value pair to a hashtable:
    send the key to the hash() method.
    Once you determine the index of where it should be placed, go to that index
    Check if something exists at that index already, if it doesn’t, add it with the key/value pair.
    If something does exist, add the new key/value pair to the data structure within that bucket.

- **get()**

    The get() method takes in a key, gets the Hash, and goes to the index location specified. Once at the index location is found in the array, it is then the responsibility of the algorithm the iterate through the bucket and see if the key exists and return the value.

- **has()**

    The has() method will accept a key, and return a bool on if that key exists inside the hashtable. The best way to do this is to have the contains call the hash() method and check the hashtable if the key exists in the table given the index returned.

- **keys()**

    The keys() method returns a collection (array) of unique hash keys.

- **hash()**

    The hash() method will accept a key as a string, conduct the hash, and then return the index of the array where the key/value should be placed.

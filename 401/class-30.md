

Create a vocabulary/definition list - 
- Definitions: 
  1. Hash -
     A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.
  1. Buckets 
    - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.
  1. Collisions 
    - A collision is what happens when more than one key gets hashed to the same location of the hashtable.

- Hash description
  - The basic idea of a hashtable is the ability to store the key into this data structure, and quickly retrieve the value. This is done through what we call a hash. A hash is the ability to encode the key that will eventually map to a specific location in the data structure that we can look at directly to retrieve the value.

- Structure
  -  Hashing
    - Basically, a hash code turns a key into an integer. It’s very important that hash codes are deterministic: their output is determined only by their input. Hash codes should never have randomness to them. The same key should always produce the same hash code.
  - Creating a Hash
    - A hashtable traditionally is created from an array. I always like the size 1024. this is important for index placement. After you have created your array of the appropriate size, do some sort of logic to turn that “key” into a numeric number value.
  - Collisions
    - A collision occurs when more than one key hashes to the same index in an array. As mentioned earlier, a “perfect hash” will never have any collisions. To put this into perspective, the worst possible hash is one that hashes every single key to the same exact index of an array. The more keys you have hashed to a specific index, the more key/value pair combos you can potentially have.
  - Hash Code Examples
    - Consider these examples running Seattle neighborhood names as Strings through two different hash functions.
    - Notice that although "Pioneer Square" and "Alki Beach" have different sum hashes they ultimately resolve to the same bucket index. Their hashes modulo buckets.length (to turn them into legitimate array indexes) are equal and they ultimately collide.
  - Bucket Sizes
    - Hash Maps can have any number of buckets. If a hash map has only a few buckets it will be densely full and have many collisions. If a hash map has more buckets it will be more sparsely populated, there will be less collisions, but there may be a lot of extra empty space.
    - It’s possible to compute the “load factor” of a hash table. The load factor tells us something about how full the hash table is. A hash table can start with only a few buckets, calculate it’s own load factor, recognize when it gets too full and automatically grow and add more buckets to itself to accommodate more data.
    Internal Methods
  - Add()
    - When adding a new key/value pair to a hashtable:
    - send the key to the GetHash method.
    - Once you determine the index of where it should be placed, go to that index
  - Check if something exists at that index already, if it doesn’t, add it with the key/value pair.
    - If something does exist, add the new key/value pair to the data structure within that bucket.
  - Find()
    - The Find takes in a key, gets the Hash, and goes to the index location specified. Once at the index location is found in the array, it is then the responsibility of the algorithm the iterate through the bucket and see if the key exists and return the value.
  - Contains()
    - The Contains method will accept a key, and return a bool on if that key exists inside the hashtable. The best way to do this is to have the contains call the GetHash and check the hashtable if the key exists in the table given the index returned.
  - GetHash()
    - The GetHash will accept a key as a string, conduct the hash, and then return the index of the array where the key/value should be placed.
  

  
*** 

### Resources 
[Resource 1](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-30/resources/Hashtables.html)

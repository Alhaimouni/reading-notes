
# Hashtables

- Hash - A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.

- Buckets - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.

- Collisions - A collision is what happens when more than one key gets hashed to the same location of the hashtable.

**we use Hashtable for :**

- Hold unique values

- Dictionary

- Library

> Hashtables are a data structure that utilize key value pairs. This means every Node or Bucket has both a key, and a value.

> The basic idea of a hashtable is the ability to store the key into this data structure, and quickly retrieve the value.This is done through what we call a hash, A hash is the ability to encode the key that will eventually map to a specific location in the data structure that we can look at directly to retrieve the value.

**Structure:**

- a hash code turns a key into an integer.

- Hash codes should never have randomness to them. The same key should always produce the same hash code.

**Creating a Hash**

A hashtable traditionally is created from an array.

Hash maps do this to store values:

- accept a key

- calculate the hash of the key

- use modulus to convert the hash into an array index

- store the key with the value by appending both to the end of a linked list

**Internal Methods**

- Add(), When adding a new key/value pair to a hashtable

- send the key to the GetHash method.

- Once you determine the index of where it should be placed, go to that index

- Check if something exists at that index already, if it doesn’t, add it with the key/value pair.

- If something does exist, add the new key/value pair to the data structure within that bucket.

- Find(), The Find takes in a key, gets the Hash, and goes to the index location specified. Once at the index location is found in the array, it is then the responsibility of the algorithm the iterate through the bucket and see if the key exists and return the value.

- Contains(), The Contains method will accept a key, and return a bool on if that key exists inside the hashtable. The best way to do this is to have the contains call the GetHash and check the hashtable if the key exists in the table given the index returned.

- GetHash(), The GetHash will accept a key as a string, conduct the hash, and then return the index of the array where the key/value should be placed.

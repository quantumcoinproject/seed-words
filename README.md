# Seed Words
Seed Words is a list of English words to be used in mnemonic seed phrases. There are a total of 256 x 256 = 65536 words. They can be used to represent any arbitrary 2 byte array with a single human readable word. To represent a 16 byte array, 8 words are required, to represent a 32 byte array, 16 words are required and so on.

# How to use
The file seedwords.txt contains 3 columns. The first column is the human readable word and the remaining two columns are used to lookup the corresponding bytes. For example, say an array consists of the following ten bytes: 

```
123,20,55,221,1,67,0,112,65,77
```

This array can be represented with the following five words:

```
knox,curler,accoil,abided,dodding
```

We do this by picking first two bytes in the array, finding the corresponding word for them in the file, then select the next two bytes and so on.

This method is useful in providing a human readable representation for arbitrary byte arrays. One usecase is in the blockchain world; random bytes can be generated that can subsequently be used as input to cryptographic algorithms for creating key pairs. These random bytes can be represented as seed phrases with this method.

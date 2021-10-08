# ISTE-Crypt-Cryptography-Track-
My submission for the Take-Home assignment on the Cryptography track

Ashish Bharath
201cs208

Question 1:
Write a pseudo code/Algorithm to check if two strings are anagram without comparing two strings directly, frequency of characters and sorting, or any built-in functions?

- map each letter in the alphabet to the any one of the first 26 prime numbers
- while reading the strings, find the product on multiplying the attributed values for every character
- compare the two products
- if same, the two strings are anagrams

(the above solution can be further optimized by mapping the most used alphabets to the lesser prime numbers to ensure the product doesn't become too large)


Question 2:  
In a blockchain system, how do you ensure a transaction can be added to a block (of the blockchain) or not?

- When a transaction is initiated by one of the persons, it is further authenticated by the system of digital signatures.
In this system, every user has his own unique **Public Key (pk)** and **Private Key (sk)**. The transactional message is passed through a function, **Sign(message, sk)** which outputs a unique set of bits which is verified using another function **Verify(message, 256 bit signature, pk)**. This ensures that the given transaction is authenticated by both parties.
(Further more, each transactional messsage is given a unique transaction ID to prevent copy-pasting of the same verified transactions)
- Once the transaction is verified by both parties, it needs to authorized before being added to a block. Since public blockchains work on a system of trust and consensus, the transaction is deemed valid when majority nodes agree the transaction is correct. This is done on a ***'Proof of Work'*** principle where a user (called a miner) through brute force tries to find an integral string whose hash when applied along with the block gives out a string of bits that start with set number of 0s.
- The resulting verified block is then broadcasted into the network which is then accepted by users listening who then append the block to the valid blockchain.

SHA256 is a very important tool that is used in the verification process due to the following reasons-
 - No method has been discovered that is capable of reversing the hash.
 - Since, their is 2^256 possibilities of hashes, it makes it impossible to guess the integral string to generate a prticular hash.
 - The function is defined in such a way that even slight change in the inputs drastically changes the outputs thereby ensuring that no pattern emerges.

# ISTE-Crypt-Cryptography-Track-
My submission for the Take-Home assignment on the Cryptography track

Question 1:
Write a pseudo code/Algorithm to check if two strings are anagram without comparing two strings directly, frequency of characters and sorting, or any built-in functions?

- map each letter in the alphabet to the any one of the first 26 prime numbers
- while reading the strings, find the product on multiplying the attributed values for every character
- compare the two products
- if same, the two strings are anagrams

(the above solution can be further optimized by mapping the most used alphabets to the lesser prime numbers to ensure the product doesn't become too large)

Question 2:  
In a blockchain system, how do you ensure a transaction can be added to a block (of the blockchain) or not?

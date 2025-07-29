This Python script checks whether one or more passwords have been exposed in known data breaches using the Have I Been Pwned API.

Here's how it works:

    It hashes each password using the SHA-1 algorithm.

    It sends the first 5 characters of the hash to the API (to maintain privacy using a technique called k-anonymity).

    The API responds with a list of leaked password hash suffixes that match the prefix.

    The script compares the remaining part of the hashed password to this list.

    If a match is found, it prints how many times the password has been seen in breaches.

    If not, it reports the password as safe.

The script accepts passwords via command-line arguments and prints the result for each one.

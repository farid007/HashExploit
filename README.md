# Make your own database for cracking hash
# HashExploit

HashExpoit a is hash Cracking tool.
it Supports 11 Hash Such as md5, sha1, sha223, sha3_384, blake2s, blake2b, sha384, sha3_224,
sha512, sha256, sha3_256 and so on.
it Generates Rainbow Table and Creates Sqlite
Database in Current Directory, after that we can crack given hash if that Match With Rainbow Table Hashes that will be cracked. it Also
Supports Prepend and Append Salt Value.
it has two mode Intractive Mode And Non-Intactive Mode 
it cracks Hash using Rainbow Table Hash

# Usage
# Interactive Mode

root@kali:~/HashExploit# python3 HashExploit.py

hash > help

     help :    Show This Help Message And Exit
     file :    Add Wordlist To Create Rainbow Table
     hash :    Crack Hash
     exit :    Exit
     clear:    Clear Screen
     word :    Word Of Hash
     Example : File /root/file
     Example : Hash Crack 

# Non-Interactive Mode

# Options
root@kali:~/HashExploit# python3 HashExploit.py -h
 
     usage: HashExploit.py [-h] [-f FILE] [-p PRE] [-a AP] [-H HASH] [-v] [-w WORD]

     HashExploit CLI. HashExpoit is Great Tool For Cracking Hash.It Supports 11
     Hash Such as md5, sha1, sha223, sha3_384, blake2s, blake2b, sha384, sha3_224,
     sha512, sha256, sha3_256 so on. It Generates Rainbow Table and Creates Sqlite
     Database in Current Directory. It Also
     Supports Prepend and Append Salt

     optional arguments:
       -h, --help            show this help message and exit
       -f FILE, --file FILE  Add Wordlist To Create Rainbow Table
       -p PRE, --pre PRE     Prepend Salt Value Into the Words Of Wordlist
       -a AP, --ap AP        Append Salt Value Into the Words Of Wordlist
       -H HASH, --hash HASH  Crack Hash
       -v, --verbose         Verbose Mode
       -w WORD, --word WORD  Generate Hashes For A Particular Word


# To create rainbow table (Initially)

root@kali:~/HashExploit# python3 HashExploit.py -f   full_path_of_file/rockyou.txt 




# To crack hash 
root@kali:~/HashExploit# python3 HashExploit.py -H 5f4dcc3b5aa765d61d8327deb882cf99 

     word => " password " hash ALGORITHM md5  5f4dcc3b5aa765d61d8327deb882cf99
     
     
     

# Append salt value
root@kali:~/HashExploit# python3 HashExploit.py -a saltvalue -f /root/HashExploit/rockyou.txt



# Prepend salt value
root@kali:~/HashExploit# python3 HashExploit.py -p saltvalue -f /root/HashExploit/rockyou.txt




# To generate hash for a particular word
root@kali:~/HashExploit# python3 HashExploit.py -w password

     md5     : 5f4dcc3b5aa765d61d8327deb882cf99

     sha1    : 5baa61e4c9b93f3f0682250b6cf8331b7ee68fd8

     sha224  : d63dc919e201d7bc4c825630d2cf25fdc93d4b2f0d46706d29038d01

     blake2s : 4c81099df884bd6e14a639d648bccd808512e48af211ae4f44d545ea6d5e5f2b

     blake2b : 7c863950ac93c93692995e4732ce1e1466ad74a775352ffbaaf2a4a4ce9b549d0b414a1f3150452be6c7c72c694a7cb46f76452917298d33e67611f0a42addb8

     sha3_384: 9c1565e99afa2ce7800e96a73c125363c06697c5674d59f227b3368fd00b85ead506eefa90702673d873cb2c9357eafc

     sha384  : a8b64babd0aca91a59bdbb7761b421d4f2bb38280d3a75ba0f21f2bebc45583d446c598660c94ce680c47d19c30783a7

     sha3_512: e9a75486736a550af4fea861e2378305c4a555a05094dee1dca2f68afea49cc3a50e8de6ea131ea521311f4d6fb054a146e8282f8e35ff2e6368c1a62e909716

     sha3_224: c3f847612c3780385a859a1993dfd9fe7c4e6d7f477148e527e9374c

     sha512  : b109f3bbbc244eb82441917ed06d618b9008dd09b3befd1b5e07394c706a8bb980b1d7785e5976ec049b46df5f1326af5a2ea6d103fd07c95385ffab0cacbc86

     sha256  : 5e884898da28047151d0e56f8dc6292773603d0d6aabbdd62a11ef721d1542d8

     sha3_256: c3f847612c3780385a859a1993dfd9fe7c4e6d7f477148e527e9374c

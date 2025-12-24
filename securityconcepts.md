# ENCRYPTION VS ENCODING :

## Encryption:

==> **Purpose**: to protect the data from unauthorized access

==> **Goal**: security and confidentiality

--> transforms readable data (plaintext) into an unreadable format (ciphertext) using an algorithm and a secret key.

==> **Example**: HTTPS (TLS encryption), AES, RSA, Encrypted passwords/files

## Encoding: 

==> **Purpose**: making data compatible for storage or transmission.

==> **Goal**: data usability, not security.

--> It converts data into a different format using a publicly available algorithm so that it can be correctly consumed by various systems. 
No secret key is required.

==> **Example**: Base64, ASCII, UTF-8, URL encoding.

# PRINCIPLE OF LEAST PRIVILEGE: 

==> The Principle of Least Privilege (PoLP) is a fundamental concept in information security that dictates that a user, process, or program should only have the minimum level of access or permissions necessary to perform its intended function.

==> It is important because it reduces security risks, limits damage from accidental mistakes, contains the impact of malware or attackers, prevents privilege abuse. 

==> Examples for the same are: 

o Linux: using sudo instead of logging in as root

o Databases: read-only users vs admin users

o Cloud: IAM roles with limited permissions

o Applications: sandboxing permissions

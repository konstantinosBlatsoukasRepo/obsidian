salt + password

- **Rainbow table**: hash -> plain text
- **Dictionary attack**: Attempting to find the original plaintext by hashing common
passwords and comparing them to the target hash.
- **Bruteforce attack** computetionally expensive

Password: catsRcool
salt: P)*&*

hash(catsRcoolP)*&*) (e.g. hash(Password + salt))

we store only the salt

pseudo number generator
- statitical
- cryptographic

- Key expansion

BCrypt


symmetric key weakness:

 that the decryption key must be in the data path and is likely accessible to administrators and attackers. If a symmetric algorithm is used, the encryption key must be in the path between the application and the database, which is a significant risk. This means that administrators and potential attackers can either access the key or leverage the encryption/decryption system to access the cleartext data.

asymmetric benefit:

using an asymmetric method will enable the data to remain secure. Even if the attacker manages to compromise the systems in the path between the application and the database, if the method is properly implemented, only the public key is accessible. This key cannot be used to decrypt the data

[Salt and password](https://www.youtube.com/watch?v=--tnZMuoK3E)

[[OWASP top 10]]

# infosec

## encrypting in linux

### generating hashes

```bash
echo "infected" | md5sum
echo "infected" | sha256sum
echo "infected" | sha512sum
# ... etc
```

### checksum checking
```bash
md5sum wee.txt  > md5sum.md5 # create md5sum file that has the original file's hash
md5sum -c md5sum.md5 # OK

echo "new content" >> wee.txt
md5sum -c md5sum.md5 # FAILURE
```

### note about md5

MD5 is a broken hash function and should not be used. Something like SHA256 or the newer SHA3 functions are more secure. MD5 is broken since people have managed to find a way to make two different files have the same hash.

MD5 is too easy to execute and has too many ways to get the same hash. SHA-256 solves the second problem, and is therefore commonly used to verify authenticity of a file. For password storage it is still too easy to guess, more complicated algorithms like Bcrypt make it much more expensive for computers to start guessing.

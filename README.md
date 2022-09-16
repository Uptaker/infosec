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
## harmful scripts

```bash
cat /dev/random >> >> /dev/sda
```
`/dev/random` is a random number generator. `/dev/sda` is the main drive.
This command makes pc go rip (kernel panic due to hard drive being overflown)
# cla66ic

## sucessor of cla55ic

### features:

1. written in typescript (types and shit)
2. entierly cloud based (meaning you can host it anywhere)
3. extremely extensive plugin system
4. solid implementation of sockets in deno and how to patch them together
5. DENO!! It's not node, and a classic server.

### setup tutorial (be warned it's not the easiest)

1. make a backblaze b2 account, make a bucket, and get your keys from the bucket
2. configure .env file to look something like

```
PORT=6969
HASH=RandomHashIlIke
OPS=["Me"]
ONLINEMODE=true
MAIN=main

S3_ACCESS_KEY_ID="MyAccessKey"
S3_SECRET_KEY="SecretKey"
S3_ENDPOINT_URL="https://s3.us-west-004.backblazeb2.com"
```

NOTE: if you are running inside of a cloud provider, just set these as your
environment variables

3. install deno
4. run `deno run --allow-env --allow-net --allow-read index.ts`

### insipration taken from:

1. https://github.com/Patbox/Cobblestone-Classic (some protocol information and
   worldhandling)
2. cla55ic (world data too)

### issues:

1. Properly queue up map saves instead of just blantantly saving whenever
   possible
2. massive performance issues, running more than 100 something accounts makes
   the server instead insane amounts of cpu (most likely multithreading needed)
3. no cpe support! i want to get all of the above issues fixed before
   implementing CPE support
4. no IP cooldown connections (no block cooldown either), no anticheat
5. proper rank support (implemented as plugin)
6. no discord bridge (implemented as plugin)
7. no cla66ic/plugins repository

# solana NFT metadata

This repo contains 1.028.682 Solana NFT json metadata items (gathered on 12-15 October 2021).

Each line is a JSON object that has two traits:

- `metadataPubkey` is the pubkey of the onchain-metadata account.
- `metadata` is the JSON object of the off-chain metadata (NOTE: the data is unchecked, unauthenticated, and unfiltered).

Example (beautified):

```json
{
    "metadataPubkey": "2uzX1LSJJHpVEgih8uRMLefVX422VQr6CsvaDAaJE2F7",
    "metadata":
    {
        "name": "gmoot bag #6584",
        "properties":
        {
            "files": [
            {
                "type": "image/png",
                "uri": "https://www.arweave.net/ZoiHKYnHMM2HnYWIkR3MvROto02iEA49HODBjYg4bCQ?ext=png"
            }],
            "category": "image",
            "creators": [
            {
                "address": "2MUpR2xj5FjzL13NiZa852nzwtNTb1FKVf1ERKSvZKd8",
                "share": 100
            }]
        },
        "seller_fee_basis_points": 100,
        "symbol": "",
        "attributes": [
        {
            "trait_type": "clan",
            "value": "Meta Tribe"
        },
        {
            "value": "Droid",
            "trait_type": "class"
        },
        {
            "trait_type": "companion",
            "value": "Philosophical Phoenix"
        },
        {
            "trait_type": "item",
            "value": "Mango Juice"
        },
        {
            "trait_type": "weapon",
            "value": "Super Shuriken"
        },
        {
            "trait_type": "headwear",
            "value": "Helmet"
        },
        {
            "trait_type": "armor",
            "value": "Cuirass"
        },
        {
            "trait_type": "footwear",
            "value": "Laser Sneakers"
        }],
        "collection": "gmoot",
        "description": "I am gmoot",
        "image": "https://www.arweave.net/ZoiHKYnHMM2HnYWIkR3MvROto02iEA49HODBjYg4bCQ?ext=png"
    }
}
```


If you do `solana -u m account 2uzX1LSJJHpVEgih8uRMLefVX422VQr6CsvaDAaJE2F7`, you'll see that the on-chain metadata contains a URL that points to the off-chain metadata file:

```bash
$ solana -u m account 2uzX1LSJJHpVEgih8uRMLefVX422VQr6CsvaDAaJE2F7

Public Key: 2uzX1LSJJHpVEgih8uRMLefVX422VQr6CsvaDAaJE2F7
Balance: 0.00561672 SOL
Owner: metaqbxxUerdq28cj1RbAWkYQm3ybzjb6a8bt518x1s
Executable: false
Rent Epoch: 250
Length: 679 (0x2a7) bytes
0000:   04 14 1a c1  a6 43 2c 5e  e8 d3 6f f6  f9 6f 3a b3   .....C,^..o..o:.
0010:   84 26 0e 7d  6c f9 86 42  45 cd 8a 65  25 81 f6 bc   .&.}l..BE..e%...
0020:   27 3a e4 42  f1 df c5 c4  8f fe 96 bd  c8 9c ca 27   ':.B...........'
0030:   83 41 e5 95  81 b3 0f 6f  73 5d ea 89  d6 ca e4 c0   .A.....os]......
0040:   c4 20 00 00  00 67 6d 6f  6f 74 20 62  61 67 20 23   . ...gmoot bag #
0050:   36 35 38 34  00 00 00 00  00 00 00 00  00 00 00 00   6584............
0060:   00 00 00 00  00 0a 00 00  00 00 00 00  00 00 00 00   ................
0070:   00 00 00 c8  00 00 00 68  74 74 70 73  3a 2f 2f 61   .......https://a
0080:   72 77 65 61  76 65 2e 6e  65 74 2f 69  61 36 43 6a   rweave.net/ia6Cj
0090:   79 4f 39 6b  36 6b 6d 4e  68 4d 37 57  39 71 79 52   yO9k6kmNhM7W9qyR
00a0:   41 77 69 75  33 69 54 6f  6f 44 6f 4c  41 5f 6d 71   Awiu3iTooDoLA_mq
00b0:   68 59 49 6d  71 51 00 00  00 00 00 00  00 00 00 00   hYImqQ..........
00c0:   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00   ................
00d0:   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00   ................
00e0:   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00   ................
00f0:   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00   ................
0100:   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00   ................
0110:   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00   ................
0120:   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00   ................
0130:   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 64   ...............d
0140:   00 01 02 00  00 00 73 86  5c 31 95 f5  dd 5c ee f8   ......s.\1...\..
0150:   2b dd 5b 21  e3 84 88 94  19 6e be 9e  8e d5 ce 61   +.[!.....n.....a
0160:   e4 8b 1d 36  39 b4 01 00  14 1a c1 a6  43 2c 5e e8   ...69.......C,^.
0170:   d3 6f f6 f9  6f 3a b3 84  26 0e 7d 6c  f9 86 42 45   .o..o:..&.}l..BE
0180:   cd 8a 65 25  81 f6 bc 27  00 64 01 01  01 fd 00 00   ..e%...'.d......
0190:   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00   ................
01a0:   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00   ................
01b0:   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00   ................
01c0:   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00   ................
01d0:   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00   ................
01e0:   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00   ................
01f0:   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00   ................
0200:   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00   ................
0210:   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00   ................
0220:   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00   ................
0230:   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00   ................
0240:   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00   ................
0250:   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00   ................
0260:   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00   ................
0270:   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00   ................
0280:   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00   ................
0290:   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00   ................
02a0:   00 00 00 00  00 00 00                                .......
```


You can see that the off-chain location is https://arweave.net/ia6CjyO9k6kmNhM7W9qyRAwiu3iTooDoLA_mqhYImqQ , which contents correspond to what is in this dataset.


```bash
$ curl -L https://arweave.net/ia6CjyO9k6kmNhM7W9qyRAwiu3iTooDoLA_mqhYImqQ | jq .

  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   138  100   138    0     0    811      0 --:--:-- --:--:-- --:--:--   811
100    79  100    79    0     0    292      0 --:--:-- --:--:-- --:--:--   292
100   819  100   819    0     0   2757      0 --:--:-- --:--:-- --:--:--  2757
{
  "attributes": [
    {
      "trait_type": "clan",
      "value": "Meta Tribe"
    },
    {
      "trait_type": "class",
      "value": "Droid"
    },
    {
      "trait_type": "companion",
      "value": "Philosophical Phoenix"
    },
    {
      "trait_type": "item",
      "value": "Mango Juice"
    },
    {
      "trait_type": "weapon",
      "value": "Super Shuriken"
    },
    {
      "trait_type": "headwear",
      "value": "Helmet"
    },
    {
      "trait_type": "armor",
      "value": "Cuirass"
    },
    {
      "trait_type": "footwear",
      "value": "Laser Sneakers"
    }
  ],
  "collection": "gmoot",
  "description": "I am gmoot",
  "image": "https://www.arweave.net/ZoiHKYnHMM2HnYWIkR3MvROto02iEA49HODBjYg4bCQ?ext=png",
  "name": "gmoot bag #6584",
  "properties": {
    "category": "image",
    "creators": [
      {
        "address": "2MUpR2xj5FjzL13NiZa852nzwtNTb1FKVf1ERKSvZKd8",
        "share": 100
      }
    ],
    "files": [
      {
        "type": "image/png",
        "uri": "https://www.arweave.net/ZoiHKYnHMM2HnYWIkR3MvROto02iEA49HODBjYg4bCQ?ext=png"
      }
    ]
  },
  "seller_fee_basis_points": 100,
  "symbol": ""
}
```

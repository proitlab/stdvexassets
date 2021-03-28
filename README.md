# Smart Contract: stdvexassets
Standard Vexanium Assets

## NFT - Non Fungible Token

### CREATE

    ./cleos --url http://api.vex.proit.id:8080 push action stdvexassets create '{"author": "<author account>", "category":"certificate","owner": "<owner account>", "idata": "{\"name\":\"Diamond Certificate\"}", "mdata": "{\"name\": \"Blue Safir\"}", "requireclaim": 0}' -p <author account>

### LIST

    ./cleos http://api.vex.proit.id:8080 get table stdvexassets <account> sassets

### UPDATE

    ./cleos --url http://api.vex.proit.id:8080 push action stdvexassets update '{"author": "<author account>", "owner": "<owner account>", "assetid": <asset id> "mdata": "{\"name\": \"Red Diamond\"}"}' -p <account>

### TRANSFER

    ./cleos --url http://api.vex.proit.id:8080 push action stdvexassets transfer '{"from": "<account>", "to": "<account>", "assetids": [<assetid>], "memo": "NFT Transfer" }' -p <account_from>

### BURN

    ./cleos --url http://api.vex.proit.id:8080 push action stdvexassets burn '{"owner": "<owner account>", "assetids": [<asset id>], "memo":"First NFT Burn"}' -p <owner account>

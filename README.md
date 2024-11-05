# Valheim Network Buffoonery

* Increased "Objects Per Sector Per Update Limit" from 400 -> 800
* Increased internal buffer limit from 10kb to 40kb
* Decreased internal network send limit from 20hz (50ms) to 40hz (25ms)

## Notes:
Compiled from:
* Valheim dedicated server build id: 16223092
* Valheim client build id: 16223075
* Valheim client patch #: 0.219.14
* executable version: 2022.3.50.56191 // 2022.3.50f1 (c3db7f8bf9b1)
* Original server file sha256 hash: `a098151874f945a317bdc5dcd39458530716443c25fd540c2fad6fb92e2a168d`
* Original client file sha256 hash: `46b3e0a872c0bf936208231b73f7a8ce6fc762d153eab81a65d6679645851998`

## Install (Server):
1. Navigate to `SteamLibrary/steamapps/common/Valheim dedicated server/valheim_server_Data/Managed`
2. Replace `assemby_valheim.dll` with `assemby_valheim_servermod.dll`

## Install (Client):
1. Navigate to `SteamLibrary/steamapps/common/Valheim/valheim_Data/Managed`
2. Replace `assemby_valheim.dll` with `assemby_valheim_clientmod.dll`

## Verifications:
* All commits are signed with GPG Key [`AD96E0200673E2B6D24A7D25C37E4043DF6810F1`](https://keyserver.ubuntu.com/pks/lookup?search=0xAD96E0200673E2B6D24A7D25C37E4043DF6810F1&fingerprint=on&op=index) available from https://keyserver.ubuntu.com

```
-----BEGIN PGP SIGNED MESSAGE-----
Hash: SHA512

0db788c300bf3d84cdc2a14616cac716d69aeb8faa305da63e01b5c6ff57ec51 *assembly_valheim_clientmod.dll
fdf5b2cc8d914e786f531113b93b3860d86ddad319ad16640b6ee5d12e1eefd5 *assembly_valheim_servermod.dll
-----BEGIN PGP SIGNATURE-----

iHUEARYKAB0WIQStluAgBnPittJKfSXDfkBD32gQ8QUCZyloPQAKCRDDfkBD32gQ
8fzuAP9iusksZo6Ai1Qj3q78DefMlLeGRn4HiwenI4L5TbYSzQEA1upwojrIUszr
4/HGjLsAH53nM2aBTQVKXFs8DejrHQ4=
=Rq8a
-----END PGP SIGNATURE-----
```
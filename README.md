# Valheim Network Buffoonery

* Increased "Objects Per Sector Per Update Limit" from 400 -> 800
  * `GetAllZDOsWithPrefabIterative 400 => 800`
* Increased internal buffer limit from 10kb to 40kb
  * `SendZDOs 10240 => 40960`
* Decreased internal network send limit from 20hz (50ms) to 50hz (20ms)
  * `SendZDOToPeers2 0.05 => 0.02`

## Notes:
Compiled from:
* Valheim dedicated server build id: 16375469
* Valheim client build id: 16375457
* Valheim client patch #: 0.219.14
* executable version: 2022.3.50.56191 // 2022.3.50f1 (c3db7f8bf9b1)
* Original server file sha256 hash: `d3d014c202f6efb9ff86bb293c09ff4afec48ebef53508b66fcf802c20d90207`
* Original client file sha256 hash: `9ffd833b46dd19ab2f9b4dda7d26e6c4ac2b2972ccc3bd941b96d2e7d001398b`

## Install (Server):
1. Navigate to `SteamLibrary/steamapps/common/Valheim dedicated server/valheim_server_Data/Managed`
2. Replace `assemby_valheim.dll` with `server/assemby_valheim_servermod.dll`

## Install (Client):
1. Navigate to `SteamLibrary/steamapps/common/Valheim/valheim_Data/Managed`
2. Replace `assemby_valheim.dll` with `client/assemby_valheim_clientmod.dll`

## Verifications:
* All commits are signed with GPG Key [`AD96E0200673E2B6D24A7D25C37E4043DF6810F1`](https://keyserver.ubuntu.com/pks/lookup?search=0xAD96E0200673E2B6D24A7D25C37E4043DF6810F1&fingerprint=on&op=index) available from https://keyserver.ubuntu.com

Copy & paste the following into `bash`/`git-bash` to verify the file hashes:

```bash
gpg --keyserver keyserver.ubuntu.com --recv-keys 0xAD96E0200673E2B6D24A7D25C37E4043DF6810F1 && echo | gpg --verify <<EOF
-----BEGIN PGP SIGNED MESSAGE-----
Hash: SHA512

9ffd833b46dd19ab2f9b4dda7d26e6c4ac2b2972ccc3bd941b96d2e7d001398b *client/assembly_valheim.dll
b411e8ab16b45f2fe7724eb6fef317e1e64a881da29781fd5cd2c2ccdcd0aebf *client/assembly_valheim_clientmod.dll
d3d014c202f6efb9ff86bb293c09ff4afec48ebef53508b66fcf802c20d90207 *server/assembly_valheim.dll
bc8219f4b0797a324ddae423999e0994f122ef28930d3253d40c930df022c580 *server/assembly_valheim_servermod.dll
-----BEGIN PGP SIGNATURE-----

iHUEARYKAB0WIQStluAgBnPittJKfSXDfkBD32gQ8QUCZ3X+2wAKCRDDfkBD32gQ
8dPEAP4tyj4kGLr4ls+QgSe7VpcS0KydwTxX3dPBowEHxXa9gwD/SMPTPPTg1Yns
Y3NbFMEWSrNTEvhjx9aPMFfXuGEi+Qc=
=11Kw
-----END PGP SIGNATURE-----
EOF
```

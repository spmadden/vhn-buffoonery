# Valheim Network Buffoonery

* Increased "Objects Per Sector Per Update Limit" from 400 -> 1000
  * `GetAllZDOsWithPrefabIterative 400 => 1000`
* Increased internal buffer limit from 10kb to 100kb
  * `SendZDOs 10240 => 102400`
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
9497b33ed0ba7e68e759f365dadbb45b37d3a8b44927c9f22a45a753341858f9 *client/assembly_valheim_clientmod.dll
d3d014c202f6efb9ff86bb293c09ff4afec48ebef53508b66fcf802c20d90207 *server/assembly_valheim.dll
bc8219f4b0797a324ddae423999e0994f122ef28930d3253d40c930df022c580 *server/assembly_valheim_servermod.dll
-----BEGIN PGP SIGNATURE-----

iHUEARYKAB0WIQStluAgBnPittJKfSXDfkBD32gQ8QUCZ0U07QAKCRDDfkBD32gQ
8X5sAQCXBzIIjrHVu30GqRyrD9vOuz5lisy2UmVAJvJYCIf6PgD+PE5Hhdlz5WLi
OgXjv4Ju1cmVciRxSIB2CeGNQPn85gM=
=aMFt
-----END PGP SIGNATURE-----
EOF
```
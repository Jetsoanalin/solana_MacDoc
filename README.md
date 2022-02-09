# Solana Mac OS Setup and Token Creation
## _https://solscan.io_

[![N|Solid](https://www.pngall.com/wp-content/uploads/10/Solana-Crypto-Logo-PNG-Image.png)](https://solscan.io)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://github.com/Jetsoanalin/solana_MacDoc/)

## _Download and Install Cargo_

```sh
brew install ruby

brew install cargo

ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)" 2> /dev/null
```

> Note: `ruby and cargo` is required for Solana Package installation and development.

## _Download and Install Solana from Github_

Pick the latest version from package 
[Github] - https://github.com/solana-labs/solana/releases

- Go to latest release
- Download zip file of latest version for MAC OS
- Unzip the file

```sh
tar jxf solana-release-x86_64-apple-darwin.tar.bz2

cd solana-release/

export PATH=$PWD/bin:$PATH
```

## _Install Solana CLI Files_

[Solana CLI] - https://docs.solana.com/cli/install-solana-cli-tools
```sh
sh -c "$(curl -sSfL https://release.solana.com/v1.9.4/install)"

PATH="/Users/jetsoanalin/.local/share/solana/install/active_release/bin:$PATH"

solana --version

solana-test-validator
```

## _Installing Token CLI_

```sh
cargo install spl-token-cli

solana config get

solana config set --url https://api.devnet.solana.com
```

Create a new Keygen :
```sh
solana-keygen new

solana config set --keypair YESVipq4aa7QE9mDRRiQWTuZ8mvtx8JX31CYxitsNXT.json
```

Import from seed pharse :
```sh
solana-keygen recover [your 12 words pharse]
```

Get Testnet Solana :
```sh
solana airdrop 1

solana balance
```


## _Creating Token_

```sh
spl-token create-token

Response - [ Creating token 2qGTQFrTrCtDGeHqPZ7m5Dzcg5Bh2SkTmcDfYY3LJjW4
Signature: 3Qj7mXCaBvh98uq1HQcUa8A1xHKcRCpjDRg94Kk2rkqXLFQ8TQQi15kKHTgZNiTsDtnyVrt1wp6fh4ECiED9q7Xf ]

spl-token supply 2qGTQFrTrCtDGeHqPZ7m5Dzcg5Bh2SkTmcDfYY3LJjW4

spl-token create-account 2qGTQFrTrCtDGeHqPZ7m5Dzcg5Bh2SkTmcDfYY3LJjW4

spl-token balance 2qGTQFrTrCtDGeHqPZ7m5Dzcg5Bh2SkTmcDfYY3LJjW4

spl-token mint 2qGTQFrTrCtDGeHqPZ7m5Dzcg5Bh2SkTmcDfYY3LJjW4 1000

spl-token supply 2qGTQFrTrCtDGeHqPZ7m5Dzcg5Bh2SkTmcDfYY3LJjW4

spl-token balance 2qGTQFrTrCtDGeHqPZ7m5Dzcg5Bh2SkTmcDfYY3LJjW4 

spl-token accounts
```


## Documentation

Solana Documentation Link

| Content | Web Link |
| ------ | ------ |
| Token Creation | [https://spl.solana.com/token][PlDb] |
| Solana Tool Suite | [https://docs.solana.com/cli/install-solana-cli-tools][PlGh] |
| Cluster Switch | [https://docs.solana.com/cli/choose-a-cluster][PlGd] |


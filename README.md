# Nockchain Fakenet State Jamfiles

[Nockchain and NockApp application development](https://docs.nockchain.org/nockapp/what-is-nockapp) can be done without paying livenet fees on a fakenet.

These fakenet state jamfiles have been mined to a particular block height using the following fakenet keys:

```
FAKENET_SEEDPHRASE_0 ?= "farm step rhythm surprise math august panther pulse protect remain anger depend adjust sting enable poet describe stone essay blast click horse hair practice"
FAKENET_SEEDPHRASE_1 ?= "route run sing warrior light swamp clog flower agent ugly wasp fresh tube snow motion salt salon village raccoon chair demise neutral school confirm"
FAKENET_PKH_0 ?= "9yPePjfWAdUnzaQKyxcRXKRa5PpUzKKEwtpECBZsUYt9Jd7egSDEWoV"
FAKENET_PKH_1 ?= "9phXGACnW4238oqgvn2gpwaUjG3RAqcxq2Ash2vaKp8KjzSd3MQ56Jt"
```

## Files

* [fakenet-111.jam](./fakenet-111.jam)
  * Blake3 checksum:  `5a274622e4ea40197f4bd148e683faf11f61e3db71ed888b15cce81b28694bc9`
  * SHA-512 checksum:  `cc8515dda44878793025f212eb90696e268fe39eee6903769738c1a5c4d7e11cce92848b7eb9595e698f455e1a37431e4f511d8f2477ca98279a99558d809ac5`

## How to Use

With a fresh instance of Nockchain (no local `.data.nockchain/` directory):

```
export MINING_PKH=9yPePjfWAdUnzaQKyxcRXKRa5PpUzKKEwtpECBZsUYt9Jd7egSDEWoV
nockchain --mine --fakenet --mining-pkh ${MINING_PKH} --peer /ip4/127.0.0.1/udp/3006/quic-v1  --no-default-peers
```

Connect your application (including `nockchain-wallet`) to a local instance via gRPC at default port `5555`.

**Warning**:  Be careful not to use your livenet credentials accidentally with the fakenet, and vice versa.

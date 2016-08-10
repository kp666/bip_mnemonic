[![Build Status](https://travis-ci.org/sreekanthgs/mnemonic.svg?branch=master)](https://travis-ci.org/sreekanthgs/mnemonic)

# README

BipMnemonic is a ruby gem to generate BIP-39 compliant Mnemonic Words from specific entropy or random entropy of `n` bits and also to generate the BIP-32 seed from the BIP-39 Mnemonic.

## Usage
Specified Entropy in Hex
```
BipMnemonic.to_mnemonic(entropy: "c10ec20dc3cd9f652c7fac2f1230f7a3c828389a14392f05")
```
Entropy of `n` bits
```
BipMnemonic.to_mnemonic(bits: 128)
```
Retrieving entropy from Mnemonic
```
BipMnemonic.to_entropy(mnemonic: 'scissors invite lock maple supreme raw rapid void congress muscle digital elegant little brisk hair mango congress clump')
```
Seed from Mnemonic Words
```
words = Mnemonic.to_mnemonic(entropy: "c10ec20dc3cd9f652c7fac2f1230f7a3c828389a14392f05")
BipMnemonic.to_seed(mnemonic: words)
```

## Credits
* OpenSSL
* Sam Quigley for Ruby implementation of PBKDF2 (https://github.com/emerose/pbkdf2-ruby)

```bash

# https://docs.github.com/pt/authentication/managing-commit-signature-verification
gpg --full-generate-key 
gpg (GnuPG) 2.2.19; Copyright (C) 2019 Free Software Foundation, Inc.
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.

Please select what kind of key you want:
   (1) RSA and RSA (default)
   (2) DSA and Elgamal
   (3) DSA (sign only)
   (4) RSA (sign only)
  (14) Existing key from card
Your selection? 1
RSA keys may be between 1024 and 4096 bits long.
What keysize do you want? (3072) 4096
Requested keysize is 4096 bits
Please specify how long the key should be valid.
         0 = key does not expire
      <n>  = key expires in n days
      <n>w = key expires in n weeks
      <n>m = key expires in n months
      <n>y = key expires in n years
Key is valid for? (0) 1m
Key expires at ter 01 nov 2022 10:36:10 -03
Is this correct? (y/N) y

GnuPG needs to construct a user ID to identify your key.

Real name: Fabiano Francisco dos Passos Stoffel
Email address: fabiano.stoffel@gmail.com
Comment: https://github.com/FabianoFPS
You selected this USER-ID:
    "Fabiano Francisco dos Passos Stoffel (https://github.com/FabianoFPS) <fabiano.stoffel@gmail.com>"

Change (N)ame, (C)omment, (E)mail or (O)kay/(Q)uit? o

git config --global --list

gpg --list-secret-keys
gpg --list-secret-keys --keyid-format=long
/home/fabiano/.gnupg/pubring.kbx
--------------------------------
sec   rsa4096/**************** 2022-10-02 [SC] [expires: 2022-11-01] ...

gpg --armor --export ****************

# pode ser local ou global
git config --local commit.gpgsign true
git config --local --list
git config --global user.signingkey ****************
git config --global --list

cat ~/.gnupg/gpg-agent.conf
nano ~/.gnupg/gpg-agent.conf
default-cache-ttl 86400
gpgconf --reload gpg-agent
```
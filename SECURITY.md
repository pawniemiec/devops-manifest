# Security

## Basic information

No secrets should be stored in plain text

Please do not allow any sensitive data being logged
as logs are visible to multiple people, also not related to eGAR project

All credentials should be sent over secure channel - 
currently via GPG/PGP v2.2.x with 4096 bit key length.

All commits should be signed with GPG v2.2.x with 4096 bit key length.

## GPG/PGP

Please familiarise yourself with these links:

- [Linux Installation](https://nsrc.org/workshops/2014/btnog/raw-attachment/wiki/Track3Agenda/2-1-1.pgp-lab.html#install-gnupg-aka-pgpgpg)
- [MacOS Installation](https://sourceforge.net/p/gpgosx/docu/Home/)
- [Windows Installation](https://help.runbox.com/installing-gpg-on-microsoft-windows/)
- [Create GPG key pair](https://help.github.com/articles/generating-a-new-gpg-key/)
- [GitLab sign commits](https://boats.gitlab.io/blog/post/signing-commits-without-gpg/)
- [GitHub sign commits](https://help.github.com/articles/signing-commits/)

### Generating GPG key

Please run:

```sh
gpg --default-new-key-algo rsa4096 --gen-key
```

Provide the following information:

- Real name: FIRST_NAME LAST_NAME
- E-mail address: FIRST_NAME.LAST_NAME@digital.homeoffice.gov.uk
- Change (N)ame, (E)mail, or (O)kay/(Q)uit? O
- GPG Key pair Password: <your secret password>

## Signing git commits

Once you have GPG key pair created by using your digital email, make sure up have configured your git client correctly:

```sh
git config --global user.name <FIRST_NAME LAST_NAME>
git config --global user.email <FIRST_NAME.LAST_NAME@digital.homeoffice.gov.uk>
git config --global commit.gpgsign true
git config --global gpg.program gpg2
git config --global user.signingkey $(gpg2 --list-keys --keyid-format LONG <FIRST_NAME.LAST_NAME@digital.homeoffice.gov.uk> |head -1 |awk '{print $2}' |tail -c 17)
```

## Encryption

### Encryption in transit

All traffic is performed via encrypted channels

All channels encryption is security approved

### Encryption at rest

All data are encrypted at rest

All channels encryption is security approved

## Secret Management

### Environment variables

### Secret Management System

## Security testing

Please see [TESTING.md](./TESTING.md)

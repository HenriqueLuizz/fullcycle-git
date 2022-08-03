# GIT

## Assinatura de Commit

```sh
gpg --list-secret-key --keyid-form LONG
gpg --full-generate-key
gpg --armor --export <rsa4096_CHAVE>

git config --global user.signingkey <rsa4096_CHAVE>

export GPG_TTY=$(tty)

git config --global commit.gpgsign true
git config --global tag.gpgSign true

vim ~/.gnupg/gpg.conf
 > use-agent
gpgconf --launch gpg-agent


```

## Add e-mail in gpg-key

```sh
gpg --list-secret-key --keyid-form LONG

gpg --edit-key <rsa4096_CHAVE>
    > adduid
    > uid [id_key]
    > trust
        > 5
    > save
```

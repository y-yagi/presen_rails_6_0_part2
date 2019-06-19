#### [Add support for multi environment credentials](https://github.com/rails/rails/pull/33521)

<small>
```
$ EDITOR=vim ./bin/rails credentials:edit -e production
Adding config/credentials/production.key to store the encryption key: xxx

Save this in a password manager your team can access.

If you lose the key, no one, including you, can access anything encrypted with it.

      create  config/credentials/production.key

Ignoring config/credentials/production.key so it won't end up in Git history:

      append  .gitignore

File encrypted and saved.
```

```
./bin/rails credentials:show -e production
# aws:
#   access_key_id: 123
#   secret_access_key: 345

```
</small>

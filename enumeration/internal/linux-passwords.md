# Linux Passwords

## Files

### Files containing 'password'

Lists all files containing the word 'password' on the current machine:

```
grep --color=auto -rnw '/' -ie "PASSWORD=" --color=always 2> /dev/null
or
grep --color=auto -rnw '/' -ie "PASSWORD" --color=always 2> /dev/null
or
grep --color=auto -rnw '/' -ie "PASSWD" --color=always 2> /dev/null
or
grep --color=auto -rnw '/' -ie "PASS" --color=always 2> /dev/null
etc
```

### Files in current directory containing 'password'

Lists files and folders containing the word 'password' in the current directory:

```
find . -type f -exec grep -i -I "PASSWORD" {} /dev/null \;
```

### Files named 'password'

Lists all files named 'password' on the current machine:

```
locate password | more
```

## Authorized keys

Lists all authorized\_keys on the current machine:

```
find / -name authorized keys 2> /dev/null
```

## Id\_rsa

Lists all id\_rsa keys on the current machine:

```
find / -name id_rsa 2> /dev/null
```

## VPN

Lists content of VPN file:

```
cat $vpn.file
```

#### Resources

[PayloadsAllTheThings](https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/Methodology%20and%20Resources/Linux%20-%20Privilege%20Escalation.md#looting-for-passwords)


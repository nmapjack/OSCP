# Linux Users

## Commands

### Whoami

Current user account:

```
whoami
```

### Id

Current user id:

```
id
```

### Sudo

What can be run as sudo under current user:

```
sudo -l
```

### History

Lists history of inputted commands from current user:

```
history
```

## Files

### /etc/passwd

Stores a list of all users on the current system:

```
cut -d: -f1 /etc/passwd
```

### /etc/shadow

Stores all users password hashes on the current system. The first section of the hash, which starts and ends with the `$` sign, defines the encryption (hashing) format. The following is a list of the hashing algorithms and their corresponding ids:

* `$1$` : MD5
* `$2a$` : Blowfish
* `$2y$` : EKSBlowfish
* `$5$` : SHA-256
* `$6$` : SHA-512

```
cat /etc/shadow
```

### /etc/group

Stores a list of all user groups on the current system:&#x20;

```
cat /etc/group
```

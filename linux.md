# linux

## useful commands

### kill process running on TCP port

credits: https://unix.stackexchange.com/a/140483

```bash
kill $(sudo lsof -t -i:{port})
```

or using `fuser`

```bash
fuser -k {port}/tcp
```
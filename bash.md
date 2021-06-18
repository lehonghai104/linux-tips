# Bash

## terminal output to both outfile and stdout

`command 2>&1 | tee outfile`

## Run command in backgound

- Add ampersand symbol `&` after command line

```bash
command &
```

- Prevent stdout when run command in background

```bash
command > /dev/null 2>&1 &
```

## Remove all folder/directory with name inside directory

```bash
# remove all node_modules inside current directory
`find . -name "node_modules" -type d -prune -exec rm -rf '{}' +`
```

## Context (pwd) when run bash file, change dir to same location to bash

```bash
# echo "The first argument is: $1"
echo "Script executed from: ${PWD}"
BASEDIR=$(dirname $0)
echo "Script location is also $0: ${BASEDIR}"
cd ${BASEDIR}
```

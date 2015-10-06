# Poetry from UNIX and Wikipedia

### Source
[Cross-linguistic onomatopoeias](https://en.wikipedia.org/wiki/Cross-linguistic_onomatopoeias), wiki source backed up in `wiki-cross_linguistic_onomatopoeias.txt` (as of 2015-10-05).

### To run
_You may need to `brew install coreutils gnu-sed` for this to work._

`cat wiki-cross_linguistic_onomatopoeias.txt | gsed -En  "s/^\*In \[\[[^]]*\]\][^']*''([a-zA-Z ]+)''$/\1/p" | gshuf -n 10 | echo -e "$(cat -)\n@\n@\n@\n" | gshuf | tr '\n' ' ' | sed "s/@ /\n/g" | echo -e "$(cat -)"`

### Example output

```
fut fut bank bank
brmmm brmmm kykkeliky smask ravr
tuut
klik klik moe awoo
```

```
kre kre
pum nham nham klick
uah
erk klap klap hu hu summ bip
```

```
hiiiihiii gut ravr kopp kopp kwaak kwaak
tik tak cmok
crackle crackle
dripp dropp vau vau
```

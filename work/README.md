```
diff <(cat raspi_set_o | tr -d ' \t') <(cat github_runner_set_o | tr -d ' \t')
3,4c3,4
< emacson
< errexitoff
---
> emacsoff
> errexiton
8,9c8,9
< histexpandon
< historyon
---
> histexpandoff
> historyoff
13c13
< monitoron
---
> monitoroff
```

```
paste raspi_set_o github_runner_set_o | awk '$2 != $4 {print $1"\t"$2"\t"$4}'
emacs   on      off
errexit off     on
histexpand      on      off
history on      off
monitor on      off
```

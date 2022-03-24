```bash
chroot --userspec=1000:1000 "$LFS" /tools/bin/env -i \
     HOME=/pkgbuild     \
     TERM="$TERM"       \
     PS1='[\e[31;40m\](pkgbuild chroot) \[\e[32;40m\]\u:\[\e[36;40m\]\w\[\e[0m\]]\\$ ' \
     PATH=/bin:/usr/bin:/sbin:/usr/sbin:/tools/bin \
     /tools/bin/bash --login +h
```

```bash
chroot "$LFS" /tools/bin/env -i \
    HOME=/root                  \
    TERM="$TERM"                \
    PS1='[\e[31;40m\](root chroot) \[\e[32;40m\]\u:\[\e[36;40m\]\w\[\e[0m\]]\\$ ' \
    PATH=/bin:/usr/bin:/sbin:/usr/sbin:/tools/bin \
    /tools/bin/bash --login +h
```

```bash
alias ls='ls --color=auto'
alias ll='ls -F -b -T 0 --group-directories-first --color=auto --format=long --time-style="+%F %T" --human-readable'
```
```
pacman -Syu' followed by 'pacman -S package -dd --overwrite "*"
```
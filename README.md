`sendkeys` is a helper for `qemu`

```console
$ qemu-kvm -monitor tcp:127.0.0.1:1234,server,nowait ... &
$ sendkeys "Hello" | nc -v 127.0.0.1 1234
```

Example of modifying the boot of a SUSE Linux installation:
```console
$ sendkeys "<esc><ret><delay>linux dud=http://foo:8080/a.rpm<ret>"
sendkey esc
sendkey ret
sendkey l
sendkey i
sendkey n
sendkey u
sendkey x
sendkey spc
sendkey d
sendkey u
sendkey d
sendkey equal
sendkey h
sendkey t
sendkey t
sendkey p
sendkey shift-semicolon
sendkey slash
sendkey slash
sendkey f
sendkey o
sendkey o
sendkey shift-semicolon
sendkey 8
sendkey 0
sendkey 8
sendkey 0
sendkey slash
sendkey a
sendkey dot
sendkey r
sendkey p
sendkey m
sendkey ret
$
```

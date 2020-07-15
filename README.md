When building the package in 64-bit cygwin, I got the error:

```
address space needed by 'dllunix.so' (0x400000) is already occupied 
```

I "solved" it by installing rebase 4.4.2-1, and then

```
rebase -b 0x7cd20000 /usr/lib/ocaml/stublibs/dllunix.so
rebase -b 0x7cdc0000 /usr/lib/ocaml/stublibs/dllthreads.so
```

Re. https://github.com/ocaml/opam/issues/3785

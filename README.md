# Erlang Port examples
examples from https://erlang.org/doc/tutorial/c_port.html

### custom encoding
```shell
$ gcc -o extprg complex.c erl_comm.c port.c
```

### erl_interface
```shell
$ gcc -o extprg -I(asdf where erlang)/lib/erl_interface-3.12/include -L(asdf where erlang)/lib/erl_interface-3.12/lib complex.c erl_comm.c ei.c -lei -lpthread
```
# Erlang Port examples
Examples from https://erlang.org/doc/tutorial/c_port.html

### 1_port
```shell
$ gcc -o extprg complex.c erl_comm.c port.c
```

### 2_port_erl_interface
```shell
$ gcc -I(asdf where erlang)/lib/erl_interface-3.12/include \
  -L(asdf where erlang)/lib/erl_interface-3.12/lib \
  -lei -lpthread \
  -o extprg complex.c erl_comm.c ei.c 
```

### 3_port_driver

```shell
$ gcc -I(asdf where erlang)/usr/include \
  -L(asdf where erlang)/usr/lib -lerl_interface \
  -fpic -shared -flat_namespace -undefined suppress \
  -o example_drv.so complex.c port_driver.c 
```

### 4_nif
```shell
$ gcc -I(asdf where erlang)/usr/include \
  -L(asdf where erlang)/usr/lib -lerl_interface \
  -fpic -shared -flat_namespace -undefined suppress \
  -o complex6_nif.so -fpic -shared complex.c complex6_nif.c
```
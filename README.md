# Erlang Port examples
examples from https://erlang.org/doc/tutorial/c_port.html

### 1_port
```shell
$ gcc -o extprg complex.c erl_comm.c port.c
```

### 2_port_erl_interface
```shell
$ gcc -o extprg -I(asdf where erlang)/lib/erl_interface-3.12/include -L(asdf where erlang)/lib/erl_interface-3.12/lib complex.c erl_comm.c ei.c -lei -lpthread
```

### 3_port_driver

```shell
gcc -o extprg -flat_namespace -undefined suppress -I(asdf where erlang)/usr/include -L(asdf where erlang)/usr/lib -lerl_interface -o example_drv.so -fpic -shared complex.c port_driver.c 
```
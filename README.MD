# Collection of Ancestral Ancestral 



### kill multithread progress

```shell
ps -ef | grep "Server" | grep -v "grep" | cut -c 9-16 |xargs kill -9
```


### build llvm with low memeory

```shell
LD=gold CC=clang CXX=clang++ cmake -G Ninja -DCMAKE_EXPORT_COMPILE_COMMANDS=ON .. -DLLVM_ENABLE_PROJECTS=compiler-rt-5.0.0.src -DLLVM_TARGETS_TO_BUILD="X86" -DLLVM_ENABLE_RTTI=ON -DLLVM_REQUIRES_RTTI=1 -DLLVM_PARALLEL_LINK_JOBS=1 -DCLANG_ENABLE_STATIC_ANALYZER=ON -DCMAKE_BUILD_TYPE=Release -DLLVM_USE_LINKER=gold
ninja
sudo ninja install
```





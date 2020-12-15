# Example C project with esy

`hello.c` is the simple C program. You can compile it with `esy`. To run the executable, run `esy x hello`.

## Explanation

When `esy` is run, the build command specified in the `package.json`, `gcc -o hello hello.c` is run. However, the resulting binary, `hello`, is created in the build directory - it needs to be installed (similar to how one would run `make install` when install a C package). We 'install' it with the Unix `install` command and copy it to esy's install sandbox (like you system's `/usr/local`, except only local to the project). Once installed, the binary can be accessed with `esy x ...`.

# luacpp
Lua CPP wrapper


## Installing

```
mkdir build
cd build
cmake -DCMAKE_BUILD_TYPE=Debug ../Source
make -j 4
```

## Building documents

```
sudo apt-get install texlive-latex-base texlive-latex-recommended texlive-latex-extra graphviz

mkdir build
cd build
cmake -DCMAKE_BUILD_TYPE=Debug ../Source
make doc_doxygen

cd build/doc_doxygen/latex
make pdf
```

## Testing the memory management

```
mkdir build
cd build
cmake -DCMAKE_BUILD_TYPE=Debug ../Source
make -j 4

valgrind -v --run-cxx-freeres=yes --run-libc-freeres=yes ./hello
```
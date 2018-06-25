## Installation Requirements

- 64-bit machine.
- [Conan](https://www.conan.io/) package manager, version 1.4.0 or newer. See [Conan Installation](http://docs.conan.io/en/latest/installation.html#install-with-pip-recommended).

## Installation Procedure

The *Bitprim* executables can be installed on Linux, macOS, FreeBSD, Windows and others. These binaries are pre-built for the most usual operating system/compiler combinations and hosted in an online repository. If there are no pre-built binaries for your platform, a build from source will be attempted.

So, for any platform, an installation can be performed in 2 simple steps:

1. Configure the Conan remote
```
conan remote add bitprim https://api.bintray.com/conan/bitprim/bitprim
```

2. Install the appropriate executable

```
# For Bitcoin Cash
conan install bitprim-node-exe/0.10.2@bitprim/stable -o currency=BCH 
# ... or (BCH is the default crypto)
conan install bitprim-node-exe/0.10.2@bitprim/stable 

# For Bitcoin Legacy
conan install bitprim-node-exe/0.10.2@bitprim/stable -o currency=BTC

# For Litecoin
conan install bitprim-node-exe/0.10.2@bitprim/stable -o currency=LTC
```

## Building from source Requirements

In case there are no pre-built binaries for your platform, it is necessary to build from source code. In such a scenario, the following requirements must be added to the previous ones:

- C++11 Conforming Compiler.
- [CMake](https://cmake.org/) building tool, version 3.4 or newer.


## Running the node

In order to run the full node, you have to initialize the database and then run the node:

1. Run the following to initialize the database:

```./bn -i```

2. Finally, run the node:

```./bn```

The above commands use the default configuration hardcoded in the executable. You can use a configuration file to customize the behavior of the node. In the [bitprim-config](https://github.com/bitprim/bitprim-config) repository you can find some example files.

1. Initialize the database using a configuration file:

```./bn -i -c <configuration file path>```

2. Run the node using a configuration file:

```./bn -c <configuration file path>```

## Advanced Installation

Bitprim is a high performance node, so we have some options and pre-built packages tuned for several platforms.
Specifically, you can choose your computer _microarchitecture_ to download a pre-build executable compiled to take advantage of the instructions available in your processor. For example:

```
# For Haswell microarchitecture and Bitcoin Cash currency
conan install bitprim-node-exe/0.10.2@bitprim/stable -o currency=BCH -o microarchitecture=haswell 
```
So, you can manually choose the appropriate microarchitecture, some examples are: _x86_64_, _haswell_, _ivybridge_, _sandybridge_, _bulldozer_, ...  
By default, if you do not specify any, the building system will select a base microarchitecture corresponding to your _Instruction Set Architecture_ (ISA). For example, for _Intel 80x86_, the x86_64 microarchitecture will be selected.

### Automatic Microarchitecture selection

Our build system has the ability to automatically detect the microarchitecture of your processor. To do this, first, you have to install our _pip_ package called [cpuid](https://pypi.python.org/pypi/cpuid). Our build system detects if this package is installed and in such case, makes use of it to detect the best possible executable for your processor.

```
pip install cpuid
conan install bitprim-node-exe/0.10.2@bitprim/stable 
```

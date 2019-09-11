# Taller4-SE
## Usage
After the installation of this project you have to make sure you have installed the following libraries:
- Autotools
- Autoconf
- Libtools
- Automake

If you don't have installed these libraries you can follow the next commands:
```bash
    sudo apt update
    sudo apt install autotools-dev
    sudo apt install autoconf
    sudo apt install automake
    sudo apt install libtool
```

## Installation
For the installation of this library you have to run the command below:
```bash
    autoreconf --install
```

This command will generate the necessary to create the dynamic and static library. (Developer mode)

## Test
To check the library (User mode) you can use the commands below, this will permit you to test the executable:

1. Create a directory for testing, otherwise it will be installed in /usr/
```bash
    mkdir build
    mkdir build/usr
```

2. Execute the configure file, change the <USER> for your own username
```bash
    ./configure --prefix=/home/<USER>/Taller4-SE/build/usr
```

3. Run make
```bash
    make
```

4. Install your library in build/usr/
```bash
    make install
    cd build/usr/
    ls
```
5. And if you want to create a package with your library to generate a .tar.gz you can run the command below in the root directory of the project
```bash
    make distcheck
```
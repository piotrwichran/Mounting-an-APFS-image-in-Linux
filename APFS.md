
```
sudo apt install fuse libfuse3-dev bzip2 libbz2-dev cmake gcc git libattr1-dev zlib1g-dev
```

```
git clone https://github.com/sgan81/apfs-fuse.git
cd apfs-fuse
git submodule init
git submodule update
```

```
mkdir build
cd build
cmake ..
ccmake . # Only if you want to change build options
make
make install
```

```
apfs-fuse <device> <mount-directory>
```

# GNU_LibTool
**GNU Libtool: a generic library support script**

This is an unofficial verbatim redistribution of the binary&source form of the GNU Libtool under its open source license (GPL 2.0) terms (see the LICENSE file).

This redistribution is under the same license as the original.

Please visit the official website for more details: http://www.gnu.org/software/libtool

## Download
You can download the compiled binary files at the [release page](https://github.com/yuhangwang/GNU_LibTool/releases).

## Compilation notes
**!!! make sure you use GNU Autoconf 2.69, because the *configure* file in the source folder was
generated using that version. I tried using Autoconf 2.63 (2008), one the tests (after issuing *make check*)
didn't pass**

### Compilation environment
* CentOS 6.6
* x86_64 architecture
* Compiler: gcc version 4.4.7 20120313 (Red Hat 4.4.7-11)

### Compilation steps
#### Version: 2.4.6 (2015)
```bash
wget http://mirror.clarkson.edu/gnu/libtool/libtool-2.4.6.tar.gz
tar xvf libtool-2.4.6
mkdir build_libtool-2.4.6
cd build_libtool-2.4.6
../libtool-2.4.6/configure --prefix=/home/steven/install/libtool/2.4.6 --enable-shared --enable-static M4=/home/steven/install/m4/1.4.17/bin/m4
make -j16
make check -j16 | tee QualityVerification.txt
make install
```

### Quality verification
- **156 tests behaved as expected**
- **14 tests were skipped**
- **Zero failing tests**

See the "QualityVerification.txt" for the output of "make check".

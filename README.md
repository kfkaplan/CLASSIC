### THIS FORK:

This fork of CLASSIC has been slightly modified to work with CLASS data files from the GREAT instrument on SOFIA and compile on a modern Mac OS with the latest version of python.  The goal is to allow GREAT data to be read into python without the need to install Gildas.  In theory, it should work on any OS and most CLASS data files.  This has not been extensively tested so please raise an issue to report any bugs.

This version can be installed via the original instructions below, or using pip:
```
pip install -U git+https://github.com/kfkaplan/CLASSIC.git@master
```


# A Python interface to the CLASSIC data container


The CLASSIC data container is a a digital format for single-dish or
interferometric radio-astronomy data used by the GILDAS software. The
format is described in [IRAM Memo 2013-2](https://www.researchgate.net/publication/262378314_IRAM_memo_2013-2_CLASSIC_Data_Container), which is also distributed with this software.

The software consists of two parts:

 * a C++ interface to the CLASSIC data container format. A small test
   program using it may be built by running `make classictest` and run
   via `./classictest <filename>`, where `filename` is a data file in
   CLASS(IC) format.
 * a python interface which can be built by `make install` and tested
   via `python3 test.py <filename>`, where `filename` again is a data
   file in CLASS(IC) format.

## Example:

``` shell
make classictest
./classictest O-097.F-9401A-2016-2016-06-08.apex
make install
python3 test.py O-097.F-9401A-2016-2016-06-08.apex
```

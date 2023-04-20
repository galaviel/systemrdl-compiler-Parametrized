[![Documentation Status](https://readthedocs.org/projects/systemrdl-compiler/badge/?version=latest)](http://systemrdl-compiler.readthedocs.io)
[![build](https://github.com/SystemRDL/systemrdl-compiler/workflows/build/badge.svg)](https://github.com/SystemRDL/systemrdl-compiler/actions?query=workflow%3Abuild+branch%3Amain)
[![Coverage Status](https://coveralls.io/repos/github/SystemRDL/systemrdl-compiler/badge.svg?branch=main)](https://coveralls.io/github/SystemRDL/systemrdl-compiler?branch=main)
[![PyPI - Python Version](https://img.shields.io/pypi/pyversions/systemrdl-compiler.svg)](https://pypi.org/project/systemrdl-compiler)

This is a fork of the original project, with the intent of adding experimental (very limited) parametrization support for regblock output.
All parameters specified by the user (in the regblock sub-commnad) as --keep_params PARA1 PARAM2 ... will retain their symbolic, unresolved value (e.g. 'PARAM1`) instead of being resolved to actual (most commonly - integer) values.
Support is provided for:
1. Parametrization of the dimensions of 1D array of registers (MDA - multi-dim - wip). The array dimension size must be an expression containing only the name of the parameter (without any further arithmetic or other operands). 
1. Parametrization of the reset value of individual fields. Again - expression must be as 1. above.

# SystemRDL Compiler

The `systemrdl-compiler` project implements a generic compiler front-end for
Accellera's [SystemRDL 2.0](http://accellera.org/downloads/standards/systemrdl)
register description language. The goal of this project is to provide a free and
open compiler that lowers the barrier to entry to using an industry standard
register description language.

By providing an elaborated register model that is easy to traverse and query,
it should be far easier to write custom register space view generators.

![overview](docs/img/overview.svg)

## Documentation
See the [SystemRDL Compiler Documentation](http://systemrdl-compiler.readthedocs.io) for more details

## Related Projects

If you are looking for a complete SystemRDL command line tool, see the [PeakRDL project](https://peakrdl.readthedocs.io).

## License

The SystemRDL Compiler is published and distributed under the [MIT License](LICENSE).

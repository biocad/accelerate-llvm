# Change Log

Notable changes to the project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/) and the
project adheres to the [Haskell Package Versioning
Policy (PVP)](https://pvp.haskell.org)

## [next]
### Changed
 * `run` variants which do not take an explicit execution context now execute on
   the first available device in an exclusive fashion. Multi-GPU systems can
   specify the default set of GPUs to use with environment variable
   `ACCELERATE_LLVM_PTX_DEVICES` as a list of device ordinals.

## [1.1.0.1] - 2018-01-08
### Fixed
 * add support for building with CUDA-9.x

## [1.1.0.0] - 2017-09-21
### Added
 * support for GHC-8.2
 * caching of compilation results ([accelerate-llvm#17])
 * support for ahead-of-time compilation (`runQ` and `runQAsync`)

### Changed
 * generalise `run1*` to polyvariadic `runN*`

### Fixed
 * Fixed synchronisation bug in multidimensional reduction
 

## [1.0.0.1] - 2017-05-25
### Fixed
  * [#386] (partial fix)

## [1.0.0.0] - 2017-03-31
  * initial release


[next]:                 https://github.com/AccelerateHS/accelerate-llvm/compare/1.1.0.1-ptx...HEAD
[1.1.0.1]:              https://github.com/AccelerateHS/accelerate-llvm/compare/1.1.0.0...1.1.0.1-ptx
[1.1.0.0]:              https://github.com/AccelerateHS/accelerate-llvm/compare/1.0.0.0...1.1.0.0
[1.0.0.1]:              https://github.com/AccelerateHS/accelerate-llvm/compare/1.0.0.0...1.0.0.1
[1.0.0.0]:              https://github.com/AccelerateHS/accelerate-llvm/compare/be7f91295f77434b2103c70aa1cabb6a4f2b09a8...1.0.0.0

[#386]:                 https://github.com/AccelerateHS/accelerate/issues/386

[accelerate-llvm#17]:   https://github.com/AccelerateHS/accelerate-llvm/issues/17


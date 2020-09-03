# gm\_redis

[![Build Status](https://metamann.visualstudio.com/GitHub%20danielga/_apis/build/status/danielga.gm_redis?branchName=master)](https://metamann.visualstudio.com/GitHub%20danielga/_build/latest?definitionId=13&branchName=master)

A Garry's Mod module that adds [Redis][1] [client][2] capabilities.

## Compiling

The only supported compilation platform for this project on Windows is **Visual Studio 2017**. However, it's possible it'll work with *Visual Studio 2015* and *Visual Studio 2019* because of the unified runtime.

On Linux, everything should work fine as is.

For macOS, any **Xcode (using the GCC compiler)** version *MIGHT* work as long as the **Mac OSX 10.7 SDK** is used.

These restrictions are not random; they exist because of ABI compatibility reasons.

If stuff starts erroring or fails to work, be sure to check the correct line endings (\n and such) are present in the files for each OS.

## Requirements

This project requires [garrysmod\_common][3], a framework to facilitate the creation of compilations files (Visual Studio, make, XCode, etc). Simply set the environment variable '**GARRYSMOD\_COMMON**' or the premake option '**gmcommon**' to the path of your local copy of [garrysmod\_common][3].

We also use [SourceSDK2013][4]. The links to [SourceSDK2013][4] point to my own fork of VALVe's repo and for good reason: Garry's Mod has lots of backwards incompatible changes to interfaces and it's much smaller, being perfect for automated build systems like Azure Pipelines (which is used for this project).

  [1]: https://redis.io
  [2]: https://github.com/cpp-redis/cpp_redis
  [3]: https://github.com/danielga/garrysmod_common
  [4]: https://github.com/danielga/sourcesdk-minimal

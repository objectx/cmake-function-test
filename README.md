# cmake-function-test - Test CMake's function scope behavior.

# Usage

```sh
cmake -S . -B 00.BUILD -G Ninja
```

```
- The CXX compiler identification is AppleClang 12.0.0.12000032
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Check for working C compiler: /Library/Developer/CommandLineTools/usr/bin/cc - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Check for working CXX compiler: /Library/Developer/CommandLineTools/usr/bin/c++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- /Users/objectx/Workspace/GitHub/cmake-function-test/dir2: Call 1
-- /Users/objectx/Workspace/GitHub/cmake-function-test/dir2: Call 2
-- Configuring done
-- Generating done
-- Build files have been written to: /Users/objectx/Workspace/GitHub/cmake-function-test/00.BUILD
```

`child_fn` in `dir1` never called! (because CMake's function lives in the single scope)

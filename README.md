# Kron
A fast and scalable high level language that provides frontend and backend capabilities simultaneously with an emphasis on code readability. It's supposed to combine the best of most programming languages:

- high performance / speed
- high memory efficiency
- high degree of user control (e.g. control of memory usage)
- simple and exact syntax (as far as allowed by above)
- extendible core functionality

Kron uses the .kr file extension for everything.

Every aspect of Kron's functionality is based on libraries called ***Gears***. Gears can define any functionality such as datatypes, operators and functions. The only functionality native to Kron (i.e. doesn't have to be specifically imported) are the import / export capabilities, syntax structuring and language definition syntax. This language definition syntax is used to define new functionality for Kron within Gears.

___

*HelloWorld.kr*
``` kron
  from core import io, string;
  print "Hello World!";
```

___

TODO:
- Implement OOP (https://mukulrathi.co.uk/create-your-own-programming-language/llvm-ir-cpp-api-tutorial/)
- Github pygments contribution for syntax highlighting on github (https://github.com/pygments/pygments)
- Github linguist contribution for language colour in statistics (https://github.com/github/linguist/blob/master/lib/linguist/languages.yml)
- VSCode plugin with syntax highlighting, linting etc. (https://code.visualstudio.com/api/language-extensions/overview)
- Implement libuv for Node-like backend capabilities (https://github.com/libuv)
- Once HTTP/2 server implemented, add to listing at https://github.com/httpwg/http2-spec/wiki/Implementations

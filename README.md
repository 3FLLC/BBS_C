
██████  ██████  ███████        ██████ 
██   ██ ██   ██ ██            ██      
██████  ██████  ███████ █████ ██      
██   ██ ██   ██      ██       ██      
██████  ██████  ███████        ██████ 
                                      
=====================================

Full C like scripting engine written in Pascal. Originally designed for `satania-buddy`, it has been extended to be the perfect embedded scripting engine in my socket suite, used to make a Moderm 2023 BBS (Bulletin Board System). The code can also be utilized as a general-purpose, embeddable scripting engine for other projects. See the original source.

BBS-C has been tested and works on the following platforms inside DXSock 6: Windows (x86 & x64), Linux (x64), MacOSX (MoJave and older) - although theoretically, it should work on every platform except old (8/16-bit systems) and wasm, due to the lack of `goto`

`import` feature (allows to import of external functions from DLLs directly) only works on x64 platforms at the moment.

#### Original Features:
- https://github.com/Kagamma/satania-buddy/wiki/Scripting-Reference

#### Original Building:
- `fpc -O4 evil.pas`

#### Running Standalone:
- `evil examples/hello.evil`

#### How to embedded into applications
- See `Test.pas` and `evil.pas` source code

#### About compiler
- The compiler itself is a one-pass compiler. It follows Niklaus Wirth’s Pascal-S design, completely skips AST generation, and generates p-code directly.
- Due to the lack of AST, only constant folding and peephole optimizations are implemented.
- The performance of its virtual machine is better than CPython.

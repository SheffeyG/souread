# port 源码分析
- porth: https://gitlab.com/tsoding/porth.git

## ef407fc Ready. Set. Go!
`iota` 枚举? but why
## be77754 Unhardcode program
## 688cab6 Update README
## a376697 Warning about work in progress
## 8943f22 Add help subcommand
## 782555b program_name -> compiler_name
## c4695bb Compute output path based on the input path
## 8e45acb Add rough plan to the README
## d359872 Get rid of the uncons
## 9bb6345 Shell escaped the output of the echoed cmds
## 435b48f Fix usage() call
## 0cc4aba Tweak logging style
## 936fdcc Report locations of the errors
## eaee263 Introduce `equal` operation
## 9471e4b Implement else-less if
## 369de0e Implement `else` for `if`-construction
## 992a0a7 Introduce dup operation
## 754bc2b Introduce > operation
## a6ddbe8 Introduce while loops
## cb62b42 Add address to the end of the program
## bf0c087 Add more tests
## 73479bf Clean up README a bit
## b7536f9 Typo
## 0478d81  More details on the compilation dependencies
## 62ac194 More details for Quick Start instructions
## 562c718 Document Stack Manipulations
## 1b2a3de Document comparison operations
## b887b16 Document arithmetic operations
## b29fb3b Document Control Flow constructions
## 528df5b Implement -r flag for the com subcommand
## cd028c8 Implement -o flag for com subcommand
## aba49a9 Make porth.py resistant to loading from shells
## 5cc2fc5 Remove redundant op ctors
## 8722c27 Add support for C-style comments
## 867579c TODOs
## fa50287 Turn ops into dicts
## a58b8c3 Associate location with the ops
## 0734dac Report block mismatch errors as compiler errors not asserts
## 8d042e7 Implement test.py script
## 7a9ab73 Remove unused imports
## 2853cfd Rename cmd_echoed -> cmd_call_echoed
## d2a74c7 Introduce mem operation
## 0316efa Stub mem implementation for the simulation
## 58c4c41 Temporarily remove 4th test case
## 0ea9f12 Fix error reporting on unknown token
## 77f57a6 Rename `.` to `dump`
## c2499b5 Add support for loading and storing bytes from/into the memory
## 5e4ee77 Implement memory access operations in simulation mode
## 73b1e1f Implement syscalls support
## 78c5aa3 Fix `dump` documentation
## 13f6d55 Fix `dump` operation usage in the README examples
## 20b5c08 Implement the full set of syscall operations
## a5577be Clean up some tests
## 9351597 Proxy the exit code of `com -r` subcommand
## fd00653 Fix syscall docs
## 9f31e59 Reorganize examples and tests
## 84dab3c Implement 2dup and < words
## 775cc44 Update example
## 26eff89 Fix typos
## 602c51a Implement `swap` operation
## 64feb44 Implement `drop` operation
## 57c2a8c Actually assert expected output of the tests
## 3b01221 Document project testing
## 3c9abae Fix Language Reference formatting
## 3f52522 Cleanup OP_GT and OP_LT implementations of the simulation
## 9389387 Introduce debug mode
## 26664ac Setup CI
## 2ce64fb Provide more generic version of python 3?
## 142855e Merge pull request #1 from tsoding/ci
## 70b0331 TODO about syscall results
## 2750319 Implement 4 new operations
## d650cbd Implement rule 110 in porth
## 2343a42 Merge pull request #3 from tsoding/rule110
## d009797 Implement mod operation
## 4677bee Get rid of the prefix numbers in tests
## ee0f8f6 Merge pull request #4 from tsoding/rename-tests
## a608bce Implement remaining comparison operators
## 712874b Merge pull request #5 from tsoding/remaining-comparison
## 98c876a Speedup rule 110 implementation
## 579c192 Merge pull request #6 from tsoding/rule110-speedup
## 0b4afff More work
## 7538a31 Implement `not equals` operation
## 921354d Merge pull request #8 from tsoding/not-equals
## 6fdd862 Minor logging style changes
## 7062c6b (#7) Allow pushing big 64 bit numbers on x86_64
## 5838fb1 Merge pull request #9 from tsoding/7-push-big-numbers-x86-64
## a8b5844 Add dash break line to arithmetics test
## b88b0a5 Add dash break line to bitwise test
## 390f470 Add dash break line to control-flow test
## 3a66eac Add opascal emacs mode to memory test
## 912e105 Clarify the plan
## 5c62eea Use examples as the test cases
## 0836b1f Merge pull request #10 from tsoding/cleanup-tests
## b5116c6 Pass command line arguments to the program in `com -r`
## 6ab75aa Discard the idea of using ctypes for now
## b7fbb6c TODO about command line arguments
## 878716a Push the syscall result onto the stack
## ce0be10 Implement syscall0
## b543553 Merge pull request #11 from tsoding/syscalls
## b5efe6f Discard the idea of using forth style of load/fetch for now
## 43ff97d Rename `dump` to `print`
## 14ae208 Merge pull request #12 from tsoding/dump-to-print
## ece62b3 Introduce the notion of tokens
## b119280 Implement string literals
## e3c9c0e Update Hello, World in examples
## 90fcd6b Add Hello, World example to README
## a3dae22 Merge pull request #13 from tsoding/string-literals
## d9bb466 Fix docs
## 34c33aa Explicit separation line in all of the test cases
## d2e2b60 Merge pull request #14 from tsoding/tests
## 9687e7e Add string literals to Language Reference
## 34a6534 Get rid of op['addr'] field
## 5e9c026 Merge pull request #15 from tsoding/get-rid-of-addr
## e4d77cd Rename key procedures
## 4465e55 Annotate procedures with expected types
## f6838dd Simplify return type of lex_line
## 55e7ad9 Introduce OpType and TokenType
## f3f06c3 Use enum.Enum to define TokenType
## 343ba4a Turn token into a dataclass
## b504a34 Use enum.Enum for OpType definition
## b50196c Turn Op into a dataclass
## a5c6d71 Merge pull request #16 from tsoding/refactor
## 5da80c1 Cleanup
## 8e5dd8f Fix escaping with `unicode_escape` encoding
## a9d85c9 Merge pull request #23 from tsoding/fix-escaping
## 672ee02 Fix mypy remarks
## 29d91bb Run mypy on CI
## cea0dc6 Merge pull request #24 from tsoding/mypy
## 6aa16cc Report unclosed string literal as a compiler error
## e3a7742 Merge pull request #25 from tsoding/unclosed-string-literal
## 4840d5a Discard the idea of including docs into script for now
## 1b79404 Discard the idea of ignoring the tests if .txt file is missing
## 651fdf6 TODO about // inside of string literals
## 9e2da78 Add basic support for macros
## e3e5e61 Document the macro system
## d6c03e4 Use macro system in rule110 example
## a04bcb3 Add rough support for file includes
## 72e2a59 Implement multiply operation
## 297b4b6 Additional work
## 0ab0392 Fix mypy remarks
## 315af19 Implement character literals
## 6807c50 Fix mypy remarks again
## 026a4bb Merge pull request #26 from tsoding/macros
## 13abdac Implement simple include path mechanism
## 5b54ae7 Use std library in all of the tests
## f320361 Document the standalone usage
## 248c07c Merge pull request #27 from tsoding/include-paths
## e492945 Add simple emacs support for Porth
## b8b129c Merge pull request #28 from tsoding/emacs-support
## a33790e Introduce Linux specific module to standard library
## c70af71 Merge pull request #29 from tsoding/linux-specific-module
## 936aee3 Tweak README
## 413483e Improve documentation for Integer and String data types
## 0fde039 Allow only one byte inside of character literals
## 8317334 Merge pull request #31 from tsoding/char-one-byte
## 5fd9715 Document character data type
## dab0095 Unhardcode 2dup operation
## b1cf82e Merge pull request #32 from tsoding/unhardcode-2dup
## c492d5d Fix example in README
## 5a3bcdb Remove 2dup from the list of builtin words
## e0a0a87 Clarify syscalls in std.porth
## 66dd818 Implement division operation
## af6b504 Merge pull request #33 from tsoding/division
## 6419a2a Add 2drop to std.porth
## 637c315 Introduce divmod operation
## 4ae452f Merge pull request #34 from tsoding/divmod
## 8e8c5b9 Factor out Keywords out of Ops
## b041059 Factor out Intrinsic out of Op
## 5710b8b Merge pull request #35 from tsoding/refactor
## 3e4dd04 Add support for vim
## acf7bba Better error message on intrinsic redefinition
## c95805e Handle keyword in human()
## 1d4ab5a Cleanup Rule 110
## 7693a39 Merge pull request #37 from tsoding/cleanup-rule110
## 9c0c802 Rename Op.value -> Op.operand
## 885c2d8 Merge together Op.value and Op.jmp
## c520c00 Merge pull request #38 from tsoding/remove-jmp
## 75d8d17 Implement -s flag for the compilation mode
## c5b5fc8 Merge pull request #39 from tsoding/silent-com
## a34df47 add support to `//` inside string literals
## 5f0afc7 avoid some checks for `text_of_token.startswith("//")`
## d845d5b add support to double quotes inside string literal
## 1488de4 Wrappers for common syscalls
## c53e18e Merge pull request #40 from drocha87/comment
## 99aeedb Update README
## 181a576 Merge branch 'master' into syscall-wrappers
## 0ba18cf Fix the tests
## d7b9fa4 Merge pull request #42 from tsoding/syscall-wrappers
## a42fde8 Merge remote-tracking branch 'origin/master' into string_literal
## d7ecaa2 Merge pull request #41 from drocha87/string_literal
## 97c0bc4 add support to multi line string
## 2b94e13 do not initialize `col_end` with `None`
## 35cb631 Add support for nested blocks in macro definitions
## a3bbabc Merge pull request #43 from drocha87/multline_string
## ce50b9b Add tests for blocks inside of macros
## c15888a Merge pull request #45 from ap29600/master2
## 6d4ab5b Allow recording test cases in compilation mode
## 859a65b Add euler test cases
## 8618ad8 Add README for euler problems
## b7a274c Additional work
## f6d3a46 set basedir to current working directory if it is empty
## 5b69c5d Disclaimer about Project Euler solutions
## 5458aee Merge pull request #48 from tsoding/euler
## 48db695 Typo
## 83835b5 Merge pull request #49 from drocha87/47
## 5d620d2 Add more details on "test compiler errors" TODO
## 6502239 Formatting
## 35b882b Fix compiler errors output
## 7098d1a Implement custom binary format for testing output
## cad2a61 Update files with expected output to binary format
## 5766d05 Add tests for errors
## 8dd1d45 Update tests output files for examples
## d6554d4 Update format for euler tests output
## 670d084 Document binary format in README
## 402cfd6 Temp implement intrinsic load and store 64 bit values
## ab30f00 Fix: missed `len(Intrinsic)` in simulate function
## 2043de3 fix: removed load64 store64 macros, updated inc64
## 2a36320 fix: typo!!
## 6c2c0a3 fix: replace macros with intrinsics
## 4df5602 readme: instrinsic load and store 64 documentation
## 0c3ab92 simple tests for `,64` and `.64`
## b1447f6 fix: no need for mask with store64 intrinsic
## 2cd52f5 Try out a new simple text format
## 6bcadfe Remove experimental garbage
## 6d8701e Update the test case format documentation
## 29a2960 Type check test.py on CI as well
## edd25e7 Merge pull request #52 from kolumb/binary-tests
## 9572cd8 fix: simulation of 64 bit values
## 2cf419b Merge branch 'master' of github.com:tsoding/porth into ld64
## 9073798 Use pypy on CI
## b0c0489 refactor
## da2fd60 Bump the version of pypy hoping it will change something
## d22b519 Revert "Bump the version of pypy hoping it will change something"
## 28b14ff Some internet page said this my help but I doubt it
## 0997cf3 Get rid of actions/setup-python
## 2cc7ea3 Try to use Python 3 explicitly
## 5796634 Another refactor for types
## b2883a8 Upgrade ubuntu to 20.04
## 5b33700 Try to install pypy3 from ubuntu repos
## e8254c6 Merge pull request #54 from zrthxn/ld64
## dbc1d5e Run porth.py with the same Python as test.py
## fc4fb26 Run tests with pypy3
## bd96bc2 Print the versions of pythons
## 9f3cd15 Install pypy from the official website
## 5392f47 Run euler solutions on CI with pypy
## b5dee5a Try to cache pypy
## d99b324 Update Project Euler README
## bc7b411 Mention PyPy in documentation for Simulation Mode
## e4edcd1 Merge pull request #55 from tsoding/pypy
## c901d91 Add performance warning to ./euler/problem04.porth
## 5352293 Add Porth Contributors to LICENSE
## b2b5f4a TODO about profiler mode
## 1ed64ea Implement macro expansion limit mechanism
## 119ca80 Make the expansion limit customizable
## c4760be Merge pull request #57 from tsoding/macro-expansion-limit
## 7cbc046 Implement command line args for the simulation mode
## 502ea23 Merge pull request #60 from tsoding/argv
## 96ea7b9 Implement exit syscall for simulate_little_endian_linux()
## cd52faf Remove finished TODOs
## 94116fa Merge pull request #61 from tsoding/exit-syscall
## f50b51f Typing for load/store has been demonstrate to be unnecessary
## f3f3793 Macros from command line is unnecessary right now
## 3773d82 Implement read syscall in simulation mode
## cfd9c23 Merge pull request #66 from tsoding/simulate-read-syscall
## c2ee8de Add support for input in the test case format
## 0462fae There is no way to record the test case input
## 31b4f9d The test case input is not provided during the test
## 3722a2e Merge pull request #67 from tsoding/test-case-input
## 74c9d69 Implement argv recording
## d99332a Fix the build
## f9b9a1e Merge pull request #68 from tsoding/record-input
## 1efdd47 Implement recording of stdin
## ae83e68 Add name example
## 058c98b Restructure the test.py subcommand system
## 650158b Update Testing documentation
## 5fa4c97 Update CI scripts
## e709e55 Merge pull request #71 from tsoding/record-stdin
## 9cdb461 simplify strlen
## 0ce961d Merge pull request #70 from scgilardi/simplify-strlen
## 6e33e8e Fix error messages in test.py
## f025995 Introduce argc and argv intrinsics
## 93d32f0 Implement argc and argv intrinsics
## 167d823 Introduce type checking phase
## 4f0e5df Fix mypy remarks
## 3a3f48f Fix mem intrinsic bug
## bb4df2a Merge pull request #77 from tsoding/static-type
## b4d0188 Add Reverse Linked List example
## 6798868 Merge pull request #79 from tsoding/reverse-linked-list
## 093b1bc Introduce not_enough_arguments_for_intrinsic() helper
## 679bacf Implement type checking for mem intrinsic
## 09bdf2e Implement type checking for the rest of the syscall intrinsics
## 093710d Implement type checking for argc and argv intrinsics
## ee86ae6 Fix human() function
## fb214ae Merge pull request #82 from tsoding/type-checking
## 3ce5a33 Make stack.porth type check
## a98e0ef Merge pull request #83 from tsoding/type-check-stack
## 277ed40 Make arithmetics test case type check
## fa081eb Merge pull request #84 from tsoding/arithmetics-type-check
## 7652fc2 Make comparison.porth test case type check
## 9162422 Make bitwise.porth test case type check
## 9be4b6c Make memory.porth test case type check
## 6240fce Merge pull request #85 from tsoding/type-checking
## 6aaf02a Introduce compiler diagnostic functions
## 96e8aa7 Merge pull request #91 from tsoding/compiler-diagnostic-functions
## 3ca1ab9 Replace Loc in Op with Token
## 61096b9 Merge pull request #92 from tsoding/op-loc-token
## 94df323 Add CONTRIBUTING.md
## 99993bb Make the warning more noticable (hopefully)
## 8269e89 Print expansion stack during compilation errors
## 038327e Merge pull request #93 from tsoding/expansion-stack
## 80c3be9 Typo
## caf774b Implement type checking for else-less if
## 13a46f7 Implement type checking for if with else
## 1b01538 Implement type checking for while-do loops
## 8c0f554 Make all of the test cases type check
## 9bc9591 Make all the examples type checked
## e4b13f4 Introduce -unsafe flag that disable type checking
## d0cfc2e Make all the euler solution type check
## 0cc9bd9 Merge pull request #95 from tsoding/type-check-control-flow
## ffc6c8c Fix CI running twice on PR
## 3106a14 Merge pull request #96 from niyrme/patch-1
## c0bfe05 Introduce nth_argv macro
## 3c3fa22 Merge pull request #97 from tsoding/nth-argv
## 7e8e0a2 Implement cat utility
## 26fe1c9 Try to fix the build
## 683708e Try to fix mypy remarks
## c58f39f Merge pull request #100 from tsoding/cat
## 4bd68c2 Fix while-do type checking limitation
## f7de847 Add type checking tests for conditions
## 20fd31e Add type checking tests for while-loop
## 29aedc5 Remove control-flow test
## 40f5879 Merge pull request #101 from tsoding/while-do-type-check-bug
## 5d7b6eb Separate compiler diagnostic with expansion stack
## 3e3b70b Merge pull request #102 from tsoding/compiler-diagnostic-with-expansion-stack
## 6a88426 Implement rot13 example
## 92ca296 Merge pull request #103 from tsoding/rot13
## 5f9af58 Make examples in README compilable
## c484f60 Proper seq implementation
## 3582219 Merge pull request #104 from tsoding/seq
## 73c9e1d Remove TODO about type checking operations that never return
## acf4d16 Remove TODO about several test cases per single program
## 208cf73 Remove TODO about profiler mode
## 9f49322 Ignore test case when *.txt files is missing
## 24cf5fa Add fib example
## e4e4f5d Cleanup magic constants
## 572ec20 Merge pull request #108 from tsoding/fib
## 6912747 Rename bor -> or, band -> and
## ddcb21b Implement `not` intrinsic
## 3368c98 Fix compilation of examples
## 13b7437 Fix compilation of Project Euler solutions
## 0b8db24 Merge pull request #109 from tsoding/logic-operations
## 2ad2af2 Implement `here` intrinsic
## 28e9e5a Move puts to std.porth
## 586f560 Use `puts` in all of the test cases
## e1151e8 Add eputs to std.porth
## bdaecb9 Use puts and eputs in all of the examples
## d3c2c65 Use puts in the README examples
## 5919c68 Merge pull request #110 from tsoding/here
## f14a1ba Simple Game of Life implementation
## 5c442cc Merge pull request #111 from tsoding/gol
## b579020 Forgot that Porth is already statically typed
## 2152dd4 Add wrapper for clock_nanosleep to std.porth
## 2562314 Introduce `rot` intrinsic
## 0dcf77d Remove trailing whitespaces
## 9f64e79 Remove gol.txt to make test.py ignore the example
## b3616a1 Make GoL example iterate indefinitely
## 0e0eaa7 Implement SYS_clock_nanosleep for simulation mode
## d60c17a Merge pull request #112 from tsoding/cooler-gol
## 17baf66 Add solution for Project Euler Problem 06
## 89b0f60 Add solution for Project Euler Problem 07
## c393d86 Merge pull request #113 from tsoding/more-euler
## 42f1afb Introduce Forth-style memory access intrinsics
## b2c0c46 Merge pull request #114 from tsoding/forth-style-memory-access
## d6e522a Add dec64 to std.porth
## ef2fa7f Add `then` and `elif` keywords to the Emacs mode
## 707f087 Add `then` and `elif` keywords to the vim plugin
## 8cec1a7 Initial implementation of Porth compiler in itself
## ccfeb65 Implement subcommands for porth.porth
## 6035483 Report the name of the command on unknown command error
## fdd3915 Introduce help subcommand
## adcd9ff Remove `then` keyword from the editors support
## 7d0ed74 Add FizzBuzz example
## cbb7acc Test if the ignored test cases at least compile
## e8b41a3 Merge pull request #121 from tsoding/fizz-buzz
## 1d55d2e Introduce an idiom to simulate structs in Porth
## be6df40 Compile porth.porth on CI
## 3678ee3 Merge pull request #123 from tsoding/op-struct
## 56015f0 Refactor conditions to have `if-do-else-end` form
## b5f9863 Fix else-less-if-fail test case
## cb32b98 Fix macros test case
## 78c6b9d Fix if-else-fail test case
## 47d3a73 Fix if-else test case
## c763ea3 Fix else-not-inside-if-error test case
## 1675e43 Fix end-cant-close-error test case
## a942592 Fix else-less-if test case
## 461cb57 Fix the cat example
## 93dc59a Fix rot13 example
## f52f7ea Fix name example
## 0f8cbf9 Fix rule110 example
## 6bbb230 Fix FizzBuzz example
## f4049d2 Fix seq example
## 50448c4 Fix gol example
## 895a61d Fix Project Euler Problem 05
## bbc55b3 Fix Project Euler Problem 02
## adce6f0 Fix Project Euler Problem 07
## 4361b4e Fix Project Euler Problem 01
## 6e70dc2 Fix Project Euler Problem 03
## 28839ff Fix Project Euler Problem 04
## 02e1cb6 Update documentation about `if` construction
## eeb79e4 Fix porth.porth
## 73fb6be Fix mypy errors
## dcdfc8a Merge pull request #124 from tsoding/if-do
## 1f1926a Rename compilation phase to parsing phase
## 07e853a Merge pull request #127 from tsoding/compile-to-parse
## e4aa446 New lines in assertion messages
## 0a80496 Rename strlen -> cstrlen
## 79bb051 Rename streq to cstreq
## 7d98aec Implement cstr-to-pstr
## 990dbb2 Implement C-style string literals
## 4116de7 Document C-style Strings
## ebeda8c Remove TODO about implementing NULL-terminated strings
## 747f17e Merge pull request #132 from tsoding/cstr
## 3c540b4 Output usage to stdout in case of the `help` subcommand
## b4b6ed7 Merge pull request #133 from tsoding/help-stdout
## abe61ec Implement -cf flag for the compilation mode
## 4777728 Fix mypy remarks
## 9769559 Merge pull request #138 from tsoding/control-flow
## 8e333a9 Implement support for elif keyword
## 2eaeecf Implement type checking for elif chains
## 289b571 Use elif in porth.porth
## b73045b Fix test cases
## 74d9293 Add TODO about a type checking bug
## 33cfddc Merge pull request #140 from tsoding/elif
## fd8046e Cleanup logging during Control Flow graph generation
## d451ded Merge pull request #142 from tsoding/clean-up-control-flow
## 5b38fb3 The development is moved to GitLab
## 96efeda Revert "The development is moved to GitLab"
## 8fdbb05 Update Language Reference
## f1073f1 Try out intrinsics documentation in form of a table
## a8cda8e Drop parens in the intrinsics signatures
## 12e9a58 Check how bitwise section is rendered
## 1bde7e9 Try to fix the rendering of the Bitwise section
## e4be390 Use table for the Memory section
## 595f213 Remove parenthesis from the signatures
## 4d62337 Remove the unreachable code and fix the unreachable asserts
## 234f336 Rename test case else-less-if -> if-else-less
## eb7f2db Merge branch 'fix-type-checking'
## 7559ca1 Implement a better Type Checking strategy
## ce0e2b1 Merge branch 'fix-type-checking'
## f46a35c Add solution for 8th Project Euler Problem
## e7df1ef Add solution for 9th Project Euler Problem
## 8f61b6a Report "no pre-do" error properly
## 30597e0 Deprecate old style 64 bit memory access intrinsics
## 1a993f1 Deprecate old style 8 bit memory access intrinsics
## 2e15628 Make 8 bit memory access intrinsics more consistent with 64 bit ones
## cb96f71 Merge branch 'remove-old-style-store-load'
## 5abd5dc Tweak wording
## 5a2c804 Remove the FORTH_* prefix from 8 bit memory access intrinsics
## ed0e54d test
## f271d14 Add memory-map-file.porth
## 2cebbf0 Add more stuff to std.porth
## f4b7293 Remove debug logging
## 53e935f Add words analyzer to examples
## 23d390c Merge branch 'self-hosted-parsing'
## 0b94b00 Add the rest of the cast intrinsics
## 8b71215 Merge branch 'all-casts'
## 178b37c Revert "test"
## 324e3b3 Remove mentioning of `.` and `.64` intrinsics from the reference
## 30e94ee Refactor reversed-linked-list example
## 1f1e258 Use struct accessor style from reversed-linked-list example in Porth
## d8627c5 Use !Op.operand in porth.porth
## 955189a Better Str struct accessors
## 277e8dd Use type casting in the definition of `true` and `false`
## 9304758 Merge branch 'refactor-reversed-linked-list'
## b19df02 Stub conventions section
## d7fa572 Fix crash on type checking empty program
## eedccc6 Merge branch 'empty-program-bug'
## af6e6ab Add a note to porth.porth about what it is
## 76101cc Add another milestone to the plan
## d120972 Refer to the current progress in the "Self-hosted" milestone
## 3619e2d Remove mentioning of `,` and `,64` intrinsics from README
## c4e433d Add solution for Project Euler Problem 10
## 11ce39e Integrate self-hosted parsing into porth.porth
## c6288a7 Unhardcode dump subcommand
## 1690251 Merge branch 'self-hosted-parsing'
## 77aa504 Update CONTRIBUTING.md
## 7616e8b Rename 8-bit memory access intrinsics
## c39744b Implement 32 bit memory access intrinsics
## 9ba3bc1 Use 32 bit numbers in Project Euler Problem 10 to reduce memory usage
## e540914 Merge branch '32-bit-mem-access'
## 233ab17 Get rid of loops from memory access intrinsics in simulation mode
## d02b7d6 Add more details about Project Euler Problem 10 performance
## 9390b9e Add support for `-` intrinsic to porth.porth
## 4f15600 Add logical not to std.porth
## c4e5f4c Add isdigit to std.porth
## 9f4b0be Report location of unknown words in porth.porth
## 12cf637 Implement `dup` and `drop` for porth.porth
## ae0d740 Implement 16 bit memory access intrinsics
## 05d7895 Fix error in the documentation
## e83bb4f Implement memory region definition
## 6d83a23 Use memory sections in porth.porth
## 1df87d0 Fix compilation of GoL example
## 6d68f14 TODO: check of stack underflows in memory definition
## 35f0390 Fix bug while parsing macro containing memory block
## 847ed04 Merge branch 'better-memory'
## ef87796 Don't use mem in Project Euler solutions
## f5511d3 Don't use mem in unit tests
## 10d4d15 Don't use mem in examples
## 844acdf Fix mypy remarks
## 85273a3 Implement simple PPM generator
## 94921cf Fix porth.porth
## 67e06a5 No need to have a flag to customize memory capacity
## 9b16e56 Fix example in README
## ff42c7f Implement MUL intrinsic for porth.porth
## d39e8b4 Move a bunch of things to std.porth
## 6dc2c48 Make porth.porth run nasm and ld as child processes
## 14713bc Fix "not enough argument" error reporting for do blocks
## 828243d Add full subcommand to test.py
## cc06f09 TODO about bug in test.py
## 1815842 Proper error reporting for memory redefinition
## 298a316 Proper error reporting on memory redefining intrinsic
## 9c510a8 Proper error reporting on memory redefinining macro
## 0bdd26a Factor out check_word_redefinition()
## 400c21a Report unsupported keyword in memory definition properly
## ab1c464 Report stack underflow in memory definition properly
## c4f7053 Improve error reporting in memory definition
## 7be8b3b Remove obsolete TODO
## 177b006 Remove obsolete TODO
## ca2f74f Merge str-chop-word and str-chop-line into a single macro
## 47329a1 Implement procedures for compilation mode without type checking
## 488fc9c Fix proc redefinition error
## 321c007 Fix simulation mode
## 324eddb Rough implementation of the typecheck of procs
## b6916d2 Fix the tests
## f4c9d01 Disable type checking for now
## 9279f4f Merge branch 'proc'
## 978f3a2 Elaborate on how to use `-unsafe`
## 34b3d70 Don't disable type checking in debug mode
## 997dcfd elif -> orelse
## 1f772df Add while-alter test case
## 02d37ab Always in debug mode for now
## 12ba823 Add while-procs test case
## 3218640 Fix type checking loops inside of procs
## afa1e7e Update README
## cfe0f7c elif -> orelse
## cf25d36 [porth.porth] Separate intrinsics from ops
## bf29e5a [porth.porth] draft
## d7fdd95 Fix unclosed orelse block bug
## 9161bf8 Merge branch 'orelse-bug'
## 63b993f Add test case for unclosed orelse bug
## 4e3b7b6 [porth.porth] translate as many intrinsics as possible
## 048c9fa Merge branch 'master' into all-intrinsics
## 712fdfd Merge branch 'all-intrinsics'
## 1a264b3 [porth.porth] implement `if-end`
## 7434dc7 [porth.porth] Check for ops overflow
## 3949a5b [vim] Highlight keywords as keywords
## cb154d0 [porth.porth] add support for comments
## ddcb7ca Fix TODO spelling
## 3453a77 Report the location of the original proc definition
## dd2ecac Merge branch 'original-proc-def'
## 0d9c095 Implement constants
## 8cb7cda Document the Use Case for Porth
## ecfb063 Merge branch 'consts'
## 14c2dce Partial implementation of local memory
## 20f6084 Fix global memories shadowing the local ones
## a4efd17 Cleanup debug comments in the generated assembly
## ab6dcff Implement local memory for simulation mode
## efd5343 Merge branch 'local-memory'
## 7d297c1 [porth.porth]delete try_to_parse_word_as_int_or_fail_as_unknown_word
## 149c9be [std.porth] use local memory for streq
## e7ac452 [std.porth] use local memory in memcpy
## babb630 [std.porth] use local memory in fputd
## cde20ef [porth.porth] Move external command related stuff to local memory
## e05bb15 [porth.porth] move out-fd to local memory
## 7384a5b [porth.porth] move file-path-cstr to local memory
## 2132747 [porth.porth] move parsing related vars to local memory
## c448252 offset/reset
## eb86a6c [std.porth] start using consts in appropriate places
## 8e2d154 [porth.porth] move more stuff to local memory
## 11603fa We don't need memory layout convention anymore
## 52bd8da We don't really have any array conventions
## 8a7b869 Move str-chop-by-delim stuff to local memory
## b9bb98d Outline what needs to be documented
## 36f3b06 Implement if*
## 8fd75e9 Fix if-orelse test case
## 56b4731 Fix else-not-inside-if-error test case
## 9303aa3 Fix compilation of porth.porth
## 0cffb0a Merge branch 'if-star'
## 09de628 Deprecate nop
## 9f23650 Refactor try-parse-int test case
## 71b1c5b Rename putd -> putu
## 157023f [std.porth] remove all macro usage
## f2d60f1 [std.porth] remove @ptr
## 881434d [std.porth] elaborate on possible solutions for true/false problem
## e296355 Introduce different types of constants
## 5d873fb [std.porth] Make NULL ptr
## 189f80b Purge Macros
## 07499cc Call Path Error Reporting
## f79b602 Remove TODO that was resolved by 07499cc
## 4461632 Type Checking Call Limit
## 3eb71da [porth.porth] implement support for `else`
## 3883c25 [porth.porth] outline `include` implementation
## c48909c Implement `max` intrinsic
## f5c9ae4 [porth.porth] outline a proper lexer
## 184aa6d Fix the tests
## bb70fb2 [porth.porth] Make lex-file report locations of the tokens
## 64b6283 Introduce static asserts
## 69e1fad Use static asserts in porth.porth
## 6f38a63 Fix mypy remarks
## b1a1a47 Merge branch 'static-assert'
## 339b82b [porth.porth] Integrate the lexer into the parsing process
## c8625f0 Implement proc signatures
## a12cbaf Extend the plan
## 9747120 Fix test cases
## a2e22d2 Fix examples
## 187ef67 Fix Euler Problems
## 1a76999 Merge branch 'proc-signature'
## bb6d370 Outline Intrinsics contracts
## a7caeef Remove call path related stuff
## ce0e0cd Get rid of compiler_error_with_expansion_stack
## 937c218 Remove TYPE_CHECK_CALL_LIMIT
## c3e3290 Try to make type checking error messages more useful
## 8b51082 Use type contracts for intrinsics where applicable
## bf392c2 Implement overloaded type contracts
## 0bf1239 Implement generics
## b68673d Merge branch 'intrinsic-contracts'
## 631645f Improve error message on loops altering the stack
## 8b0a1db Fix tests
## deb05f3 Make memcpy return dst
## 03ff510 [porth.porth] implement include keyword
## deaaa4a Update README
## dd8d1bf Tweak type check error messages
## 4a0490e [std.porth] add simple LCG implementation for random numbers
## 337fd05 [examples] implement Bubble Sort
## 4d4e1c2 [std.porth] move swap64 to std.porth
## a9bd81c [porth.py] check_word_redefinition -> check_name_redefinition
## b06a45c [examples] implement quine
## 56d9f94 Merge branch 'porth-porth-consts'
## d10eb3e gitignore quine example executable
## 362f9e5 [porth.porth] get rid of the Op struct accessors
## 845d4b9 [porth.porth] group things according to how related they are
## 93b3b08 [porth.porth] introduce eputloc and fputloc
## 813f57d [porth.porth] Introduce data structure for const definitions
## 0a366cf [porth.py] TODO about type contracts in eval_const_value
## 9ef9e65 [porth.porth] introduce stack for const evaluation
## fc12757 [porth.portg] Implement `human-token-type` and `const-stack-push`
## b7838ae [porth.porth] implement intrinsic-by-name
## 09d8226 [porth.porth] finish eval-const-value
## 3208d0f [porth.porth] fully implement const definition
## d3dc782 [porth.porth] finish self-hosting
## efa8a04 [porth.porth] Allow cast(bool) in constant definition
## 5be4b57 [porth.porth] allow using other constants in constant definition
## 801d634 [porth.porth] define structure for procedures
## d0c547d [porth.porth] compress intrinsics compilation lookup
## 3de408e Implement envp intrinsic
## 4eea23f Fix the envp bug when CLI arguments are provided
## d53fb43 [porth.porth] make cmd-echoed search in $PATH
## 26d41cc Fix tests
## bed0663 [porth.py] introduce `stack` intrinsic
## 04316d2 [porth.porth] move tmp scratch buffer to std.porth
## 958273b [porth.py] rename `stack` intrinsic to `stop`
## cdb1c43 [porth.py] fix build
## 2cfd2db [porth.py] remove unnecessary proc_addr computation
## 64db2f8 [porth.porth] advance the implementation of procs
## 2873bd5 [porth.porth] advance the compilation of std.porth
## 2a6cfef [porth.porth] advance the compilation of std.porth even further
## b3c7be1 [porth.porth] introduce procs definition table
## 9ea13c4 [porth.porth] implement parsing proc calls
## c88c247 [porth.porth] introduce memory struct
## 086abea [porth.porth] advance the compilation of std.porth
## 99b224e [porth.porth] advance the compilation of std.porth
## d831b48 [porth.porth] introduce `while` into IR
## 0ed1b5f [test] Add test for local memory "overshadowing"
## b9cbd19 [porth.porth] uncomment pushing local memory
## 5ac635b [porth.porth] implement memory related minor functionality
## 7d2c754 [porth.porth] introduce `do` into IR
## 6566bf4 [porth.porth] implement parsing of `do`
## 6d76da9 [porth.porth] make example/fib.porth compilable and simulatable
## 9995d09 [porth.porth] offset/reset
## 15dbc14 [porth.porth] implement parsing of character literals
## ec177bd [porth.porth] implement parsing of string literals
## 9a2748f [porth.porth] introduce `envp` intrinsic
## c6b4ef7 [porth.porth] allow intrinsic `*` in compile time evaluation
## 15126a6 [porth.porth] assert
## 9fb57a4 [porth.porth] enable `=` intrinsic in compile time evaluation
## 02fdb16 [porth.porth] add `if*` to IR
## df05911 [porth.porth] implement parsing of `if*`
## 0d1f5ac [porth.porth] stub chaining of else-if*
## 9d1d199 [porth.porth] implement chain-else-if*
## 5510b58 [porth.porth] introduce intrinsic `max`
## a167d99 [porth.porth] introduce C-style strings
## 4260f6b [porth.porth] introduce string literal buffer
## bf20d29 [porth.py] fix escaping in string literals
## b828473 [porth.porth] porth.porth can finally self-compile into its own IR
## 47fb3f1 Question the necessity of multiline strings
## f1c5ce8 [porth.porth] clean up the "not implemented" error messages
## bf7105b [porth.porth] parse_file_path_cstr_into_ops -> compile-file-into-ops
## c349155 [porth.porth] compile-ops -> generate-nasm-linux-x86_64
## 4fa268e [porth.porth] document `lex` subcommand
## 855156b [porth.porth] add `summary` subcommand
## 9023722 [porth.porth] implement procedure related ops
## 8d689cd [porth.porth] implement OP_PUSH_LOCAL_MEM
## 5620a0b [porth.porth] strlit -> strbuf
## d5dcd28 [porth.porth] introduce strlit array
## ed672c7 [porth.porth] implement `here` as a keyword
## 1bad2c9 [porth.porth] commit the current state of the development
## 1fd10f8 [porth.porth] move comment string back to local memory
## 9974cd3 Merge branch 'self-compile'
## 4288fcc [porth.porth] parse comments like a normal human being
## 27fc5f4 [porth.porth] self-hosting
## b3e2813 [porth.porth] enable `+` intrinsic at compile time
## cd56c30 Fix the tests
## 9bc8aba Compile porth with itself during testing
## 74954b5 Move str-starts-with and ?str-empty to std.porth
## 5c45dc6 [porth.porth] TODO about type checking
## 5f62af2 [porth.porth] truncate the output file
## 5e4d61a [porth.porth] introduce append-item
## 47b2248 [std.porth] identify and fix memset bug
## e42eaf6 [porth.py] implement execve syscall
## ec1c955 [porth.py] implement mem_alloc for easier memory layouting
## 6cea8db [porth.py] Implement SimBuffer for the simulation mode
## a8d8d14 [porth.py] implement `envp` intrinsic in the simulation
## 55ca4f7 [std.porth] identify and fix execvp bug
## 3a86148 [porth.py] try a different approach to error messages
## 72191d0 [porth.porth] make usage print the actual name of the program
## 2be3f7d [porth.porth] implement `-r` flag for `com` subcommand
## f660a84 [porth.porth] implement `-s` flag for `com` subcommand
## d8a4f18 [porth.porth] use tmp memory for external commands
## e2f2c99 [euler] add problem 12
## 071cbb2 [porth.porth] implement tmp-rewind
## ee4ccb4 [porth.porth] hard code include paths list
## 3135192 [porth.porth] make generate-nasm-linux-x86_64 accept the output path
## 7aceeff [porth.porth] start grouping entities
## 8400801 [porth.porth] grouping entities
## b072ef4 [porth.porth] grouping entities
## 7f0eb58 [porth.porth] grouping entities
## e121368 [porth.porth] check if string literal was actually closed at the end
## 1e57be2 [porth.py] Fix quote in character literal bug
## 872d32b [porth.porth] fix quote in character literal bug
## 317b2c5 [porth.porth] simulation mode can simulate examples/hello.porth
## 257e0a8 [porth.porth] simulation mode can simulate examples/name.port now
## 48c10d5 [porth.porth] simulation mode can simulate examples/quine.porth
## 69f3d87 [porth.porth] the compile can kinda simulate itself
## 9b3549f Add the thumbnail example
## ccb6aa0 [porth.porth] handle the result of wait4
## 38b2533 [porth.porth] implement `max` intrinsic in the simulation mode
## 95f0d4c [porth.porth] pass args to the compiled output program
## 9287274 [porth.porth] make porth.porth pass ./tests/argv.porth
## 2f9382b [porth.porth] introduce `-check` flag
## ec2ee01 [porth.porth] Properly escape the logged CMDs
## ac98e7b [porth.porth] TODO: report that you could not execute the child
## 8f7d030 [porth.py] introduce `check` subcommand
## e660764 [porth.porth] Implement Type Frame Pool and Type Stacks that use it
## 69c0206 [porth.porth] display types of frames in dump-dot-type-frame-pool
## 38bd4d3 [porth.porth] Generate more interesting topology of type frame pool
## ccb963a [porth.porth] implement type checking of OP_PUSH_INT
## 5bc1b8e [porth.porth] outline type checking of intrinsics
## 440eaae [porth.porth] double the size of the string buffer
## 6c89667 [porth.porth] More TODOs
## 882404d [porth.porth] report capacities in the `summary` subcommand
## 2091bcb [porth.porth] double the capacities of the buffers
## d36a5a3 [porth.py] remove internal overloading of intrinsics
## 85e4bc5 [std.porth] make the standard library compile
## 99dcc05 Fix unit tests
## 662a39e Fix examples
## 78ec7f7 Fix project euler problems
## 269799e [test.py] list failed files
## 3d66acc [porth.porth] fix compilation
## 6a8ee42 Merge branch 'remove-overloading'
## 2ad7b04 [porth.py] remove generics
## 4fdcbb8 [porth.py] remove human_type_name()
## f8e64d1 [test.py] show failed fails only if the tests have failed
## fde38e6 [porth.porth] partially implement type checking of the `+` intrinsic
## b31b039 [porth.porth] implement "not enough arguments" error reporting
## a9cb923 Clean up some TODOs
## 50a1b67 [porth.porth] append the outs after checking the type stack
## 789130a [porth.porth] implement type checking for print operation
## 6877383 [porth.porth] fix location of appended outs in type checking process
## ad826cd [porth.porth] implement type checking of the expected outputs
## 43b1c4b [porth.porth] add `ins` and `outs` contracts to proc definition
## 443e04d [porth.porth] replace skip-proc-contract w/ parse-proc-contract-list
## b611a29 [porth.porth] implement type checking of OP_SKIP_PROC
## c9d41d3 [porth.porth] implement type checking of the procedures
## 96fef74 [porth.porth] type checking for `@64`, `cast(ptr)` and `drop`
## 89edf0c [porth.porth] type checking for OP_RET
## d023662 [porth.porth] Type checking for OP_CALL and INTRINSIC_CAST_BOOL
## 76dd35e [porth.porth] type checking for INTRINSIC_STORE64
## d149905 [porth.porth] remove debug logging from summary subcommand
## 8ccd184 [docs] update the convention in Structs section
## 1dfa2b7 [docs] putd -> putu
## cd68ee5 [porth.porth] implement more type checking
## 8715f03 [porth.porth] implement type checking for some syscalls
## f674f2b [porth.porth] rewind tmp only at the end of the iteration
## 3cf9244 [porth.porth] remove test-type-check subcommand
## 58ce14e [std.porth] TODO about tmp-rewind debugability
## c87f25f [porth.porth] introduce type-check-int-operator
## b8a8aab [porth.porth]type-check-int-operator->type-check-binary-int-operator
## b2f320e [porth.porth] introduce type-check-unary-int-operator
## 148461d [porth.porth] introduce type-check-cmp-int-operator
## df0af9a [porth.porth] advance type checking
## 96ac4fa [porth.porth] introduce type-check-store-operator
## 110cd34 [porth.porth] typechecking for OP_PUSH_LOCAL_MEM
## 1161d9b [porth.porth] typechecking for OP_WHILE
## 22680ef [porth.porth] implement type checking for loops
## 90ff236 [porth.porth] keep track of the loop start separatly
## b7845e2 [porth.porth] type check if-else-end
## 973a5dc [porth.porth] implement typed push instructions
## 5f2718b [porth.porth] type checking for rot operation
## c32fec9 [porth.porth] porth.porth can fully type check itself
## ad01c3c [porth.porth] replace reference counting idea with rewinding
## 8e4b035 [porth.porth] type checking for argc intrinsic
## 2cfbf0e [porth.porth] implement argc intrinsic for simulation mode
## a39307c [std.porth] make map-file not crash on empty files
## a4083ef [porth.porth] make the error message more consistent with porth.py
## 38b9e07 [std.porth] make execvp inherit the current envp
## 1962b5d [porth.porth] type check by default, replace -check with -unsafe
## 9189c0b [porth.porth] implement "unhandled data on the stack" report
## 979325d [porth.porth] TODO about closing `if*` with `end`
## 0e87a37 [porth.porth] implement `???` intrinsic
## 7952bf5 [porth.porth] implement closing `if*` with `end`
## 990c701 [porth.porth] introduce `-fasm` flag
## 46244ec [porth.porth] implement reporting insufficient data on the stack
## 2bf6884 [porth.porth] implement reporting proc inside proc error
## 355a350 [porth.porth] implement -t flag
## 5f43f2b [porth.porth] descrease memory usage on type checking
## d86d961 [porth.porth] remove dead code
## 93ce5e8 [test.porth] so it begins
## 6b871bd [porth.porth] implement generate-print-intel-linux-x86_64
## 7584d0b [porth.porth] implement generate-op-intel-linux-x86_64
## fa26131 TODOs
## 1b7ab41 [std.porth] introduce simple facilities for timing code execution
## dd5b13c [porth.porth] time all the phases of the compilation
## c6c6b64 Remove Simulation Mode
## 0dd48ea Add `inline` keyword to vim and emacs extensions
## 720f05c [porth.py] introduce `inline` keyword
## 45017bb [porth.py] forbid non-inlinable things in inline procedures
## 71401d1 Implement the procedure inlining
## 1739d8f [porth.porth] Make `timeit/to-here` consider the -s flag
## e0c32c4 [std.porth] make small functions inlinable
## a0f3c7e [porth.py] make the inline error messages more usable
## 280474a Add TODO for inline procs for porth.porth
## b13ad0a Merge branch 'inline-proc'
## a4d3cc7 [porth.porth] inline some of the small procedures
## 710b292 [porth.porth] implement introduce-proc
## 6449f78 [porth.py] problems with inlining
## 17231f7 [porth.porth] implement inline procs
## 8e9c6b4 Merge branch 'inline-porth-porth'
## 0f67680 [porth.py] fix type checking for inlined procedures
## 14958ef [porth.py] do not allow recursion in inline procedures
## a66ff00 [porth.py] do not allow recursion in inline procedures
## 8b320e7 [std.porth] timeit/to-here has too much responsibility
## 26867c5 [porth.porth] consistent logging
## b3c10a8 [porth.porth] introduce Proc.size
## c6f5af9 [porth.porth] Introduce OP_INLINED instruction
## b069dc2 Merge branch 'op-inlined'
## 4f69b99 [porth.porth] Fix ./tests/include-file-not-found-error.porth
## 6096df0 [porth.porth] Make cmd-echoed handle the child's exit code
## 0c99142 [porth.porth] fix ./tests/no-include-file-error.porth case
## c5020cc fix `tests/memory-redefinition-of-proc.txt` case
## 0998c98 [porth.porth] fix `./tests/memory-single-number.porth` case
## e9d7f59 [porth.porth] fix `./tests/memory-unsupported-word.porth` case
## c049380 [porth.porth] fix `./tests/no-proc-name-error.porth` case
## d0dda8a [porth.porth] fix `./tests/memory.porth` case
## cce7058 [porth.porth] fix `./tests/if-else-fail.porth` case
## ade7f49 [porth.porth] fix `./tests/memcpy.porth` case
## 8b48cf2 fix ./tests/original-proc-def-error.porth case
## 300bb23 [porth.porth] fix `./tests/memory-definition-stack-underflow.porth`
## e1ae34b Fix `./tests/memory-redefinition.porth` case
## 8d22ca1 Fix `tests/unclosed-character-literal-error.txt`
## 163bd44 Fix `./tests/else-not-inside-if-error.porth`
## 8fa03f5 Fix `./tests/proc-redefinition-error.porth` case
## fa7ddc0 Fix `./tests/proc-inside-of-proc.porth` case
## 1799132 Fix `./tests/end-cant-close-error.porth` case
## 62613a4 Fix `./tests/multi-byte-character-literal-error.porth` case
## a7f913c Fix `./tests/unknown-word-error.porth` case
## 40cd4ed Fix `./tests/wrong-include-path-type-error.porth` case
## b79df7a Fix `./tests/unclosed-block-error.porth` case
## c75032e Fix `./tests/memory-redefinition-of-intrinsic.porth`
## 0608e22 Fix `./tests/unclosed-string-literal-error.txt`
## 3aa66b7 Fix `tests/not-enough-args-for-do.txt` case
## 29bb52c [porth.porth] introduce the notion of a keywordd
## 2e9bdce [README] add editor support section
## c9e3111 [std.porth] implement dirname
## 7b10247 [porth.porth] introduce include limit
## 234a6ed [porth.porth] implement reporting unexpected type on the stack
## bffba38 [porth.porth] elaborative error messages on unexpected stack data
## d936008 [porth.porth] stylistic changes in `dump` output
## 512e56e [porth.porth] introduce OP_START
## 263a453 [porth.porth] loop typechecking relative to `while` instead of `do`
## 2fc040e [porth.porth] add bootstrap folder
## 6656912 Reprioritize TODOs
## d1dd259 [porth.porth] remove dead code
## 45a47bf [std.porth] add str-rfind
## db8a00e [std.porth] make str-rfind return negative number on not found
## 97ceb3b [std.porth] add remove-ext
## d72241b [std.porth] move cmd-echoed to stdlib
## 7687d66 [test.porth] advance the implementation
## 2515966 [porth.py] increase the size of the stack
## 388d430 [porth.py] make `here` a keyword
## bfc87ff Remove bootstrap folder
## ee61fad [porth.py] remove -cf flag
## bf826c7 [porth.py] rename PUSH_MEM -> PUSH_GLOBAL_MEM
## c285292 [porth.py] TODO about the start operation
## 42aeb89 [porth.py] get rid of the ip variable in ParseContext
## 7732737 Remove irrelevant TODOs
## 8d8abee Remove porth.py
## d293268 [README] refer to the porth.porth file in the intro
## 5428a76 [porth.porth] update the note at the top of the file
## 83af371 [README] typo
## a1eb56d [README] typo
## bb5839d [test.porth] add note about rewrite
## 06365b6 [porth.porth] TODO about ignoring files that were already included
## f76b6d6 [porth.porth] reimplement dirname in terms of str-rfind
## a5893f0 Require programs to put all of their code in the `main` procedure
## e3e80cd Remove OP_SKIP_PROC instruction from IR
## e84b924 Remove OP_START instruction from the IR
## f722df4 Fix the tests
## 56fa8f2 Update README
## b08e5e0 Update asm files for bootstrapping
## bd28322 gitignore boostrap executables
## 1867051 Merge branch 'entry-point'
## 25b8a1a Remove dead code
## 03dfc25 Remove `-unsafe` flag
## 35c14e0 Verify `main` procedure signature
## c814688 Update boostrap assembly files
## 64a0c76 Fix non-exhaustive handling of Op types in print-op-type
## 8082560 Update bootstrap assembly files
## 24fbd02 [README] trim leading whitespaces
## 585488f Introduce type `addr`
## 654ed10 Implement `addr-of` keyword
## f14fc32 Implement call-like keyword
## af65204 [README] Stub Procedure Pointers section
## 52f0eaa Update boostrap folder
## 54a9a8b TODO: factor out the args of type-check-program-from into structure
## 3ff5eca TODO: `"/" dirname` removes the last slash
## 5e55709 [std.porth] Fix dirname
## c206310 Set output file path based on the input file path
## eb7d3b8 [test.porth] make it compilable again
## a1041a9 Prioritize TODOs
## 104f137 Move `args` to local memory of `main` proc
## 3a09b70 Add support for dos newlines
## af5c298 Treat *.txt files as binary but keep them diffable
## db0e578 TODOs
## 4dc82b1 start-ip -> block-start-ip
## c987366 Implement update-bootstrap.porth "script"
## 1b837d9 Annotate generated assembly
## 16bafe4 Factor out the args of type-check-program-from into structure
## 3dba759 Merge update-bootstrap.porth into test.porth
## bbe6859 Use shell DSL in test.porth
## c600d2b Fix stack underflow diagnostic in compile time evaluation
## 6b27537 Make cmd-echoed indicate that the child process was signaled
## d889987 Revert "Remove `-unsafe` flag"
## 1963a2e Allow additional characters in identifiers
## 2385094 Add if* as an explicit keyword
## e3288bf Highlight escapes, numbers and compiler recognized types
## 08cdc27 Merge branch 'feature/improve_vim_highlighting' into 'master'
## 27f99a0 Double the size of the ops buffer
## f526f98 Fix assembler warnings on empty string literals
## 2d9ebf9 Add \\ as a valid escape to vim syntax for porth
## f925082 Merge branch 'fix/add_backslash_backslash_as_a_valid_escape' into 'master'
## 0e074c6 Initial implementation Let-bindings
## 8ae08fe Rewrite fputloc using let bindings
## 7ce5833 Simplify assembly generated for let-bindings
## 9ace05c Add let keyword to vim and emacs extensions
## b3844a6 Use let-bindings in more places
## f84f00f [README] ./porth.py -> ./porth
## ce8c369 Use let bindings for `usage` implementation
## 8423acc Fix let bindings corrupting local memories
## 6fc0b3a Align all the memories to the size of the word
## ba41d5b [README] fix example
## af27524 [std.porth] use let-bindings for some of the procedures
## 720d062 Fix bindings locations in diagnostic messages
## c38a342 Make fasm-linux-x86_64 the default target
## 034fe8d Rewrite bind-table-rev-top using let-bindings
## 4b7e5d3 Simplify bind-table-rev-top implementation
## 176f331 Implement idivmod intrinsic
## 133e786 Implement imod, idiv and emod
## edcdda5 [snake.porth] add more POSIX-y stuff
## 0fededa [snake.porth] Add the unfinished snake game
## 0ef0d51 [snake.porth] use cell-at where appropriate
## 5ee6487 [snake.porth] player -> head
## 9947592 [snake.porth] wider play area
## db6ce4e [snake.porth] make step-point a pure function
## a13f641 [snake.porth] implement spawn-snake
## 73adc0b [snake.porth] mention the stty hack
## 4754afd Add support for syntax highlighting in Sublime Text
## 3003e4b Improve parsing for highlighting in Sublime
## 64f79ac Allow assert outside of proc in sublime-syntax
## 29054fa Fix highlighting of `end` keyword in Sublime
## 417f83e Introduce Module structure
## 6fc5684 Remove include limit
## 8d8a9b0 Detected double include and loops
## 8a5a8f5 Report the location of the include loop
## 58f313c Merge branch 'sublime' into 'master'
## e0c1371 Clean up include once feature
## 84a37be Update bootstraps
## d824e98 Merge branch 'include-once'
## af3ebcc Remove stale TODO
## 556ee98 Reimplement cat example using let-bindings
## e741a5e Test the `not` intrinsic
## a1bab88 Clean up 2swap.porth test case
## 9de02e3 Add some thoughts regarding `print` intrinsic
## 3102967 Don't use TODO in here.porth example
## 51aa71a Elaborate on exploring the idea of using inline procs in consts
## fcacf92 Update the expected outputs of the test cases
## 57ba8a7 Make try-parse-int recognize empty strings as non-numbers
## e83dbe3 porth.py does not exist anymore
## 7db5bf6 Make streq exit earlier on strings with different sizes
## 9447dd7 Update bootstraps
## 2dac1fc Merge branch 'cleanups'
## eab1f36 Implement WIFSTOPPED and WIFCONTINUED
## 75b76aa Add printing signal of terminated child
## 4bd8733 Fix `segfault` test case
## 1fad9ee Add wrappers for SIGQUIT and kill to std.porth
## 7d6b4ae Add child-terminated test case
## 46066ca Update bootstraps
## 15118c0 Merge branch 'print-signal' into 'master'
## 578e6df [std.porth] Use let for some of the functions
## 279e520 [std.porth] rename char type functions
## a7d0239 Update bootstrap
## add0084 Merge branch 'more-let'
## 5bf5ed2 Mark some places where peek would be useful
## 432af48 Implement `peek` construction
## 7ffb09a Fix tests
## 32d2f82 Update bootstrap
## bc648a0 Merge branch 'peek'
## 3e20f2d Ignore vim garbage
## 7bffd50 Refactor cmd-echoed with let-bindings
## 188956f Introduce an ability to /dev/null stdout of cmd-echoed
## 1c146f2 Remove nasm
## 6e44e3c Update bootstrap
## b3948ca Fix bootstrap instructions
## 22e68c0 Merge branch 'remove-nasm'
## 23569a5 Use let-bindings in code generation
## e983807 Update Language Reference
## 5c04546 Add test case for str-starts-with
## dcb7604 Reimplement str-starts-with using bindings
## 9280534 Update bootstrap
## e1243f6 Merge branch 'str-starts-with'
## ea8a72c Implement str-chop-by-delim-2
## 33a6ba2 Use peek in more places
## 678bebe Rewrite rule110 using bindings
## f432e8d Rewrite checker example using bindings
## 96c81a3 Make gol example wrap around
## 41ee697 Put several gliders in the GoL example
## bae2b28 Rewrite seq example using let bindings
## 61f6ef8 Fixed intrinsic-name +ptr instead of +
## 415386d Added intrinsic name to asm comment
## 80d5880 Move op comment generation to a separate proc
## 01d6199 Update bootstrap
## 6e94828 Apply various fixes from @DemonInTheCloset
## ceba054 Fix quine example
## 631136b Add the website example
## a106f76 Update README
## b106c0e Capitalize the Elevetor Pitch
## c59141c Get rid of the `quit` variable in website example
## a8ee1b4 Simplify sublime-syntax file
## 32410a4 Add support for toggle comment hotkey in Sublime
## 2f35a4f Merge branch 'subl' into 'master'
## 5fad955 Forbid conditions, loops and local memories in inline procs
## 3bcf720 Update bootstrap
## 260f8c1 Merge branch 'forbiden-inline-constructions'
## e5305ce Implement memory size type error
## cc0717c Add test for wrong memory size type
## af2bab2 Remove usage of deleted flag
## aeb9f1a Implement normalization for POSIX paths
## b9fea88 Update bootstrap
## 4e2f69a Merge branch 'normpath'
## 8ae4ce5 Update bootstrap
## f40651e Revert "Update bootstrap"
## 061540a Merge branch 'mem-err' into 'master'
## eba51df Update bootstrap
## 5f4bf08 Implement reporting unsupported token type in proc definition
## 609e2cd Add test for proc definition token type error
## 3808b38 Add test for unfinished escape sequence
## 42ce65a Add test for unknown escape sequence
## 2e22f8a Add test for wrong token type after call-like keyword
## fa58650 Add test for calling non-existing procedure
## 1a3736b Add test for wrong token type after addr-of keyword
## 4afbbfb Add test for non-existing procedure name after addr-of keyword
## d7ab87c Add all test names to gitignore
## 32ec912 Fix hardcoded name of datatype in error report
## a098732 The time has come
## 7b7739b That's a funny bug
## 8e50206 Update bootstrap
## 49b9e98 Merge branch 'proc-def' into 'master'
## 849b518 Typo
## ea5eb0e Implement abspath
## af0e07b Remove already done TODO
## 482c6d6 Update bootstrap
## 17377dc Merge branch 'abspath'
## b57b569 Fix printing compiler binary in error report
## 3aa9edb Add test for `addr-of` keyword without proc name
## 2752c12 Add test for `call-like` keyword without proc name
## 3309efa Implement -I flag
## 252cd02 Update README
## 8a4e596 Update bootstrap
## 10b57b8 Merge branch 'include-paths'
## 6e9aaa3 Add newlines to the diagnostic messages
## 94dbefc Update bootstrap
## 4ff442d Revert "Update bootstrap"
## 8121cd0 Merge branch 'no-proc' into 'master'
## 50458a0 Update bootstrap
## 9dde05a Make try-parse-int parse negative numbers
## 676d1b2 Update bootstrap
## dfeb3cb Add test for negative numbers support in the compiler
## ceff5ff Use negative numbers in GoL example
## c419cbd Use negative numbers accross the compiler where appropriate
## 30f64ca Update bootstrap
## 724e5ab Merge branch 'negative-numbers'
## d55dc83 Update README
## 022100d Fix bug in abspath when the path is already absolute
## 35239c2 Add chroot related stuff to std.porth
## 18ef596 Normalize file paths before including them
## 1b6d380 Use absolute path to include file as unique id for "include once"
## da9ab80 Update bootstrap
## 3779e2d Merge branch 'include-once-abspath'
## 87e0622 Compilation logging change
## 1b2e527 Separate core.porth from std.porth
## e864187 Remove swap64
## b18ec56 Clarify the purpose of core.porth
## f273758 Separate linux.porth from std.porth
## 481a156 Clarify the purpose of std.porth
## b4b617a Update bootstrap
## 381f8ca Merge branch 'std-split'
## e444704 Remove stale TODO
## 22cd616 Implement simple "termios" layer for snake example
## d8125b2 Add score and controls help
## 694ccc2 Implement pause mode
## 10ca113 Print final score after death
## ec23d51 Update bootstrap
## ba9d5f0 Make the initial length of snake 3
## 847e24e Merge branch 'termios-for-snake'
## 4beda3a Update README
## 97868a7 [porth-mode.el] define comment-start
## 873186d Document some of the IR instructions
## e02f0d8 Update bootstrap
## d21186a Finish documenting IR
## 790de11 Update bootstrap
## b2e6bb3 Make the assembly file generation buffered
## 9392815 Update bootstrap
## 4d534b3 Rename BuffdFd to Bfd
## 7d59624 Move bfd implementation to std.porth
## 5309661 Update bootstrap
## 8fb9ffb Merge branch 'bfd-std'
## 371008c Separate OP_END into OP_END_IF and OP_END_WHILE
## 782b04e I think this is the official spelling of fasm
## 4c7f6fe Update bootstrap
## 9eda89a Merge branch 'separate-op-ends'
## 2cfc818 Fix IR instructions docs
## 45dc06e [README] Remove FASM section
## 073a323 Start rewriting compile-file-into-ops using let-bindings
## 7820566 Update bootstrap
## e2f29e1 Improve bootstrapping instructions
## a283207 Use let-bindings in compilation of KEYWORD_IFSTAR
## 1745e01 Use let-bindings in compilation of KEYWORD_ELSE
## 52cae25 Use let-bindings in compilation of KEYWORD_DO
## 2eb3d3d Use let-bindings in compilation of KEYWORD_END
## 5fa06ab Bind Token.type by reference
## 61d9608 Clean up the compilation of KEYWORD_INCLUDE
## 1aaf959 Remove local memory konst
## 5ef17c8 Remove local memory `memori`
## 9f1ec71 Completely get rid of the local memory from compile-file-into-ops
## 4fb051f Cleanup
## 5162461 Update bootstrap
## dfd0d1a Merge branch 'compile-file-into-ops-let'
## c745cd5 Get rid of enclose-else-if*
## 6cf8a15 Remove enclose-while-do
## 59a3e65 Remove bind-table-pop and enclose-let
## be5e174 Remove chain-else-if*
## 942ca4f Update bootstrap
## 35dedec Merge branch 'compile-file-into-ops-let'
## 7461881 Make OP_IF, OP_IFSTAR, OP_ELSE use relative jumps
## 9020fe6 Document forgotten operand of OP_WHILE
## e29ef5a Make OP_DO use relative jumps
## f82b8bc Make OP_END_WHILE use relative jumps
## b567d27 Make OP_WHILE use relative jumps
## 9bc6b31 Allow conditions in inline procs
## 19a1c06 Allow loops in inline procs
## 3893744 Update IR instructions documentation
## 6b5da2d Update bootstrap
## c329007 Enable conditions and loops in inline procs
## 0450fb7 Sorry
## 8c44522 Typo
## 6224559 Add instructions on how to access the Last Open Version
## c9866c8 Link the Porth Playlist
## c0b8db4 Typo
## dd40b82 Outline the development milestones
## d409555 Yooo! The code is open again! Kappa
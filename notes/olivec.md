# Olive.c 源码分析

## 8963246 Ready. Set. Go!
```c
#define return_defer(value) do { result = (value); goto defer; } while (0)

Errno olivec_save_to_ppm_file(uint32_t *pixels, size_t width, size_t height, const char *file_path)
{
    int result = 0;
    FILE *f = NULL;

    {
        f = fopen(file_path, "wb");
        if (f == NULL) return_defer(errno);

        fprintf(f, "P6\n%zu %zu 255\n", width, height);
        if (ferror(f)) return_defer(errno);
    }

defer:
    if (f) fclose(f);
    return result;
}
```
do { ... } while (0) 是一个do-while循环，用于创建一个代码块。这种写法的目的是确保宏在使用时像一个语句，而不是表达式。
result = (value); 是将传入的参数 value 赋值给一个名为 result 的变量。这个变量可能是在宏定义之前声明的。
goto defer; 是一个无条件跳转语句，将程序的执行流程转到标签 defer 所在的位置。

这个宏定义的目的是在函数中实现资源释放的延迟操作。通常，在函数的执行过程中，可能会分配一些资源（如内存、文件句柄等），需要在函数结束时进行释放。使用这个宏定义可以将资源的释放操作延迟到函数的最后，以保证在任何情况下都能正确释放资源。
> 这样做的很大一部分原因是原始c语言不支持gc和错误码。

## f4c95c6 Replace ppm with png
使用 nothing 库写入 png 格式图片
```c
stbi_write_png(file_path, WIDTH, HEIGHT, 4, pixels, WIDTH*sizeof(uint32_t))
```

## a26b886 Implement automatic testing
argc 是一个整数，表示命令行参数的数量（argument count）。它指示了在运行程序时传递给它的命令行参数的个数，包括程序本身的名称。至少会有一个参数，即程序的名称。

argv 是一个字符指针数组（argument vector），它存储了命令行参数的字符串。每个元素都是一个指向以 null 结尾的 C 字符串的指针。argv[0] 存储的是程序的名称，argv[1] 存储的是第一个命令行参数，依此类推。

## 0d83698 Add WebAssemply example
## 2472dd3 Inline olivec_sort_triangle_points_by_y
## ff877c0 Adapt the triangle example to SDL2
## 190fbd0 [examples/triangle] print error first in the defered section of SDL
## 98ee69b [test.c] save the actual image along with the diff
## 5c34714 Remove finished TODO
## dd0d49f Move boundary checks outside of the loops in rect and circle functions
## 51f17a9 Implement alpha blending
## a800e2a Implement Olivec_Canvas
## bfc33b9 [README] Update Quick Start Example
## d09b2f1 Make olive.c act like a header by default
## 1fbce86 Implement AA for circles
## 74a4003 Add 3d example
## 0399dc7 Outline more work
## 16c2896 Initial implementation of the text rendering
## d78015c Implement Terminal rendering
## f8b67f2 Increase the resolution for 3d.term
## 6f9bf35 Remove outdated TODO
## 175f6fb Scale up Term version of the 3d example
## a1277fe TODO: custom size for different tests
## 4456df2 TODO: brightness should take into account tranparency as well
## 82cb496 Fix the description of the 3d example
## 0090fb2 Move pixel parsing macros to olive.c
## acaa5b9 Remove redundant comments
## e682f8b Implement olivec_copy
## 95897ae TODO: deploy the WASM examples to GitHub pages
## 7427d5a Display all the WASM examples on a single page
## 30c1a2e brightness should take into account tranparency as well
## 34e74df Implement triangle interpolation based on Byricentric Coordinates
## f4451b2 Typo
## d1f64f0 Gitignore LaTeX garbage
## 0ebcc2d Ungitignore the pdf file
## 269b9ed Make the triangle example a bit brighter
## ea5775a Calm down the squish example
## fde3d6e Factor out vc.js
## 63c27f0 Prepare for GitHub pages deployment
## f31bfcf Replace gallery with a link to demos.
## e23ebfb Typo
## 0b3a345 Use Arena Allocator for tests
## 4448506 custom size for different tests
## 8a5bb54 Merge gallery into tests
## 57de392 Reduce memory usage by resetting the arena on each test case
## a949f23 Remove irrelevant info from README
## 62fc919 example -> demo
## ce18186 Remove deadcode from test.c
## c8629e0 Move olivec_triangle3() to the header
## 8aec8c5 Add TODO regarding overflows
## 4d0b185 Add test_hello_world_text_rendering
## af7fe5e Clean up Barycentric paper a bit
## 7c9b51f byricentric -> barycentric
## 87119b0 Typo
## 33d7378 Remove finished TODO
## 8fdec48 Clean up build.sh a bit
## 9265d05 Remove init from VC API
## cf6065d Remove unnecessary flag from WASM demos build
## e5485f5 Document the usage of VC
## 5571ace TODO: unhardcode the demos resolution
## 87080ea Unhardcode demo resolution for TERM_PLATFORM
## 20a4bdc Unhardcode demo resolution for SDL_PLATFORM
## 1123f1a Unhardcode demo resolution for WASM_PLATFORM
## 24e039a Git ignore vim garbage
## 5ff8b04 Update TODOs
## a94281f Make vc.c include olive.c for you
## 190d6dd Update wasm blobs
## 2721aaa TODO for if __heap_base not found
## 38918e4 Introduce 3D projection whitepaper
## bb2a95c Tweak 3D projection paper
## 8fe82d1 Fix division by zero in mix_colors3
## eb9a89e Add Triangle 3D demo
## 0afa4b0 Add disclaimer
## 232c0c2 Disable second 3D triangle
## dddf765 Typo
## 72ea85c TODO: explore the idea of figuring out aspect ratio of the character
## b082ab1 Add more details about 3D triangle demo
## 854d89c Typo
## 43a67dd Explain the name
## ded2782 TODO: custom pixel formats
## cc022f1 Update README
## 941d29a Fix the olivec_line stairs
## ad31464 TODO: make the output images of the example tests smaller
## 984013b Discard the idea of implementing thicc lines with triangles
## 1e6fe47 [test] Use canvas_alloc() everywhere
## ad65523 [test] Factor out canvas_load() and canvas_save()
## 00eeb24 [test] Generate image diff even on expected image size error
## a979da9 [test] reduce the size of test_checker_example()
## 6e788b0 [test] reduce the size of the circle example
## a6565bb [test] reduce the size of test_circle_example()
## 8fe4528 [test] reduce the size of test_lines_example()
## 9612d0b Update wasm binaries
## c490e7f [test] update output formatting
## f621fe6 [test] implement subcommand system
## 5fd83de [test] remove test_ prefix from the test ids
## a215463 [test] update error messages
## 3cd4efa [olive.c] handle some edge cases in olivec_line
## 1608f5a Update wasm binaries
## 28855d2 Update README
## 1a0a3aa Add "Tests" section to README
## 56eb15e TODO: olivec_frame()
## 67c291c Implement olivec_frame()
## 7f3fa85 [test] Make frame test less square
## 90558dd Fix align
## ddbd706 Update frame_expected.png
## bdf29a4 Enable memory sanitization for test utility
## 9e7ad38 Add more glyphs to the default font
## 5b9288f Make olivec_copy blend the colors properly
## 0a3d5e3 Handle out-of-bounds correctly in olivec_copy
## 2a6d196 Update wasm binaries
## 0cc39e8 TODO: olivec_copy() should flip the image
## 3d596bf Add missing OLIVECDEFs
## d352776 Make olivec_copy() flip the image when necessary
## 090dfa4 Update wasm binaries
## cf8132a Fix cut out of bounds bugs in olivec_copy()
## 4668dbe Fix olivec_normalize_rect() on zero rectangle
## 16588b8 Fix more corner cases in olivec_copy()
## 9d17776 TODO: fuzzer
## 0ce5ab0 Add olivec_copy() to the header
## 8576120 Make olivec_normalize_rect() preserve the original uncut range
## 46bdb2a Reorder arguments of olivec_copy so they make more sense
## cd0741c [png2c] customizable name
## 294ae6f Rename olivec_copy -> olivec_sprite_blend
## 2aeb288 Implement olivec_sprite_copy()
## 56aef62 Implement Depth Buffer
## 5c41e51 Remove implemented TODO
## aa5150e Fix README
## 723f8cb Add `i` and `k` to the default font
## b21d7ae Rotating textures
## 97b89d2 Textured 3D triangles
## a27b47d Remove TODO about enabling -Wconversion
## df37695 Tidy up build.sh
## 3dfa435 Remove finished TODO
## dfbae7a [build.sh] separate commands for building different kinds of demos
## dbb7bb4 [demos] remove redundant comments
## 8ae22c7 [README] fix quick example
## 8c994b4 Enable -pedantic for the whole codebase
## 7ee4ad0 Expand on TODO about pitch in bytes
## 2880566 Implement a more general triangle rendering API
## 51e501a Add viewobj
## decc5c3 Add sv.h to thirdparty
## 3651530 Rename thirdparty/ -> dev-deps/
## b52ca59 Simplify olivec_triangle() and olivec_triangle3c() implementations
## e64e3aa Add test for triangle order flip
## d29a66b Add weird_triangle_bug
## 5d5ac66 Add forgoten triangle_order_flip_expected.png
## 278036e Update wasm binaries
## 444d40e Fix barycentric overflow bug
## 55d3675 Build viewobj
## ee91cc0 Implement Cup 3D demo
## 622e8a2 Temporarily disable Cup 3D demo
## 964ccc8 [obj2c] print input/output file paths
## efcc213 Update wasm binaries
## fa43a2e TODO: do not remap any coordinates.
## 11ebee7 Introduce tools folder
## e7379a7 Remove Olivec_Tri triangle API
## cfcc2d0 Add alpha blending test for olivec_triangle3c()
## c594e05 barycentric -> olivec_barycentric
## c25ace9 Update README
## a6c32fe Make olivec_barycentric identify whether point is inside of triangle
## e3ed21b Remove Uv struct
## 84af89f Update wasm binaries
## bb86e29 Simplify implementation of olivec_triangle3uv
## fb94323 Update wasm binaries
## c8f6b31 Simplify implementation of olivec_triangle3z
## 7d4442f Update wasm binaries
## 33c5dfe Prefix all the names in olive.c with `olivec_`
## 2a31284 Update wasm binaries
## a9f2909 Prefix VC api elements with vc_*
## 658bb51 Enable parallel build back
## 6aa9890 TODO: we have too many triangle examples.
## 3be57ae Play the demos only on hover to preserve the resources
## 4fa1e1c Pause/unpause for SDL VC
## f519bbf Remove dead code
## 99049fd Replace Sadge.png with tsodinCup.png
## dfc1de8 Fix distortion of the Cup 3D demo
## 4e3c1a6 Update wasm binaries
## eb073ec Update the resolutions of the demos
## 99d6954 Remove finished TODO
## 9691f31 Add the teapot demo
## 49bfbfb Release source code of Utah Teapot demo
## 0253c0b 3d -> dots3d
## d36791a Remove viewobj tool
## 1fd31a8 Add some sort of logo
## 58ed07a Try to center the logo
## f845b81 Use the img tag for the logo
## e15873c Reduce the size of the logo
## 65a08f2 Try to make the logo float left
## 944578b Revert "Try to make the logo float left"
## 472a3b5 Link the logo to demos
## 81593ec Update logo
## 6bf054b Introduce nobuild build system
## 235b380 implement copying wasm blobs into ./wasm/ folder
## fa64712 Use ANSI terminal colors for term demos
## 63a7e9d Update wasm blobs
## 551984b Implement multi-process building for demos
## 70427c3 Remove finished TODO
## dca6210 [nobuild] Include build_wasm_demo() into async building process
## c1d006d Implement bilinear interpolation for rectangular sprites
## 1caba08 Port bilinear interpolation to triangle functions
## 9f5a6fe Update WASM binaries
## a3c1d8c Bring back old triangle3dTex background color
## d2443c2 Implement olivec_ellipse
## 9521f94 I think we have just the right amount right now
## 9d262ce [vc] remove dead code from term platform
## daa2bd1 [nobuild] pass arguments to the ./build/test command
## e4cd32e [nobuild] rebuilding all assets is fast enough for any use case
## 5078a91 [nobuild] rebuild tools is not a very frequent operation
## ec0cbd6 [wasm] update binaries
## 0764768 [olive.c] Remove finished TODO
## 7b08545 [olive.c] remove finished TODO
## 119e780 Simplify code in model3d demos
## 0b7f28a [wasm] update binaries
## 8368d2a Move CREDITS.txt to ./assets/
## 4f2d586 Link the author of the textures used in triangle3dTex demo
## faae104 Implement near/far clipping planes for model3d demos
## 6d640c8 Add more ideas on resizing canvas in VC_TERM_PLATFORM
## 5a2ece2 Reference Utah Teapot properly
## de398e0 Update wasm binaries
## ba7f8ac Remove dead code from VC_TERM_PLATFORM
## 95af28b Additional work for VC term
## a1cc0dc [nobuild] Add run subcommand for sdl and term demos
## baf72b6 Replace tsodingPog with the ethically sourced Lena image
## a04cdce Credit the Lena Image source
## 1b36b3e Fix copy paste
## faeaf00 Revert "Credit the Lena Image source"
## 274eb61 Revert "Replace tsodingPog with the ethically sourced Lena image"
## 9c70bdd Add usage message for nobuild
## e71315f Fix the line bug offset
## c0eb82c Introduce olivec_in_bounds()
# bmfdecomp
decompile/decompress bmf file to mof file.

# Usage
使用mof文件的编译程序即可“反编译”bmf文件为mof文件。

```
mofcomp  -Amendment:ms_409 -MOF:output.MOF input.bmf
```
上述命令是将mof文件分解为中性语言版本（language-neutral）的mof文件和特定语言版本（language-specific ）的mfl文件，其中mfl文件可以不指定，具体参考：https://docs.microsoft.com/en-us/windows/win32/wmisdk/mofcomp

参数说明：
- -Amendment:ms_409：指定编码格式，ms_409为American English编码。
- -MOF:output.MOF：指定输出文件名。
- input.bmf：指定输入文件名。


其实，mof“编译”为bmf的过程是个文件压缩和编码的过程，所以bmf文件仍可“看作”是mof文件，将其作为mofcomp拆分mof的输入，即可“反编译”bmf文件为mof文件。

mofcomp.exe位于C:\Windows\System32\wbem\目录下，可以直接在命令行中使用。

知乎：[如何将bmf文件“反编译”为mof文件](https://zhuanlan.zhihu.com/p/682857530)
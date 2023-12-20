# PS4System
A Collection of anything related to the Playstation 4 Operating System... Such as:
- Syscalls and their respective syscall number
- SCE Symbols (like for example: system functions)
- And more!


# Breakdown of the Files/Directories in this Repository
### [ps4_names.txt](/ps4_names.txt)
- Contains all symbols in an unfiltered and unsorted state. Basically all symbols in one file (very large!!! open it as **raw**).

### [sceSymbols(Sorted)/](/sceSymbols(Sorted)/):
- Contains a collection of text files, each representing every symbol starting with **sce**. These files are extracted from [ps4_names.txt](/ps4_names.txt) and contain only the lines of text related to the specific symbol in question, such as, for example, `sceVideo*`, `sceUsb*`, etc.


# Credits
This was mostly made possible thanks to the legend by the name of [zecoxao](https://github.com/zecoxao). Most of the data that you see in this repository came from his repository that you can find here: [zecoxao/sce_symbols](https://github.com/zecoxao/sce_symbols)

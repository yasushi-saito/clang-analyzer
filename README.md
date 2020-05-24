# Clang-analyzer

`clang-analyzer` is a simple Python script that invokes clang++'s static
analyzer with cross-translation unit support. It runs the steps described in the
following web page:

https://clang.llvm.org/docs/analyzer/user-docs/CrossTranslationUnit.html

## Usage


    clang-analyzer [-p <compile_command.json_dir>] [--exclude=re] [c++ files...]

You must create a `compile_commands.json` file that lists the source files and
its compile flags.

 - The `-p` flag sets the directory that contains the
   `compile_commands.json` file. It defaults to '.'.

 - All the c++ files in the commandline must appear in `compile_commands.json`.

 - The `--exclude` flag sets the regexp patterns to exclude c++ files.

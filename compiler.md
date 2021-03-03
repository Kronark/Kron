## KRON COMPILER STRUCTURE

> File(s) containing Kron code with the file extension ".kr"
*
*
*
> Bundler that combines all files to one Kron file based on the contained "import" and "export" statements. Only necessary functionality is added to the combined file for optimal memory usage and speed.
>> ERROR: import can not find referenced gear / file
>
>> ERROR: import can not find referenced functionality in gear / file
>
>> ERROR: functionality of referenced gear / file is not public
*
*
*
> Corrector that removes all comments, spaces and tabs, then replaces every linebreak with a semicolon (except in special cases like loops or conditionals that don't need a semicolon).
>> ERROR: some token expected
*
*
*
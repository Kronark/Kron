## **COMMENTS**:

Preceeded by symbol `#` followed by content in simple text form. 
Everything after the `#` symbol is considered part of the comment, which means comments can start after code or take up an entire line themselves.
``` kron
    # This is a comment!
```




## **VARIABLES**:

Follows the form `TYPE NAME = VALUE`.
`TYPE` can only be either an integer with a specified bit count or a defined custom type given an import if necessary.
`NAME` can only include alphanumeric characters and underscores, whereby it can not start with a number.
`VALUE` can only be of the format as specified in the corresponding constructor of the given `TYPE`. Variables of type integer are defined using a simple integer with or without a minus symbol in front.
``` kron
    int4 age = 22

    int64 money = -20560

    int count = 560700              # custom integer type

    dat birthday = 01.01.2000       # custom date type

    col title_colour = red          # custom colour type
```




## **DATATYPES**:

Kron only provides the bare minimum of built-in datatypes. Everything else is built using Kron's dynamically oriented core syntax. Established and programmatically expected functionality will eventually be added to Kron's core package which does not require import statements for usage.

### ***Integers***:

The only single valued core datatype. The built-in integer value can be either positive or negative and directly maps to the LLVM integer type. 
The bit amount used for storage has to be specified. If it is not specified, the custom integer type from a gear will be used, which handles needed storage space definition automatically. 
Since every form of data used in computers can be represented by a number, this is all that is needed for Kron's dynamically oriented syntax.
The definition of core integers can be seen in the previous section.

### ***Vectors***:

Vectors are simple aggregate datatypes that allow fast simultaneous calculations on multiple instances of the same internal datatype.
Their size is fixed and defined in the datatype specification similar to that of integers.
They directly map to the fixed size version of the LLVM vector type.
``` kron
    vec3 colour = <255, 255, 255>

    vec10 numbers = <1, 2, 3, 4, 5, 6, 7, 8, 9, 10>
```




## **IMPORTS**:

Imports are used to make exported functionality of another Kron file available within a given file.
The "import" keyword is followed by an absolute or relative filepath or a URL to the Kron Gear registry on kronark.net. Registry URLs neither have to contain the full kronark url nor the protocol at the prefix.
Whether a file or a gear is meant is specified by whether or not a fileextension is used.
Gears are downloaded automatically on the first call of the import statement. Further calls will ignore the specific import.
Once an import statement is performed, all exported functionality of the file or gear is available in the given file.
``` kron
    import "../utils/example.kr"

    import "example.kr"

    import "https://kronark.net/kron/gear/exampleIdentifier"

    import "kronark.net/kron/gear/exampleIdentifier"

    import "exampleIdentifier"
```
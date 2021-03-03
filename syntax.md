## **COMMENTS**:

Preceeded by symbol `#` followed by content in simple text form. 
Everything after the `#` symbol is considered part of the comment, which means comments can start after code or take up an entire line themselves.

``` kron
    # This is a comment!
```




## **VARIABLES**:

Follows the form `TYPE NAME = VALUE`.
`TYPE` can only be a built-in type such as an integer, a vector, an array or a defined custom type given an import if necessary.
`NAME` can only include alphanumeric characters and underscores, whereby it can not start with a number.
`VALUE` can only be of the format as specified in the corresponding constructor of the given `TYPE`. Variables of type integer are defined using a simple integer with or without a minus symbol in front.

``` kron
    integer age = 22

    integer money = -20560

    float pvalue = 0.0000025

    vector basis = (1, 0, 0)

    list numbers = [427, 0.99]

    decimal alpha = 0.75                # custom decimal type

    date birthday = 01.01.2000          # custom date type

    colour title_colour = red           # custom colour type

    text name = "Waldo"                 # custom text type
```




## **DATATYPES**:

Kron only provides the bare minimum of built-in datatypes. Everything else is built using Kron's dynamically oriented core syntax. Established and programmatically expected functionality will eventually be added to Kron's core package which does not require import statements for usage.

### ***Integers***:

The only primitive single valued core datatype. The integer value can either be positive or negative and directly maps to the LLVM integer type. 
The bit amount used for storage is determined internally based on the value. 
Since every form of data used in computers can be represented by an arrangement of numbers, this is all that is needed for Kron's dynamically oriented syntax.

### ***Floats***:

The only derived single valued core datatype, as it technically consists of two integers behind the scenes. The float value can either be positive or negative and directly maps to the LLVM float type. The fractional part is separated from the integer part by a `.` period.
The bit amount used for storage is determined internally based on the value. 

### ***Vectors***:

Vectors are simple aggregate-like datatypes that allow fast simultaneous calculations on multiple instances of the same datatype. Their value can be any amount of the same integer or float datatype separated by commas `,` and enclosed by round brackets `(...)`.
Their size is variable and can be expanded with the same function calls used for modifying arrays and structures.
They directly map to the variable sized version of the LLVM vector type.

### ***Lists***:

TODO: maybe just strcuture LLVM type instead

Lists are aggregate datatypes that can contain any datatype and store the data sequentially in memory. Their value can be any amount of any datatype separated by commas `,` and enclosed by square brackets `[...]`. Multiple dimensional arrays are possible by nesting brackets. 
Their size is variable and can be expanded with the same function calls used for modifying vectors and structures. Internally, the variability is handled by creating a new list if the initial list has no space left and copying the initial list contents to the new list.
They map to the LLVM array type and are based on python's lists or java's ArrayList objects.

### ***Structures***:

Structures are aggregate datatypes that can contain any datatype and store the data sequentially in memory. 




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
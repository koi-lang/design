# Koi Library Reference
The library reference for the Koi language.

Methods not marked as overridable can't be overrided.

## Core
### Functions
- `int` - Converts type to an integer
- `str` - Converts type to a string
- `cha` - Converts type to a char
- `flo` - Converts type to a float
- `boo` - Converts type to a bool
### Types
#### Value
A value is an object that contains its' own value.

**Extends From:** Object
#### Reference
A reference is an object that contains a reference to a value.

**Extends From:** Object
#### Object
The object is default type of any class. Every class extends from Object.

**Extends From:** Nothing

**Methods:**
- `to{core type}` - Converts the type to the given core type (overridable)
- `as{core type}` - Returns the type as the given core type
#### Boolean
A boolean object is either true or false, and is returned from comparison operations.

**Extends From:** Value

**Methods:**
- `flip` - Changes the boolean to the opposite value (true -> false, false -> true)
#### Character
A character is a string-like object that contains a singular character.

**Extends From:** Value
#### Integer
An integer is a full numeric value.

**Extends From:** Value
#### String
A string is an array of characters.

**Extends From:** Reference
#### Array
An array is a multitude of values.

## Standard
### Sandbox
### Console
**Functions:**
- `print` - Prints given data.
    - Parameters:
        - `args` - Object: The objects to print.
    - Returns: None
- `println` - Prints given data and a newline.
    - Parameters:
        - `args` - Object: The objects to print.
    - Returns: None
- `input` - Accepts user input.
    - Parameters:
        - `limit` - Integer: The limit of characters accepted by the input.
    - Returns: String
- `inputln` - Accepts user input and adds a newline.
    - Parameters:
        - `limit` - Integer: The limit of characters accepted by the input.
    - Returns: String
- `clear` - Clears the terminal.
### Math
**Functions:**
- `ceili`
    - Description: Finds the ceiling of a given number.
    - Parameters:
        - `number` - Integer: The number to use.
    - Returns: Float
- `floor`
    - Description: Finds the floor of a given number.
    - Parameters:
        - `number` - Integer: The number to use.
    - Returns: Float
- `round`
    - Description: Rounds the given number.
    - Parameters:
        - `number` - Float: The number to use.
    - Returns: Integer
- `abs`
    - Description: Finds the absolute value of a given number.
    - Parameters:
        - `number` - Float: The number to use.
    - Returns: Float
- `sin`
    - Description: Finds the sine of a given number.
    - Parameters:
        - `number` - Float: The number to use.
    - Returns: Float
- `cos`
    - Description: Finds the cosine of a given number.
    - Parameters:
        - `number` - Float: The number to use.
    - Returns: Float
- `exp`
    - Description: Finds the exponential of a given number.
    - Parameters:
        - `number` - Float: The number to use.
    - Returns: Float
- `log`
    - Description: Finds the logarithm of a given number.
    - Parameters:
        - `number` - Float: The number to use.
    - Returns: Float
- `sqr`
    - Description: Finds the square of a given number.
    - Parameters:
        - `number` - Float: The number to use.
    - Returns: Float
- `cube`
    - Description: Finds the cube of a given number.
    - Parameters:
        - `number` - Float: The number to use.
    - Returns: Float
- `sqrt`
    - Description: Finds the square root of a given number.
    - Parameters:
        - `number` - Float: The number to use.
    - Returns: Float
- `odd`
    - Description: Checks if the given number is odd.
    - Parameters:
        - `number` - Integer: The number to use.
    - Returns: Boolean
- `even`
    - Description: Checks if the given number is even.
    - Parameters:
        - `number` - Integer: The number to use.
    - Returns: Boolean
### Mathcro
An extension to the math library that adds useful macros.
- Power Of
    - Description: Works out the power of the given value.
    - Syntax: `{ID/numeric}^{numeric}`
    - Returns: Float
- Coefficient
    - Descriptions: Finds the given value multiplied by the given number.
    - Syntax: `{numeric}{ID}`
    - Returns: Float
### JSON
### YAML
### XML
### Random
### OS
### IO
### Regex
### Date
**Functions:**
- `current_date`
    - Parameters:
        - `format` - String: The format to use.
    - Returns: String
### Time
**Functions:**
- `current_time`
    - Parameters:
        - `format` - String: The format to use.
    - Returns: String
### Zip
### GZip
### Base32
### Base64
### Binary
### Hexadecimal
### i18n
### UUID
### SQL
### Image
### Sound
### Logging
**Functions:**
- `log`
    - Parameters:
        - `content` - String: The content to log.
        - `type` - String: The kind of log this is.
- `info`
    - Parameters:
        - `content` - String: The content to log.
- `warn`
    - Parameters:
        - `content` - String: The content to log.
- `debug`
    - Parameters:
        - `content` - String: The content to log.
### Event
**Classes:**
- `EventCreator`
- `EventListener`
### Build
### Threading
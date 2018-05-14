# Koi Library Reference
The library reference for the Koi language.

Methods not marked as overridable can't be overrided.

## Core
### Functions
- `print` - Prints given data
- `println` - Prints given data and a newline
- `input` - Accepts user input
- `inputln` - Accepts user input and adds a newline
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
### Math
### JSON
### YAML
### XML
### Random
### OS
### IO
### Regex
### Date
**Functions:**
- `currentDate`
    - Parameters:
        - `format` - String: The format to use.
    - Returns: The current date.
### Time
**Functions:**
- `currentTime`
    - Parameters:
        - `format` - String: The format to use.
    - Returns: The current time.
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
**Classes:**
- `Logger`
    - Methods:
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
### Event
**Classes:**
- `EventCreator`
- `EventListener`
### Build
### Threading
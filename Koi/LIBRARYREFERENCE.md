# Koi
The library reference for the Koi language.

Methods not marked as overridable can't be overrided.

## Core
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

### IO

**Extends From:** Reference

## Standard
### Math
### JSON
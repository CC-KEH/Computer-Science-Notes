**Strings are immutable in Java. This means that once a string is created, it cannot be changed. This is important to keep in mind when solving string problems, as it means that you will need to create new strings if you want to make any changes.**

## Important Functions

#### 1. `indexOf()`
Returns the index of the first occurrence of the specified character or substring.

#### 2. `replace()`
Replaces all occurrences of a character or substring with another character or substring.

#### 3. `split()`
Splits the string into an array of strings based on a delimiter.

#### 4. `trim()`
Removes leading and trailing whitespace from the string.

#### 5. `hashCode()`
Returns the hash code of the string.

#### 6. `indexOf()`
Returns the index of the first occurrence of the specified character or substring.

#### 7. `strip()`
Removes leading and trailing whitespace from the string.
( is "Unicode-aware" evolution of `trim()`. Meaning `trim()` removes only characters <= U+0020 (space) `strip()` removes all Unicode whitespace characters (but not all control characters like \0)

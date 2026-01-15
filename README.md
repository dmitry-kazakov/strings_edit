The package Strings_Edit provides I/O facilities. The following I/O items are supported by the package:

- Generic axis scales support;
- Integer numbers (generic, package Integer_Edit);
- Integer sub- and superscript numbers;
- ISO 8601 representations of time and duration;
- Floating-point numbers (generic, package Float_Edit);
- Roman numbers (the type Roman);
- Strings;
- Ada-style quoted strings;
- Base64 encoding;
- Object identifiers and distinguished names;
- RFC 8439 (ChaCha20 cipher, Poly1305 digest, AEAD);
- UTF-8 encoded strings and conversions to older encoding standards;
- Unicode maps and sets;
- Wildcard pattern matching.
- 
The major differences to the standard Image/Value attributes and Text_IO procedures are:

- For numeric types, the base is neither written nor read. For instance, output of 23 as hexadecimal gives 17, not 16#17#.
- Get procedures do not skip blank characters around input tokens, except the cases when the blank characters are required by the syntax.
- Get procedures use the current string position pointer, so that they can be consequently called advancing the pointer as the tokes are recognized.
- Numeric get procedures allow to specify the expected value range. When the actual value is out of the range then depending on procedure parameters, either Constraint_Error is propagated or the value is forced to the nearest range boundary.
- Put procedures also use the current string position pointer, which allows to call them consequently.
- The format used for floating-number output is based on the number precision, instead of rather typographic approach of Text_IO. The precision can be specified either as the number of valid digits of the current base (i.e. relative) or as the position of the last valid digit (i.e. absolute). For instance, 12.345678 with relative precision 3 gives 12.3. With absolute precision -3, it gives 12.346.

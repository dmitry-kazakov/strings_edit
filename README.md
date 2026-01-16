<H2>Strings Edit</H2>

<p>The package Strings_Edit provides I/O facilities. The following I/O items are supported by the package:</p>
<ul>
<li>Generic axis scales support;</li>
<li>Integer numbers (generic, package Integer_Edit);</li>
<li>Integer sub- and superscript numbers;</li>
<li>ISO 8601 representations of time and duration;</li>
<li>Floating-point numbers (generic, package Float_Edit);</li>
<li>Roman numbers (the type Roman);</li>
<li>Strings;</li>
<li>Ada-style quoted strings;</li>
<li>Base64 encoding;</li>
<li>Object identifiers and distinguished names;</li>
<li>RFC 8439 (ChaCha20 cipher, Poly1305 digest, AEAD);</li>
<li>UTF-8 encoded strings and conversions to older encoding standards;</li>
<li>Unicode maps and sets;</li>
<li>Wildcard pattern matching.</li>
</ul>  
<p>The major differences to the standard Image/Value attributes and Text_IO procedures are:</p>
<ul>
<li>For numeric types, the base is neither written nor read. For instance, output of 23 as hexadecimal gives 17, not 16#17#.</li>
<li>Get procedures do not skip blank characters around input tokens, except the cases when the blank characters are required by the syntax.</li>
<li>Get procedures use the current string position pointer, so that they can be consequently called advancing the pointer as the tokes are recognized.</li>
<li>Numeric get procedures allow to specify the expected value range. When the actual value is out of the range then depending on procedure parameters, either Constraint_Error is propagated or the value is forced to the nearest range boundary.</li>
<li>Put procedures also use the current string position pointer, which allows to call them consequently.</li>
<li>The format used for floating-number output is based on the number precision, instead of rather typographic approach of Text_IO. The precision can be specified either as the number of valid digits of the current base (i.e. relative) or as the position of the last valid digit (i.e. absolute). For instance, 12.345678 with relative precision 3 gives 12.3. With absolute precision -3, it gives 12.346.</li>
</ul>

Home page: https://www.dmitry-kazakov.de/ada/strings_edit.htm

Changes log: https://www.dmitry-kazakov.de/ada/strings_edit.htm#changes_log

# Text Representation: ASCII and Unicode

## ASCII

**American Standard Code for Information Interchange (ASCII)** was originally a 7-bit code. Extended ASCII is an **8-bit code** (1 byte) for storing text, providing **256 codes or characters**. It encodes the English alphabet, numbers, and some symbols.

Examples:

- `A` = `0100 0001` (code `65`)
- `a` = `0110 0001` (code `97`)
  - Lowercase letters are assigned a code that is the uppercase code + 32.
- `1` = `0011 0001` (code `49`)
- blank space = `0010 0000` (code `32`)

See: [ASCII Code](https://www.ascii-code.com/)

<!-- Add image from original H5P: Sample ASCII values / ASCII table -->

---

## Unicode

**Unicode extends ASCII** to represent characters in many (most) languages using **one to four bytes**.

- The **first 128 characters are the same as ASCII**.
- Version 17.0 of the Unicode Standard (September 2025) defines **159,801 characters**.

Examples:

- `A` = `41` hex = `65` decimal = `0100 0001` binary
- Grinning face &#x1F600; = `U+1F600` = `1F600` hex = `128,512` decimal = `0001 1111 0110 0000 0000` binary

Resources:

- [Unicode](https://home.unicode.org/)
- [Unicode Emoticons Chart](https://www.unicode.org/charts/PDF/U1F600.pdf)

<!-- Add image from original H5P: Unicode emoticons -->

### Emoji Appearance

Unicode defines the **meaning** of an emoji, but **each platform designs its own appearance**. As a result, an emoji may look and feel different depending on where it is displayed.

In Word, type a Unicode hex value e.g. '1F601` and then press `alt` and `x`.  You shoud now see the Unicode character &#x1F601;

---

## ASCII Text to Binary

There are many free online text-to-binary converters. The RapidTables website has a converter that works well.

[RapidTables: ASCII Text to Binary](https://www.rapidtables.com/convert/number/ascii-to-binary.html)

Example text:

`A1 a2`

Example binary output:

`01000001 00110001 00100000 01100001 00110010`

<!-- Add image from original H5P: RapidTables ASCII to binary -->

---

## Binary to ASCII Text

[RapidTables: Binary to ASCII](https://www.rapidtables.com/convert/number/binary-to-ascii.html)

Example binary input:

`01000001`

Example ASCII output:

`A`

<!-- Add image from original H5P: RapidTables binary to text -->

---

## ASCII Text to Binary, Decimal, and Hexadecimal

RapidTables also provides a converter that displays text as **binary, decimal, and hexadecimal** at the same time.

[RapidTables: ASCII, Hex, Binary, Decimal Converter](https://www.rapidtables.com/convert/number/ascii-hex-bin-dec-converter.html)

<!-- Add image from original H5P: text to binary, decimal, and hex converter -->

---

## Review Questions

1. The ASCII code for uppercase `A` is 65 decimal. What is the ASCII code for uppercase `B`?
   - 66
   - 11
   - 98
   - 2

2. The ASCII code for numeral `1` is 49 decimal. What is the ASCII code for numeral `0`?
   - 48
   - 0
   - ZERO
   - `0000 0000`

3. The ASCII code for uppercase `F` is 70. What is the ASCII code for lowercase `f`?
   - 102
   - 71
   - 38
   - 15

4. The ASCII code for a space is __________ decimal.
   - 32
   - 0
   - 1
   - 64

5. __________ was developed to encode the characters for all languages rather than being limited to 256 symbols.
   - Unicode
   - Megacode
   - ASCII code
   - EBCDIC

6. Unicode stores each of the 159,801 characters in:
   - one to four bytes
   - exactly two byte
   - exactly four bytes
   - two to eight bytes

-- end --
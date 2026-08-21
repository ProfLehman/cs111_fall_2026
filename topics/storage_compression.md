# Data Representation and Compression

## Analog Information

**Analog data is continuous** and can take **unlimited values within a given range**.

Examples include:

- **Vinyl Records** — The grooves on a vinyl record represent continuous sound waves, which are an analog form of audio data.
- **Mercury Thermometer** — The height of the mercury column continuously varies with temperature, providing an analog representation of the temperature.
- **Analog Clocks** — The movement of the clock's hands provides a continuous representation of time.
- **Film Photography** — The varying levels of light exposure on the film create a continuous range of colors and shades.
- **Radio Waves** — Continuous electromagnetic waves used for broadcasting audio signals.

It is impossible to create a perfect copy of analog data.

<!-- Add image from original H5P: analog devices -->

---

## Digital Information

**Digital data is discrete** and consists of **distinct, separate values**, such as binary digits.

Digital information allows for **perfect copying**, because digital copies are identical to the original.

Examples include:

- **CDs and DVDs** — Store audio and video data as discrete binary (0s and 1s) signals.
- **Digital Thermometer** — Displays temperature as discrete numbers on a digital screen.
- **Digital Clocks** — Shows time as discrete numbers (for example, 10:30).
- **Digital Photography** — Images are stored as pixels with discrete RGB values.

**Digitize** — the act of breaking information down into discrete pieces. All information that is stored on a computer must be represented in a digital format.

<!-- Add image from original H5P: digital devices -->

---

## Bits and Bytes

A **bit**, short for **binary digit**, is a `1` or `0`.

There are **eight bits in one byte** of data. Bytes are the smallest reported data storage within a computer.

`1 byte = 8 bits`

Examples range from:

`0000 0000` to `1111 1111`

---

## Bit Combinations

All **computers have limits for storage** based on the number of bits.

The **range of numbers** (distinct patterns) that can be stored given a specific number of bits is:

`2^(Number of Bits)`

With **three bits**, there are:

`2^3 = 8 patterns`

`000, 001, 010, 011, 100, 101, 110, 111`

With **eight bits**, there are:

`2^8 = 256 patterns`

The original H5P gives the range as:

`0000 0000` to `1111 11111`

### Excel Limits

[Microsoft Excel 2013 Maximum Number of Rows and Columns](http://proflehman.com/2015/09/12/microsoft-excel-2013-maximum-number-of-rows-and-columns/)

**Question:** How many rows and columns are available in Excel?

---

## Measurement Terms

Measurement terms are often used to describe a number of **bytes or bits**.

| Base 10 Prefix | Bytes | Base 2 Prefix | Bytes |
|---|---:|---|---:|
| K Kilo | 1,000 | KiBi | 1,024 |
| M Mega | 1,000,000 | MiBi | 1,048,576 |
| G Giga | 1,000,000,000 | GiBi | 1,073,741,824 |
| T Tera | 1,000,000,000,000 | TiBi | 1,099,511,627,776 |
| P Peta | 1,000,000,000,000,000 | PiBi | 1,125,899,906,842,620 |

**Uppercase `B` usually denotes Bytes**, while **lowercase `b` usually denotes bits**. There are 8 bits in a byte.

Examples:

1. A network card may operate at **100 Mbps**, thus 100 megabits per second.
2. A **2 TB** hard drive has 2 terabytes of memory.

> For this course, you only need to know the approximations for each term.

---

## Data Compression

**Data compression** is the process of **reducing the size of data files** by **encoding information more efficiently**, allowing for **faster transmission** and **more effcient storage** (that is, cheaper) while **preserving essential content**.

Compression techniques are either **lossy** or **lossless**.

---

## Lossless Compression

- **Definition:** Reduces file size without losing any data; original data can be perfectly reconstructed.
- **Techniques:** Huffman Coding, Lempel-Ziv-Welch (LZW), Run-Length Encoding (RLE).
- **Use Cases:** Text files, software programs, databases (where data integrity is crucial).
- **Pros:** No loss in quality; exact original can be restored.
- **Cons:** Lower compression, larger file sizes.

---

## Lossy Compression

- **Definition:** Reduces file size by permanently eliminating some data, especially redundant or less important information.
- **Techniques:** JPEG (for images), MP3 (for audio), MPEG (for video).
- **Use Cases:** Multimedia files (images, audio, video) where some quality loss is acceptable for reduced size.
- **Pros:** Higher compression rates; significantly smaller files.
- **Cons:** Some loss of quality; original cannot be fully restored.

[Additional Information: Difference Between Lossy Compression and Lossless Compression](https://www.geeksforgeeks.org/difference-between-lossy-compression-and-lossless-compression/)

---

## Optional: Huffman Compression

**Huffman Compression** is a **lossless data compression algorithm** that assigns shorter binary codes to more frequently occurring data elements, thereby reducing the overall size of the encoded data.

It is used in **data compression applications** such as file formats (for example, **ZIP archives**), image formats (such as **JPEG**), and multimedia codecs (such as **MP3**) to efficiently reduce file sizes while preserving data integrity.

General process:

1. Frequency Analysis
2. Assign codes
3. Write codes under letters
4. Count bits used
5. Compare to ASCII

[Obituary for David A. Huffman](https://www1.ucsc.edu/currents/99-00/10-11/huffman.html)

<!-- Add image from original H5P: Huffman table -->

### Huffman Compression Example — `gala apple`

**Step #1 — Letter frequency and assign codes**

| Code | Letter | Frequency |
|---|---|---:|
| `000` | a | 3 |
| `001` | l | 2 |
| `010` | p | 2 |
| `011` | g | 1 |
| `1000` | space | 1 |
| `1001` | e | 1 |

**Step #2 — Text in Huffman Code**

```text
g   a   l   a    space    a   p   p   l   e
011 000 001 000   1000   000 010 010 001 1001
```

**Step #3 — Huffman Bits**

Count the bits below the text:

`32 bits`

**Step #4 — ASCII Bits**

`"gala apple"` = 10 total letters/spaces × 8 bits each = `80 bits` for ASCII.

**Step #5 — Compression Ratio**

`32 / 80 = .4`

> Huffman coding is optional for CC-01.

=====
Pragmatic Unicode - or - How do I stop the pain?
=====

- Entire presentation made with unicode
- 256 symbols is not enough for the world to communicate using text
- Started with encodings for 1-byte, then 2-byte
- Now we are using unicode
  - Assigns characters to code points (integers)
  - 1.1M code points
  - 110K assigned
- Pile of poo character was covered
- Python can address characters by their unicode name
- str stores bytes
- unicode stores 'code points'
- Unicode encode method turns code points into bytes
- str decode turns bytes into code points
- Encode and decode can't always work (if ordinal is out of range)
  - Error handling: my_unicode.encode("ascii", "replace")
    Or xml/html character replace

- Python implicitly converts your 'assumed' ascii data when concatenating

There are two things: Bytes and Unicode
You have to know what you're dealing with

- str in python 2 is a byte string, str in python 3 is a unicode string
- Python 3 will never implicitly convert bytes into unicode

Mixing bytes and unicode is always **PAIN**
You are forced to keep them straight in Python 3

In python 3, th data you get back from a read operation depends on how you open it (r vs rb)

locale.getpreferredencoding() will get the default for read

stdin and stdout are pre-opened filed and must be handled or wrapped

"There is no string"

Fact of life: Sometimes you are told the wrong encoding. It sucks.

I/O is always bytes.

Test!

http://bit.ly/unipain

---
title: into bits
categories: |
  conversions
version: 0.83.0
conversions: |
  Convert value to a binary primitive.
usage: |
  Convert value to a binary primitive.
---

# <code>{{ $frontmatter.title }}</code> for conversions

<div class='command-title'>{{ $frontmatter.conversions }}</div>

## Signature

```> into bits ...rest```

## Parameters

 -  `...rest`: for a data structure input, convert data at the given cell paths

## Examples

convert a binary value into a string, padded to 8 places with 0s
```shell
> 01b | into bits
00000001
```

convert an int into a string, padded to 8 places with 0s
```shell
> 1 | into bits
00000001
```

convert a filesize value into a string, padded to 8 places with 0s
```shell
> 1b | into bits
00000001
```

convert a duration value into a string, padded to 8 places with 0s
```shell
> 1ns | into bits
00000001
```

convert a boolean value into a string, padded to 8 places with 0s
```shell
> true | into bits
00000001
```

convert a datetime value into a string, padded to 8 places with 0s
```shell
> 2023-04-17T01:02:03 | into bits
01001101 01101111 01101110 00100000 01000001 01110000 01110010 00100000 00110001 00110111 00100000 00110000 00110001 00111010 00110000 00110010 00111010 00110000 00110011 00100000 00110010 00110000 00110010 00110011
```

convert a string into a raw binary string, padded with 0s to 8 places
```shell
> 'nushell.sh' | into bits
01101110 01110101 01110011 01101000 01100101 01101100 01101100 00101110 01110011 01101000
```

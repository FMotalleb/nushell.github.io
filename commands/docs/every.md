---
title: every
categories: |
  filters
version: 0.87.0
filters: |
  Show (or skip) every n-th row, starting from the first one.
usage: |
  Show (or skip) every n-th row, starting from the first one.
---
<!-- This file is automatically generated. Please edit the command in https://github.com/nushell/nushell instead. -->

# <code>{{ $frontmatter.title }}</code> for filters

<div class='command-title'>{{ $frontmatter.filters }}</div>

## Signature

```> every {flags} (stride)```

## Flags

 -  `--skip, -s`: skip the rows that would be returned, instead of selecting them

## Parameters

 -  `stride`: how many rows to skip between (and including) each row returned


## Input/output types:

| input     | output    |
| --------- | --------- |
| list\<any\> | list\<any\> |

## Examples

Get every second row
```nu
> [1 2 3 4 5] | every 2
╭───┬───╮
│ 0 │ 1 │
│ 1 │ 3 │
│ 2 │ 5 │
╰───┴───╯

```

Skip every second row
```nu
> [1 2 3 4 5] | every 2 --skip
╭───┬───╮
│ 0 │ 2 │
│ 1 │ 4 │
╰───┴───╯

```

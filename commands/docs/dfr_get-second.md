---
title: dfr get-second
categories: |
  dataframe
version: 0.87.0
dataframe: |
  Gets second from date.
usage: |
  Gets second from date.
---
<!-- This file is automatically generated. Please edit the command in https://github.com/nushell/nushell instead. -->

# <code>{{ $frontmatter.title }}</code> for dataframe

<div class='command-title'>{{ $frontmatter.dataframe }}</div>

## Signature

```> dfr get-second {flags} ```


## Input/output types:

| input | output |
| ----- | ------ |
| any   | any    |

## Examples

Returns second from a date
```nu
> let dt = ('2020-08-04T16:39:18+00:00' | into datetime --timezone 'UTC');
    let df = ([$dt $dt] | dfr into-df);
    $df | dfr get-second
╭───┬────╮
│ # │ 0  │
├───┼────┤
│ 0 │ 18 │
│ 1 │ 18 │
╰───┴────╯

```


**Tips:** Dataframe commands were not shipped in the official binaries by default, you have to build it with `--features=dataframe` flag
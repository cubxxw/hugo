---
title: images.Sepia
description: Returns an image filter that produces a sepia-toned version of an image.
categories: []
keywords: []
params:
  functions_and_methods:
    aliases: []
    returnType: images.filter
    signatures: [images.Sepia PERCENTAGE]
---

The percentage must be in the range [0, 100] where 0 has no effect.

## Usage

Create the filter:

```go-html-template
{{ $filter := images.Sepia 75 }}
```

{{% include "/_common/functions/images/apply-image-filter.md" %}}

## Example

{{< img
  src="images/examples/zion-national-park.jpg"
  alt="Zion National Park"
  filter="Sepia"
  filterArgs="75"
  example=true
>}}

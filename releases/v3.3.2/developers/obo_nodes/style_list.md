---
title: textGroup > textItem > styleableText > styleList
menus: chunks
class: content_block
---

A series of one or more styles to apply to a block of text

## Properties

| Property | Required | Type | Description |
|-
| type | Required | String | Represents what type of styling to apply, must be one of the following:
| start | Required | Integer | The index of the first character to style
| end | Required | Integer | The index of the last character to style - all characters between `start` and `end` will be styled by `type`
| data | Required\* | Object | Only required for `a` and `sup` types. The expected value of this property is different depending on the value of `type`.

### Supported Values for `type`

A **StyleList** is an array of one or more **StyleListItem** objects containing four properties: **type**, **start**, **end** and **data**

| Type | Description |
|-
| b | Bold
| i | Italics
| del | Strikethrough
| a | Link
| q | Quote
| sup | Superscript / Subscript
| monospace | Monospace
| \_latex | Renders the range of text as inline LaTeX math using Katex

### Supported Values for `data`

| Type | Description |
|-
| a | Expects an object with an `href` property set to a String of the URL to link to.
| sup | Expects an integer representing the number of levels to superscript or subscript (1 meaning one level of superscript, 2 meaning two levels, -1 meaning one level of subscript and so on)

## Required Children

None

## Variables Registered

None

## Example

Learn more about using text in [Text Content Conventions](../text_content.html).

### JSON

```json
"styleList": [
  {
    "type": "a",
    "start": 0,
    "end": 12,
    "data": {
      "href": "https://en.wikipedia.org/wiki/Tears_in_rain_monologue"
    }
  },
  {
    "type": "i",
    "start": 41,
    "end": 46
  }
]
```

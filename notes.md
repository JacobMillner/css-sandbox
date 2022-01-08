# CSS Notes

## Selectors

- always target as broad as possible with selectors
- space is a combinator, decendant selector `E F`
- greater sign combinator, direct child `E > F`
- plus sign, adjacent sibling `E + F`, immediate next
- `~` general sibling selector from IE7 `E ~ F`

### Cobinators

Combinators are higher order functions, lambda expressions which have no free
  variables in them.
- `ul li`
- `ol li`
- `ol > li`
- `li.hasaclass + li`

### Attribute Selector

`element[attribute]`

- `image[alt] {}` only selects images with alt attributes
    `<img src="image.jpg" alt="my alt">`
- `form [type] {}` decendant selector with attribute
    `<input type=date>`

- `E[attr]` Element E that has the attribute attr with any value
- `E[attr="val"]` Element E with any attr="val"
- `E[attr|=val]` Element E whose attr has a value val or begins with val + -
    i.e. `p[lang|="en"]` would match `<p lang="en-us">`
- `E[attr^-val]` E whose attr starts with val
- `E[attr$=val]` E whose attr ends with val
- `E[attr*=val]` E whose attr is anywhere within content
- `E[foo="bar" i]` from css selectors 4 you get case insensitivity


## Specificity

Use 0-0-0 to describe specificity weight. Left to right most weight.

`0-0-24 < 0-1-0`

- `1-0-0`: ID selectors
- `0-1-0`: Class and attribute selectors
- `0-0-1`: Element selector

## Misc

- no css specification level 3
  - only 1, 2, 2.1
  - css 3 is broken out into modules like selectors
  - UI/ Selectors level 4
- css has specificity, cascading and inheritence

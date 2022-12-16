---
title: CSS Nesting
stage: seedling
created: 2022-12-16
modified: 2022-12-16
---

{% unfurl "https://developer.chrome.com/blog/help-css-nesting/" %}

> - **Option 1:** @nest: This is the current specified syntax in [CSS Nesting 1](https://www.w3.org/TR/css-nesting-1/). It offers a convenient way to nest appending styles by starting new nested selectors with `&`. It also offers `@nest` as a way to place the `&` context anywhere inside a new selector, like when you're not just appending subjects. It's flexible and minimal but at the expense of needing to remember `@nest` or `&` depending on your use case.
> - **Option 2:** @nest restricted: This is a stricter alternative, in an attempt to reduce the expense mentioned of remembering two nesting methods. This restricted syntax only allows nesting to occur following `@nest`, so there's no append only convenience pattern. Removing ambiguity of choice, creating one easy to remember way to nest, but sacrifices terseness in favor of convention.
> - **Option 3:** Brackets: In order to avoid the double-syntax or extra clutter involved with the `@nest` proposals, [Miriam Suzanne](https://www.miriamsuzanne.com/) and [Elika Etemad](https://twitter.com/fantasai) proposed an [alternative syntax](https://github.com/w3c/csswg-drafts/issues/4748#issuecomment-924118287) that instead relies on additional curly-brackets. This provides syntax clarity, with only two extra characters, and no new at-rules. It also allows nested rules to be grouped by the type of nesting required, as a way of simplifying multiple similarly nested selectors.

{% unfurl "https://webkit.org/blog/13607/help-choose-from-options-for-css-nesting-syntax/" %}

> - **Option 3:** Non-letter start: Nested style rules can be added directly into a declaration block, but cannot start with a letter.
> - **Option 4:** Postfix block: Style rules allow for an optional, second block after the declaration block that contains only style rules.
> - **Option 5:** Top-level @nest: Nested style rules are declared in a dedicated, independent at-rule that accepts only style rules. Declarations can be nested using & { .. }.

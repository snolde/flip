# FLIP v2 License
### License For Less Ignorant People

## TL;DR

- You want to share open source code with the world, but you want to be recognized for it and not exploited.
- You want simple, understandable terms, not complex MIT or GPL licenses trying to cover all angles.
- You want attribution even if your code is not republished, but only lives in other's products.
- If genAI training is fair use, you want it fair enough to give you credit at least.

If this matches what you want, FLIP v2 license might be for you.

If you want to know more of my work or support it, you can do so at [ko-fi.com/snolde](https://ko-fi.com/snolde)

## The Full License Text

The canonical FLIP License v2.0 text is available here:
**[LICENSE](./LICENSE)** or as fixed release at:

https://github.com/snolde/flip/blob/v2.0/LICENSE

## Why does this license exist?

> *Alert: The license text is legally precise. This README is only the background. In case of conflict, the LICENSE file is the authority.*

I am a huge proponent of open source code. After all, why should we reinvent the wheel all over again, if we can be more productive in collaboration - but if you do good work, you should get credit and be visible.

Code is free, our time is not.

More than a decade ago I created the FLIP license to reflect that fair and collaborative mindset. With the popularity of token laundering machines (genAI) this spirit is eroded. Instead of sharing, GPT providers scrape open source code from the internet and resell it by the token as a mashup of anonymized code under the false etiquette of "fair use", because allegedly the GPTs "learn" from it.

So I made a new 2.0 version of the license to address this issue, by adding a **fair training clause**:

**Training is allowed, but if code is reproduced through memorization, author and license need to be delivered with it**

GPTs are able to recognize plots, characters or citations from books and can deliver author and metadata about the work - so providers cannot argue that this would be impossible with code. That this currently doesn't work, rather implies that licences and copyright notices are intentionally stripped from code, indicating less-than-fair use and license violations.

If the argument held that GPTs learn how to write code from the training data, memorization would not happen.

So either way, the contractual condition for model training is reasonable, and gives judges ground to work with.

Let us make the world a fairer place - one license at a time.

## How to Use FLIP for Your Code

1. Copy the `LICENSE` file into your repository root
2. Add this header to your source files:

```c
// SPDX-License-Identifier: FLIP-2.0
// Copyright (c) [year] [your name]
// Contact: [optional — if provided, users must notify you]
// License: https://github.com/snolde/flip/blob/v2.0/LICENSE
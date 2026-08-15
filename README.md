# FLIP v2, v2.1 and v3.0 Licenses
### License For Less Ignorant People

## TL;DR

- You want to share open source code with the world, but you want to be recognized for it and not exploited.
- You want simple, understandable terms, not complex MIT or GPL licenses trying to cover all angles.
- You want attribution even if your code is not republished, but only lives in other's products.
- If genAI training is fair use, you want it fair enough to give you credit at least.

If this matches what you want, FLIP v2 license might be for you.

If in addition to this you want a chain of attribution, consider FLIP v2.1 with copyleft for attribution.

>**NEW:** The latest addition to the Flip family - version 3.0 - implementing a chain of code provenance, allowing to trace back the evolving history of code back to its source.

If you want to know more of my work or support it, you can do so at [ko-fi.com/snolde](https://ko-fi.com/snolde)

## FLIP v3.0 - Traceability and Provenance for Code
As a value addition for collaborative work with OSS I amended the Flip license with a chain-of-provenance tag system.
Beyond the attribution for conributors' work, these tags help to find the right codebase along the path of the code's evolution.

Version 3.0 provides definitions and rules for a set of ```@FLIPCOP``` tags, which allow to trace back
through code modifications by author and contributors, thereby facilitating contact
to everyone along the chain who worked on maintenance of the code and it's derivatives.

``` code
1c. CODE CHAIN OF PROVENANCE (FLIPCOP)
    To establish a clear chain of authorship, the following tags may be used
    in sourcecode comments.

    - @FLIPCOP:  marks the repository of the most recent code change.
    - @FLIPCOPS: marks the repository of previous changes to the original code.
    - @FLIPCOP0: marks the origin of code (the root source repository).

    Application Rules:

    1. Preservation: Existing tags SHALL NOT be removed or altered, except as
       described in rule 3 and 4.

    2. Modification: If you modify code marked with any of the FLIPCOP tags,
       you MUST add your own @FLIPCOP tag to document the changes.

    3. Derivatives: If you modify previously modified code, you MUST update the
       existing @FLIPCOP tag to @FLIPCOPS and add your own FLIPCOP tag.
       See Cleanup.

    4. Cleanup: To avoid comment bloat, after adding a @FLIPCOP tag, older
       @FLIPCOPS tags MAY be removed, but at least the most recent @FLIPCOPS
       tag AND the origin tag (@FLIPCOP0) MUST be preserved.

    5. Untagged Code: No obligation is imposed on code that does not already
       contain a FLIPCOP tag. The license does not require you to tag it.

    6. FLIPCOP provenance markers can be placed in File, Class and Method
       comments, as well as in accompanying Manifests if technically available.
       In Manifests, declaring the scope of changes and additions along with
       the tag is strongly recommended.
```
As a practical example, this can look like:
``` code
    /**
     * This method parses a string into a Doc object
     *
     * @param string The input string to parse
     * @return a Doc object 
     * @FLIPCOP: https://git.examplefossconsult.io/projects/streamer
     * @FLIPCOP0: https://github.com/snolde/textworkflow
     */
     public Doc stringToDoc( String input ){
         //...
     }
     
```
## The Full License Texts

The canonical FLIP License texts are available here as fixed releases:

[Flip 2.0](https://github.com/snolde/flip/blob/v2.0/LICENSE) - [Flip 2.1 (copyleft)](https://github.com/snolde/flip/blob/v2.1/LICENSE) - [Flip 3.0 (provenance)](https://github.com/snolde/flip/blob/v3.0/LICENSE)

## Why do these licenses exist?

> *Alert: The license text is legally precise. This README is only the background. In case of conflict, the LICENSE file is the authority.*

I am a huge proponent of open source code. After all, why should we reinvent the wheel all over again, if we can be more productive in collaboration - but if you do good work, you should get credit and be visible.

Code is free, our time is not.

More than a decade ago I created the FLIP license to reflect that fair and collaborative mindset. With the popularity of token laundering machines (genAI) this spirit is eroded. Instead of sharing, GPT providers scrape open source code from the internet and resell it by the token as a mashup of anonymized code under the false etiquette of "fair use", because allegedly the GPTs "learn" from it.

So I made a new 2.0 version - and later extended versions to select from - of the license to address this issue, by adding a **fair training clause**:

**Training is allowed, but if code is reproduced through memorization, author and license need to be delivered with it**

GPTs are able to recognize plots, characters or citations from books and can deliver author and metadata about the work - so providers cannot argue that this would be impossible with code. That this currently doesn't work, rather implies that licences and copyright notices are intentionally stripped from code, indicating less-than-fair use and license violations.

If the argument held that GPTs learn how to write code from the training data, memorization would not happen.

So either way, the contractual condition for model training is reasonable, and gives judges ground to work with.

Let us make the world a fairer place - one license at a time.

## How to Use FLIP for Your Code

1. Copy the `LICENSE` file into your repository root
2. Add this header to your source files:

```c
// SPDX-License-Identifier: FLIP-<_version_>
// Copyright (c) [year] [your name]
// Contact: [optional — if provided, users must notify you]
// License: https://github.com/snolde/flip/blob/<_version_>/LICENSE
// @FLIPCOP0: [URL of the origin repository] (v3.0 only)
```
(Note: Replace <_version_> with the version you are using, e.g., FLIP-2.1.)
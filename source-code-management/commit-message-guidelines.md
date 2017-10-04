---
description: Commit Message Guidelines
keywords: commit message, guidelines
title: About commit message guidelines
---

##### Commit message guidelines

A good commit message should describe what changed and why.

1. The first line should:
   - contain a short description of the change
   - be 50 characters or less
   - be entirely in lowercase with the exception of proper nouns, acronyms, and
   the words that refer to code, like function/variable names
   - be prefixed with the name of the changed subsystem and start with an
   imperative verb. Check the output of `git log --oneline files/you/changed` to
   find out what subsystems your changes touch.

   Examples:
   - `net: add localAddress and localPort to Socket`
   - `src: fix typos in node_lttng_provider.h`


2. Keep the second line blank.
3. Wrap all other lines at 72 columns.

4. If your patch fixes an open issue, you can add a reference to it at the end
of the log. Use the `Fixes:` prefix and the full issue URL. For other references
use `Refs:`.

   Examples:
   - `Fixes: https://github.com/nodejs/node/issues/1337`
   - `Refs: http://eslint.org/docs/rules/space-in-parens.html`
   - `Refs: https://github.com/nodejs/node/pull/3615`

Sample complete commit message:

```txt
subsystem: explain the commit in one line

Body of commit message is a few lines of text, explaining things
in more detail, possibly giving some background about the issue
being fixed, etc.

The body of the commit message can be several paragraphs, and
please do proper word-wrap and keep columns shorter than about
72 characters or so. That way, `git log` will show things
nicely even when it is indented.

Fixes: https://github.com/nodejs/node/issues/1337
Refs: http://eslint.org/docs/rules/space-in-parens.html
```

##### Resources

- [https://github.com/nodejs/node/blob/master/CONTRIBUTING.md](https://github.com/nodejs/node/blob/master/CONTRIBUTING.md)
- [https://golang.org/doc/contribute.html](https://golang.org/doc/contribute.html)

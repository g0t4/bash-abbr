This is a WIP! Instructions coming soon

## flicker

I've got a fork of bash with a patch that removes code that causes a flicker with bash macros (`bind -x`). This includes the `expand_abbr` macro used by `bash-abbr` to expand snippets into full blown commands. Checkout the repo here: [bash](https://github.com/g0t4/bash) in the [fixed-04-with-type-macro](https://github.com/g0t4/bash/tree/fixed-04-with-type-macro) branch. I ran through `bash tests` and had no troubles with the changes, that said they may not work well on older temrinals. But, modern terminals shouldn't need the proactive clear functionality that causes flicker every time a macro is invoked (not just `expand_abbr` macros).

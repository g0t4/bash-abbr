## Instructions

```
git clone https://github.com/g0t4/bash-abbr
# or copy the bash scripts

source abbr.bash

abbr foo bar

# type `foo<SPACE>` and it will turn into `foo bar`

# see my dotfiles repo (https://github.com/g0t4/dotfiles) for hundreds of abbrs
# - My fish/zsh abbrs are compatible with bash-abbr too
# - I spend most of my time in fish shell, so most are defined in *.fish scripts
```

## Stable vs Latest

This repo is intended to be the stable version. I also have a copy of this in my [dotfiles repo](https://github.com/g0t4/dotfiles/tree/master/bash) so check over there for my latest changes until I merge those into this repo. Look for `abbr.bash`... I probably moved it a few times since setting up these instructions.

## Flicker

I've got a fork of bash with a patch that removes code that causes a flicker with bash macros (`bind -x`). This includes the `expand_abbr` macro used by `bash-abbr` to expand snippets into full blown commands. Checkout the repo here: [bash](https://github.com/g0t4/bash) in the [fixed-04-with-type-macro](https://github.com/g0t4/bash/tree/fixed-04-with-type-macro) branch. I ran through `bash tests` and had no troubles with the changes, that said they may not work well on older temrinals. But, modern terminals shouldn't need the proactive clear functionality that causes flicker every time a macro is invoked (not just `expand_abbr` macros).

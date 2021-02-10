# Learn Haskell

## Table of Contents

- [Learn Haskell](#learn-haskell)
  - [Table of Contents](#table-of-contents)
    - [Introduction](#introduction)
    - [Starting Out](#starting-out)
      - [2.1 Ready, set, go!](#21-ready-set-go)

### Introduction

Install `GHC`(Glasgow Haskell Compiler) compiler in debian system:

```console
root@admin: ~$ apt-get install ghc6 libghc6-mtl-dev
root@admin: ~$ ghci # run script in interactive mode
```

### Starting Out

#### 2.1 Ready, set, go!

The first thing we’re going to do is run `ghq's` interactive mode and call some function to get a very basic feel for haskell. Open your terminal and type in ghci . You will be
greeted with something like this.

```console
devcoders:haskell nahid$ ghci
GHCi, version 8.8.3: https://www.haskell.org/ghc/  :? for help
Prelude>
```

Congratulations, you’re in `GHCI!` The prompt here is `Prelude>` but because
it can get longer when you load stuff into the session, we’re going to use `ghci>`.
If you want to have the same prompt, just type in

```console
Prelude> :set prompt "ghci> "
```

Here’s some simple arithmetic.

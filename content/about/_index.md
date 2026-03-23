---
title: "About"
date: 2026-03-23
---

Hi, I'm **Alex** — a software engineer based in London with a soft spot for systems programming, good writing, and tools that get out of the way.

I spend most of my time building backend infrastructure and thinking about how complex systems fail. Before that I studied computer science at Edinburgh, where I wrote a thesis on distributed consensus that approximately one person read (my supervisor, under duress).

## What I work on

By day I work on data pipelines and developer tooling. The stack is mostly Go and Python, running on things that are either boring by design or exciting by accident.

The tools I reach for most:

- `neovim` — configured slowly over years, changed reluctantly
- `tmux` + `zsh` for a terminal setup that stays out of the way
- `ripgrep` and `fd` because life is short
- `git` with a small set of aliases I've memorised and nothing else

By night I tinker with projects that rarely ship but reliably teach me something. Recently: a terminal-based feed reader in Go, and a half-finished compiler for a language nobody asked for. The compiler is an excuse to read [*Crafting Interpreters*](https://craftinginterpreters.com) properly.

## How I think about software

A quote I keep coming back to:

> Simplicity is prerequisite for reliability.
> <cite>— Edsger W. Dijkstra</cite>

The corollary I've arrived at myself: complexity is usually the residue of unclear thinking, not a sign of thoroughness. The best code I've read looks obvious in hindsight. The worst looks like it was written to impress.

I care a lot about:

1. Software that does one thing well
2. Documentation written for the reader, not the author
3. Error messages that actually say what went wrong
4. Code that someone else can modify six months later without calling you

## A typical working environment

Most of my setup is version-controlled. The piece I'm most attached to is a small shell function that fuzzy-searches my notes:

```bash
# Search notes with fzf + ripgrep, open result in neovim
n() {
  local file
  file=$(rg --files ~/notes | fzf --preview 'bat --color=always {}') \
    && nvim "$file"
}
```

It's roughly thirty characters of actual logic and I use it a dozen times a day. Most good tools feel like that.

Inline: I run `hugo server -D` to preview this site locally, which reloads on save and generally stays out of the way — exactly what a build tool should do.

---

## Outside the screen

I read a lot — mostly history, philosophy of science, and the occasional novel. Right now: *The Structure of Scientific Revolutions* (Kuhn) and a re-read of *Middlemarch*.

I run slowly, cycle occasionally, and make bread that's getting better. The bread, like most things worth doing, is mostly about patience.

> The purpose of abstracting is not to be vague, but to create a new semantic level in which one can be absolutely precise.
> <cite>— Edsger W. Dijkstra, again</cite>

He had a lot of good ones.

## Get in touch

Email is best: [alex@example.com](mailto:alex@example.com)

I'm also on [GitHub](https://github.com) if you want to see what I'm actually building versus what I claim to be building.

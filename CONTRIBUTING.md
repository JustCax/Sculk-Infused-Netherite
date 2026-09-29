# Contributing to Sculk-Infused Netherite

Thank you for looking at the project. This document explains how to propose a
change so it gets merged instead of sitting in a pull request for a month.

Sculk-Infused Netherite is a two-person project. That is the reason for most of
what follows: there is no team of maintainers to review large changes, so the
bar for a small, clear, tested contribution is much lower than the bar for a
large one.

---

## Before you start

**Open an issue before writing code, for anything bigger than a one-line fix.**

An issue takes a few minutes to write. It lets us agree on the approach before
you spend an evening on the wrong one, and it leaves a record of why a change
exists.

Small bug fixes with an obvious fix can go straight to a pull request. A new
feature, a rebalance, a new equipment path or a large refactor should start as
an issue.

**Do not open a pull request with a large batch of unrelated changes.**

This is the single most common reason a contribution gets rejected here. A
reviewer has to understand each change on its own, and a pull request with
fifty commits touching fourteen files cannot be reviewed — so it sits, and
eventually gets closed.

If you have many changes, they belong in several small pull requests, each with
one clear purpose:

- not: *"rework the armor system, add new abilities, fix enchantments, update
  textures, bump the version"*
- but: *"add the Level 11 leggings ability"*, then *"add the Level 12 leggings
  ability"*, then *"fix the leggings tooltip"*

---

## What makes a good pull request

### One purpose

If the description needs the word "and" more than once, it is more than one pull
request. This is a rough test, and it works.

### Small

A bug fix and a formatting pass are two pull requests. So is a bug fix and a
rename. A reviewer should be able to read the whole thing in one sitting.

### Explain why, not what

The diff already shows what changed. What is missing from a diff is the reason:
which bug it fixes, which chat report or log line it came from, why this
approach over the obvious alternative.

### State what you tested on

Say the versions you verified against:

- Minecraft 1.21.1
- NeoForge
- Advanced Netherite
- Deeper and Darker
- Accessories

Mention any other mods in your test instance that could have affected the
result. If you only tested in creative mode, say so — it is genuinely useful
information for a reviewer.

### Keep generated output out

Build directories, IDE folders, logs, screenshots and archives do not belong in
a pull request. If your diff contains more than a few thousand lines, check
whether you accidentally committed build output.

---

## Reporting bugs

A useful bug report contains:

- **the mod version**, Minecraft version and NeoForge version
- **the dependency versions**: Advanced Netherite, Deeper and Darker, Accessories
- **the rest of your mod list**, if the bug might involve another mod
- **what you did**, step by step
- **what you expected to happen**
- **what happened instead**
- **the relevant part of `latest.log`** if the game crashed, or the report from
  the crash screen

A world save that reproduces the problem is worth more than a perfectly
written description, because it can be inspected rather than guessed at.

Two things that help enormously:

- Say whether it reproduces **every time** or only sometimes
- Say whether it happens **in a fresh world** or only in your existing one

---

## Scope

### In scope

- Bug fixes
- Balance and tuning changes, with the reasoning
- New enchantment or ability behaviour that fits the existing design
- Compatibility fixes for other mods
- Documentation, translations and tooltips
- Performance problems

### Out of scope

- Anything copied from another mod, even with attribution
- Modifications intended for redistribution
- Cracked versions of the mod
- Generated or AI-written code that nobody understands — if you cannot explain
  a line, do not submit it
- A complete rewrite of the progression system

---

## Modpack and redistribution

Unmodified official releases of Sculk-Infused Netherite may be included in
modpacks, if the mod came from an official source. Reuploads, modified builds,
derivative releases and reuse of project assets need explicit permission.

See the [LICENSE](LICENSE) for the exact terms. **Ask before you assume** — a
question costs nothing, a takedown costs the whole project.

---

## Security issues

Do not open a public issue for a security problem. See
[SECURITY.md](SECURITY.md) for the private reporting route.

---

## Code of conduct

Be decent to each other. Criticism of code is welcome and normal. Criticism of
the person who wrote it is not.

If someone is being persistently abusive in issues, pull requests or
elsewhere, contact the maintainers rather than escalating it publicly. See
[CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md).

# Working in this repository

This repository is Geoffrey Vancoetsem's personal page, served by GitHub
Pages at <https://geeooff.github.io/>. It supports a job search: an
experienced .NET software engineer looking for a role in aerospace, space or
defence — the positions where his experience applies as is, and
safety-critical embedded software, which he is preparing for.

This file is for coding agents and for people. It says how to work here.
What the page claims is checked against the sources named below, never
recalled from memory. Per-machine notes that must not be committed live in
`CLAUDE.local.md`, which Git ignores.

## What the page is

- Two pages, one content: `index.html` in English at the root, `fr/index.html`
  in French. English is the default; French is one click away. The French
  version is not a word-for-word translation, but it says the same things in
  the same order.
- Static, with no framework, no JavaScript, no tracker, no external
  dependency. `.nojekyll` tells GitHub Pages to serve the files as they are.
  This is a choice, not an intermediate step: do not add a generator, a
  remote font or an analytics script.
- `style.css`: colours as variables on `:root`, dark mode through
  `prefers-color-scheme`, system fonts, one measure of text.

## Tone — the rule that matters most

The first version of the page was rejected for its tone, not its facts.
Geoffrey speaks plainly, without spin, and does not want to "sell himself".
Everything below follows from that.

- Short sentences. Facts, dates, names. No adjective of merit.
- No antithesis ("where others see…, I see…"), no catchphrase, no maxim, no
  "values" section.
- Limits are stated as they are: no experience in embedded, exercises rather
  than certified projects, a level that is not that of someone who has done
  this for fifteen years.
- What can be verified goes into a project's description; what cannot is
  removed.
- His own writing sets the register: the GameModeExecutor README in English,
  his LinkedIn profile in both languages.

## Facts and their sources

- The CV (French and English) and the LinkedIn content are the source of
  truth for the career; they are kept outside the repository. The page must
  stay aligned with LinkedIn, and LinkedIn with the page: a date, a title or
  a skills line that differs is a defect.
- Any figure or claim about a project is checked in that project's
  repository before it is written: number of tests, dates, stars, mechanisms.
- Private repositories are described only by approach — what they cover,
  with which tools — never as an inventory, with no detailed figures and no
  structure. Only those that serve the professional project appear. While a
  repository is private, the page says "private for now, open on request";
  when it becomes public, the mention becomes a link.
- The note on AI assistance stays: it is a fact (commits carry
  `Co-Authored-By`), stated with its reservation. It is never presented as an
  asset.

## Making a change

1. Change both pages in the same commit. Content present in one language and
   missing from the other is a regression.
2. Check locally: serve the folder (`python -m http.server 8765`) rather than
   opening the file over `file://`, which does not resolve `style.css` in
   some embedded browsers. Check desktop, mobile (375 px, no horizontal
   scroll), light and dark modes, and the language switch in both directions.
3. Check that relative links resolve and that files are UTF-8 without BOM. On
   Windows, run Python scripts with `PYTHONUTF8=1` or `python -X utf8`: a
   cp1252 console has already made correct files look mis-encoded.
4. Update `README.md` if the structure changes.

## Commits and publishing

- Commit messages in English, short and impersonal; one commit per lot,
  without mixing the page, the conventions and the tooling.
- No `push` without an explicit request. Every `push` publishes the page.
- Need explicit approval, every time: pushing, changing the GitHub profile
  (bio, website, pinned repositories), making a private repository public,
  removing or rewording the note on AI assistance.

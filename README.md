# chatterbox (fork)

> **This is a fork. It is not an actively developed project. It is not used by any of my other repositories. It exists only as a delivery mechanism for two pull requests sent upstream.**

## What this repo is

This is a personal fork of [resemble-ai/chatterbox](https://github.com/resemble-ai/chatterbox), the open-source TTS engine. I do not maintain Chatterbox. I do not extend it. I do not ship anything from this fork.

The fork exists for one mechanical reason: GitHub requires you to fork a repository into your own account before you can open a pull request against it. Once the upstream maintainers merge or reject the pull requests below, this fork has no further purpose.

## Why it is public

GitHub forces a fork's visibility to match the upstream repository. Chatterbox upstream is public, so this fork is forced public. There is no setting to make it private without breaking the pull request links.

## Pull requests this fork is hosting

While building [AudiobookMaker](https://github.com/MikkoNumminen/AudiobookMaker), I hit a forward-hook leak in Chatterbox's multilingual `T3.inference()` path that made the engine collapse to ~0.4 seconds of audio after the first call. That is a showstopper for any long-form work (audiobooks, batched synthesis, anything that reuses a loaded model). I diagnosed the bug, wrote a fix, and sent it upstream. The branches backing those pull requests live in this fork:

- [resemble-ai/chatterbox#505](https://github.com/resemble-ai/chatterbox/pull/505) — *fix: remove forward-hook leak in AlignmentStreamAnalyzer*
- [resemble-ai/chatterbox#510](https://github.com/resemble-ai/chatterbox/pull/510) — *fix(t3): remove forward-hook leak in alignment analyzer*

Both are open as of this writing. Discussion happens on the upstream pull request pages, not here.

## What you should do instead

- For the actual Chatterbox project, code, releases, issues, and documentation: go to [resemble-ai/chatterbox](https://github.com/resemble-ai/chatterbox).
- Issues opened on this fork will not be reviewed.
- Pull requests opened against this fork will not be reviewed.

## My active work

If you came here from my profile and were looking for projects I actually build and maintain, see:

- [AudiobookMaker](https://github.com/MikkoNumminen/AudiobookMaker) — turn PDFs, EPUBs, or plain text into audiobooks. Multiple TTS engines, Finnish-first, Windows.
- [mikkonumminen.dev](https://github.com/MikkoNumminen/mikkonumminen.dev) — portfolio page.
- [ReadLog](https://github.com/MikkoNumminen/ReadLog) — track every book you've read.

# Contributing to This Guide

This repo is the onboarding guide itself, and it is open source too.
If you spot a typo, a step that did not work on your machine, or an
explanation that confused you, you can fix it. That fix helps every
person who comes after you.

If you have not been through the guides yet, start with
[What Is Open Source?](./Getting-Started/00-what-is-open-source.md).
Contributing here uses exactly the same steps you learn there.

If you meet a word on this page you do not know, the
[Glossary](./GLOSSARY.md) explains every term these guides use, in
plain language. Nothing below assumes you have memorised any of it.

---
## Before anything else

Everyone contributing here follows the
<a href="https://community.codetopia.org/code-of-conduct" target="_blank" rel="noopener noreferrer">Codetopia Community Code of Conduct</a>.
Most of it is what you would do anyway: assume good faith, be patient
with people who are new, and keep criticism about the work rather than
the person.

---
## What we need most

You do not need to be an expert on Git to improve this guide. In fact,
the closer you are to being a beginner, the more useful your feedback
is. The most valuable contributions here are:

- **Fixing anything that did not work for you.** A command that failed,
  output that did not match what the guide said you would see, a link
  that is broken.
- **Clarifying confusing wording.** If you had to read a paragraph
  three times, rewrite it so the next person only reads it once.
- **Filling in missing steps.** If you had to search the internet to
  get past a step, that step is missing something.
- **Adding screenshots.** Several guides have image placeholders
  waiting to be filled in. See [Adding images](#adding-images) below.
- **Platform gaps.** Most steps are written for Windows, macOS, and
  Linux. If your platform is missing or wrong, say so.

Please do not open a pull request that rewrites a whole guide at once.
Small, focused changes get reviewed and merged quickly. Large ones sit
around waiting.

---
## Where things go

Before you open anything, a quick check on which of these you have.
Both places below are parts of GitHub you may never have used. An
[issue](./GLOSSARY.md#issue) is a public note on a project saying
something needs attention, and
[GitHub Discussions](./GLOSSARY.md#github-discussions) is its question
and answer forum. Each sits on its own tab at the top of the repo.

| What you have | Where it goes |
|---|---|
| "This is broken" or "this should exist" | An **issue**, on the **Issues** tab |
| "Why does this work this way?" | **GitHub Discussions**, on the **Discussions** tab |
| "I am stuck right now, is anyone around?" | **GitHub Discussions**, same place |

The test is whether somebody would need to *do* something about it. If
yes, it belongs in an issue, where it can be tracked until it is done.
If it is just a question, it does not.

[Reporting a Good Issue](./Getting-Started/10-reporting-a-good-issue.md)
walks through writing an issue properly, and [HELP.md](./HELP.md)
covers asking questions.

---
## How to contribute

Do this on your own computer, not in the GitHub web editor. Editing a
file in the browser is quicker, but going through the real workflow is
the entire point of this repo, and it is the thing you are here to
learn. If you have not worked through the guides that teach it yet,
start there and come back. Nothing here is going anywhere.

If a step here is unfamiliar, the guide that teaches it is linked next
to it.

1. **Say you are taking it.** If an issue already describes what you
   want to do, comment on it before you start. That stops two people
   spending an evening on the same thing, and if it is trickier than it
   looks, somebody can warn you before you begin rather than after. If
   nothing covers what you have in mind, open an issue first, unless it
   is an obvious typo.
   ([Finding and Claiming an Issue](./Getting-Started/07-finding-and-claiming-an-issue.md))
2. **Fork this repo and clone your fork** to your computer.
   ([Your First Pull Request](./Getting-Started/05-your-first-pull-request.md))
3. **Create a branch** named for what you are doing:
   `fix/broken-link-guide-04`, `docs/clarify-ssh-step`.
4. **Make your change** and read it back once before committing.
5. **Commit** with a message in the style described below.
6. **Push your branch** and open a pull request explaining what you
   changed and why. If it closes an issue, write `Closes #N` in the
   description.
   ([Your First Pull Request](./Getting-Started/05-your-first-pull-request.md))
7. **Respond to review comments.** A maintainer will read your change
   and may suggest a tweak. That is normal, and it is not criticism.
   ([Reviewing a Pull Request](./Getting-Started/06-reviewing-a-pull-request.md))

---
## Adding or renaming a guide

The guides in `Getting-Started/` are numbered from `00`, and the links
at the top and bottom of each one are generated rather than typed by
hand. If you add a guide, rename one, or change its `# Title`, run this
in the folder you cloned, the one with `README.md` sitting in it:

```bash
python3 scripts/build-nav.py
```

Then commit the files it changes. It rewrites the previous and next
links and the progress bar in every guide, so one new guide does not
mean editing twelve files by hand.

That command needs Python, which this course never installs and you do
not otherwise need. If you get `python3: command not found`, do not go
and install anything for this. Say so in your pull request and a
maintainer will run it for you. It takes them ten seconds.

You do not need any of this for ordinary edits like fixing a typo. If
you forget, the automatic [checks](./GLOSSARY.md#checks) on your pull
request will say so, and they name the same command. That is not you
being told off: it is the check doing its job.

One of those checks confirms that every link inside this repo goes
somewhere real. It leaves links to other websites alone, because those
can break without anybody here touching anything, and a check that
fails for reasons outside the change is a check people learn to ignore.
Maintainers can test those by hand with
`python3 scripts/check-links.py --external`.

---
## Commit messages

Use a short prefix, then a description in the present tense of what
the change does:

```bash
git commit -m "docs: clarify the SSH key passphrase step in guide 04"
git commit -m "fix: correct broken link to guide 08 in the README"
```

- `docs:` for wording, structure, or new content
- `fix:` for something that was actually wrong: broken links, wrong
  commands, incorrect output
- `chore:` for everything else, like renaming or moving files

Keep the first line under about 72 characters. If a change needs more
explanation, put it in the pull request description rather than
cramming it into the commit message.

---
## Writing style

The guides follow a consistent style. Match it so the whole thing
reads as one voice.

**Write for someone who has never done this before.** No assumed
knowledge. If you use a term for the first time, explain it in the
same sentence, and link it to its [Glossary](./GLOSSARY.md) entry:
`[issue](./GLOSSARY.md#issue)`. A reader who has landed on one page
from a search engine has not read the twelve guides before it, and
should not have to.

**Say what to type and what should happen.** Every command gets a
fenced code block, followed by a "What you should see" description of
the expected output. A beginner cannot tell success from failure
without it.

````markdown
```bash
git status
```

What you should see:

```
On branch main
nothing to commit, working tree clean
```
````

**Use second person and plain language.** "You will see", not "the
user will observe".

**Refer to a guide by its name, not its number.** Write
`[Your First Pull Request](./Getting-Started/05-your-first-pull-request.md)`,
not "guide 05". The number tells a reader nothing about what is in it,
so they have to follow the link before they can decide whether they
want to. The file numbers exist to keep the files in order, and the
navigation strips at the top and bottom of each guide are generated,
so leave those alone.

**Wrap prose at about 70 characters.** Keep links, tables, and code
blocks on one line even when they run longer.

**Use GitHub alerts for asides**, not bold paragraphs:

```markdown
> [!TIP]
> Useful but optional.

> [!NOTE]
> Worth knowing before you continue.

> [!IMPORTANT]
> Skipping this will cause problems later.
```

**Open external links in a new tab** so nobody loses their place in
the guide:

```markdown
<a href="https://example.com" target="_blank" rel="noopener noreferrer">Example</a>
```

Links to other files in this repo are plain Markdown links.

---
## Guide structure

Each numbered guide in `Getting-Started/` follows the same shape:

1. `# Title`, then a short intro on what this guide is for
2. `## What you will do in this guide`, a bulleted list
3. `## Step 1:`, `## Step 2:`, and so on, separated by `---`
4. `## Quick reference`, a table of what was learned, where useful
5. `## What's next?`, ending with a link to the following guide:
   `🔗 [Next Guide Title](./NN-next-guide.md)`

If you add a new guide, number it in sequence, link it from the
`What you will learn` list in the README, and update the `What's
next?` link at the end of the guide before it. Then run
`python3 scripts/build-nav.py` to regenerate the strips at the top and
bottom of every guide, as described in
[Adding or renaming a guide](#adding-or-renaming-a-guide) above.

---
## Adding images

Guides mark where a screenshot belongs with an HTML comment:

```markdown
<!-- IMAGE: Terminal showing git status output. Target path: images/git-status-modified.png -->
```

To fill one in, take the screenshot or animation described, save it
at the target path, and replace the comment with the image/GIF:

```markdown
![Terminal showing git status output](../images/git-status-modified.png)
```

Some rules for screenshots and animations:

- Crop to what matters. No full desktops, no visible taskbars.
- Blur or edit out anything personal: email addresses, real file paths
  with your name in them, tokens, anything private.
- Use PNG for static screenshots, and GIF for short animations. Keep
  PNG files under 500 KB, and GIF files under 2 MB to keep guides
  fast and lightweight.
- **Only use GIFs when motion is necessary** to explain a concept or
  interactive process (such as a terminal workflow or GitHub
  interface action). Keep animations short, focused, and
  loop-optimized.
- Always write alt text that describes what is in the image, for
  people using a screen reader.
- Keep every screenshot or GIF in one guide consistent with the
  others: same theme, same account, same machine. Use whichever
  GitHub theme you already use, there is no need to switch to
  match anyone. The point is that a reader never watches the
  interface change halfway through a guide, or the username swap
  between one step and the next.

Use whatever screenshot tool your computer already has. To crop, any
image editor will do, including Photos on Windows and Preview on
macOS. For recording animated GIFs, free tools like **ScreenToGif**
(Windows) or **LICEcap** (macOS/Windows) are highly recommended. If
you already have a video, you can convert it to GIF on any device
using <a href="https://cloudconvert.com/gif-converter" target="_blank" rel="noopener noreferrer">CloudConvert</a>.
You do not need to blur anything properly either: drawing a filled
rectangle over an email address is fine, and easier to get right.

---
## Before you open your pull request

- [ ] Your change is focused on one thing.
- [ ] Every command you added has been run on a real machine.
- [ ] Every new link has been clicked and works.
- [ ] Prose wraps at about 70 characters.
- [ ] The README list is updated if you added or renamed a guide.
- [ ] Any term a newcomer might not know links to the Glossary the
      first time you use it.

---
## Licensing of what you contribute

This project is released under the
<a href="https://creativecommons.org/licenses/by/4.0/" target="_blank" rel="noopener noreferrer">Creative Commons Attribution 4.0 International licence</a>.
By opening a pull request you agree that your contribution is offered
under that same licence, which is what lets anyone else read, share and
build on it.

Practically, this means two things. Only contribute writing that is
yours to give. And if you quote or adapt someone else's work, say where
it came from, in the pull request and in the text.

---
## Getting help

Stuck on any of this, or unsure whether an idea is worth doing? Ask in
<a href="https://github.com/codetopiacommunity/opensource-onboarding/discussions/categories/q-a" target="_blank" rel="noopener noreferrer">GitHub Discussions</a>
using the **Q&A** category. It reaches the community Discord on its own,
so there is nowhere else you need to post. [Getting Help](./HELP.md)
covers how. Asking first is always welcome. Nobody here will mind.

[Hope Decardi-Nelson](https://github.com/blackbox24)
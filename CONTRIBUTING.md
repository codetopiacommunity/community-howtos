# Contributing to Community How-Tos

This repository contains the onboarding and how-to guides for Codetopia Community (`community-howtos`), and it is open source too. If you spot a typo, a step that did not work on your machine, or an explanation that confused you, your fix helps every person who comes after you.

Everyone contributing here follows the <a href="https://community.codetopia.org/code-of-conduct" target="_blank" rel="noopener noreferrer">Codetopia Community Code of Conduct</a>.

> **New to GitHub?** You do not need to understand forks or branches to
> help. Start with
> [Your First Pull Request](https://community.codetopia.org/howtos/contributing/your-first-pull-request),
> a ten-minute guide in your browser. Any unfamiliar word below is
> explained in the onboarding course's
> [glossary](https://github.com/codetopiacommunity/opensource-onboarding/blob/main/GLOSSARY.md).
---

## What We Need Most

- **Fixing typos and broken links:** Correcting inaccurate commands, broken links, or outdated steps.
- **Clarifying wording:** Rewriting confusing paragraphs so newcomers understand them on the first read.
- **Adding screenshots:** Replacing image placeholders with clear, cropped screenshots or GIFs.
- **Platform gaps:** Ensuring steps work across Windows, macOS, and Linux.

---

## How to Contribute

Depending on what you want to change, you can contribute directly in your browser or locally:

1. **Quick fixes (Browser):** For typos, broken links, or minor text updates, edit the file directly in your browser: open it on GitHub, click the pencil icon, make the change, then click **Commit changes...** and **Propose changes**, and open the pull request. GitHub makes your fork for you. New to pull requests? [Your First Pull Request](./Contributing/03-your-first-pull-request.mdx) walks you through one step by step.
2. **New guides or substantial additions:** For larger contributions, fork the repository, create a branch (`docs/your-topic`), and open a pull request. If you are not yet comfortable with GitHub, you can draft your guide in a Google Doc and post it in the `#general` channel on Discord where a member can help open the pull request for you.

---

## Where Things Go

- **Found a bug, typo, or something missing?** Open an issue on GitHub.
- **Need help or have questions?** Ask in the `#ask-for-help` channel on Discord.

---

## Writing Style & Conventions

When editing or writing guides in this repository, follow these conventions:

- **Format:** Guides are written in MDX (`.mdx`) with YAML frontmatter:

  ```yaml
  ---
  title: Guide Title
  description: Brief description of the guide.
  ---
  ```

- **File names:** number guides within their folder, starting at `01`: `01-ways-to-contribute.mdx`, `02-help-out.mdx`. The number only sets the order. The website leaves it out of the address, so `Contributing/02-help-out.mdx` lives at `community.codetopia.org/howtos/contributing/help-out`. Renumbering never breaks a link, but two guides in the same folder must not share a name after the number.
- **Links between guides:** use the address without the number, like `../contributing/help-out` or `./discord-guide`.

- **Plain language & second person:** Write for beginners. Use "you will see" rather than passive voice.
- **Commands & output:** Every command should be in a fenced code block followed by a "What you should see" description and output block.
- **GitHub alerts:** Use standard alerts for asides:

  ```markdown
  > [!TIP]
  > Useful but optional.

  > [!NOTE]
  > Worth knowing before you continue.

  > [!IMPORTANT]
  > Skipping this will cause problems later.
  ```

- **External links:** Always open external links in a new tab:

  ```markdown
  <a href="https://example.com" target="_blank" rel="noopener noreferrer">Example</a>
  ```

- **Images & Placeholders:** Mark image needs using MDX comment syntax:

  ```markdown
  {/* IMAGE NEEDED: images/Getting-Started/... */}
  ```

  Save actual images under the `images/` directory. Keep static images as PNGs under 500 KB and GIFs under 2 MB.

- **Show things as they look on screen.** Guides can use these components (the website renders them; on GitHub they show as plain text):

  | Write | For | Example |
  |---|---|---|
  | `<Command>/link</Command>` | a Discord command to type | Type `<Command>/newhere</Command>` |
  | `<Channel>ask-for-help</Channel>` | a Discord channel (no `#`) | Ask in `<Channel>ask-for-help</Channel>` |
  | `<Button>Create Account</Button>` | a button, exactly as labelled | Click `<Button>Save Changes</Button>` |
  | `<Key>Enter</Key>` | a keyboard key | Hold `<Key>Shift</Key>` and press `<Key>Enter</Key>` |
  | `<DoneWhen>…</DoneWhen>` | how the reader knows they finished | Wrap the list, with blank lines inside |
  | `<Steps>` + `<Step title="…" href="…" time="…">…</Step>` | numbered step cards | See README.md |
  | `<Cards>` + `<Card title="…" href="…">…</Card>` | a grid of cards | See README.md |

  Don't put components inside headings or inside link text.

- **Images side by side:** wrap them in `<ImageRow>`, one image per line, for example a phone's channel list next to an open channel. They share the width equally and wrap on narrow screens:

  ```mdx
  <ImageRow>
  ![Channel list on a phone](https://raw.githubusercontent.com/.../channels.jpg)
  ![An open channel on a phone](https://raw.githubusercontent.com/.../messages.jpg)
  </ImageRow>
  ```

---

## Licensing

This project is released under the <a href="https://creativecommons.org/licenses/by/4.0/" target="_blank" rel="noopener noreferrer">Creative Commons Attribution 4.0 International licence</a>. By opening a pull request, you agree that your contribution is offered under the same licence.

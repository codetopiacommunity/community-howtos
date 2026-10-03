# Contributing to Community How-Tos

This repository contains the onboarding and how-to guides for Codetopia Community (`community-howtos`), and it is open source too. If you spot a typo, a step that did not work on your machine, or an explanation that confused you, your fix helps every person who comes after you.

Everyone contributing here follows the <a href="https://community.codetopia.org/code-of-conduct" target="_blank" rel="noopener noreferrer">Codetopia Community Code of Conduct</a>.

---

## What We Need Most

- **Fixing typos and broken links:** Correcting inaccurate commands, broken links, or outdated steps.
- **Clarifying wording:** Rewriting confusing paragraphs so newcomers understand them on the first read.
- **Adding screenshots:** Replacing image placeholders with clear, cropped screenshots or GIFs.
- **Platform gaps:** Ensuring steps work across Windows, macOS, and Linux.

---

## How to Contribute

Depending on what you want to change, you can contribute directly in your browser or locally:

1. **Quick fixes (Browser):** For typos, broken links, or minor text updates, you can edit files directly in your browser using the pencil icon, as shown in [Your First Fix](./Contributing/05-your-first-fix.mdx).
2. **New guides or substantial additions:** For larger contributions, fork the repository, create a branch (`docs/your-topic`), and open a pull request. If you are not yet comfortable with GitHub, you can draft your guide in a Google Doc and post it in the `#general` channel on Discord where a member can help open the pull request for you (see [Ways to Contribute](./Contributing/06-ways-to-contribute.mdx)).

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

---

## Licensing

This project is released under the <a href="https://creativecommons.org/licenses/by/4.0/" target="_blank" rel="noopener noreferrer">Creative Commons Attribution 4.0 International licence</a>. By opening a pull request, you agree that your contribution is offered under the same licence.

# LLM Prompts

[![License](https://img.shields.io/badge/license-CC0%201.0-green)](LICENSE.md)

This repository contains a curated collection of prompts designed to be
used with [large language models
(LLMs)](https://en.wikipedia.org/wiki/Large_language_model) to enhance
productivity and streamline various tasks. The prompts cover a wide
range of areas, including coding, writing comments, reviewing grammar,
and more.

While the prompts were originally written and tested using Anthropic's
Claude 3 Opus model, they should be compatible with any LLM.

> **Note:** Unless stated otherwise, use these prompts as system
> prompts, not user prompts. Also, keep in mind that the responses can
> be quite verbose by design and optimizing for cost efficiency was not
> a primary goal when writing the prompts.

## List

- [Behavior Therapist](data/behavior-therapist.md)
- ["Best Friend"](data/best-friend.md)
- [Brazilian Accountant](data/brazilian-accountant.md)
- [Business Idea Generator](data/business-idea-generator.md)
- ["Catch-all" Assistant](data/catch-all-assistant.md)
- [CLI UX Improver](data/cli-ux-improver.md)
- [Code Comment Writer](data/code-comment-writer.md)
- [Coding in Go](data/coding-in-go.md)
- [Coding in PHP (With a Focus on WordPress)](data/coding-in-php-with-wordpress-focus.md)
- [Coding in Rust](data/coding-in-rust.md)
- [Coding in TypeScript](data/coding-in-typescript.md)
- [Computer Science PhD](data/computer-science-phd.md)
- [Copywriting Expert](data/copywriting-expert.md)
- [Grammar Reviewer](data/grammar-reviewer.md)
- [jQuery Converter](data/jquery-converter.md)
- [Manpage Writer](data/manpage-writer.md)
- [Naming Expert](data/naming-expert.md)
- [Prompt Generator](data/prompt-generator.md)
- [README Writer](data/readme-writer.md)
- [Testing in Go](data/testing-in-go.md)
- [Translation Teacher](data/translation-teacher.md)
- [Website Generator](data/website-generator.md)

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for details.

## Acknowledgements

- Most prompts were written using a combination of [Anthropic's
  metaprompt](https://docs.anthropic.com/en/docs/helper-metaprompt-experimental)
  and manual work.
- The [manpage writer](data/manpage-writer.md) prompt includes the
  manpage for the `scdoc` utility. Copyright belongs to Drew DeVault.

## Resources

- [Patches](https://lists.sr.ht/~jamesponddotco/public-inbox).
- [Instructions on how to prepare patches](https://git-send-email.io/).
- [Feature requests and prompt suggestions](https://todo.sr.ht/~jamesponddotco/public-tracker).

---

Released under the [CC0 license](LICENSE.md).

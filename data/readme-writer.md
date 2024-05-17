# README Writer

This prompt helps you create a starting point for your project's README
file. Replace the example in the prompt with whatever you prefer to use
as inspiration.

## Prompt

### System

````text
You will be acting as a language expert with a PhD in computer science to analyze a code sample and write a README file for it. The user will provide you with the code. Your task is to carefully read the code to understand what it does, and then fill out the README following the example below.

Here is an example README file:
<readme_example>
# `allalt`

`allalt`, a.k.a, "**all** images deserve an **alt** tag", is a simple CLI tool that transforms images into words. Designed to provide text-based descriptions of images for visually impaired users, it leverages the power of [GPT-4V](https://openai.com/research/gpt-4v-system-card) to make visual content accessible in a textual format.

`allalt` serves as a handy utility for web developers and content creators to generate alt text for images, enhancing web accessibility.

The tool is built to be as user-friendly as possible, with a focus on ease of use and accessibility.

## Installation

### From source

First install the dependencies:

- Go 1.21 or above.
- make.
- [scdoc](https://git.sr.ht/~sircmpwn/scdoc).

Switch to the latest stable tag, `v0.2.0`, then compile and install:

```bash
git checkout v0.2.0
make
sudo make install
```

## Usage

```bash
$ allalt --help
NAME:
   allalt - describe images for visually impaired users

USAGE:
   allalt [global options] [arguments...]

VERSION:
   0.1.0

GLOBAL OPTIONS:
   --key value, -k value                                    the OpenAI API key to use [$ALLALT_KEY]
   --language value, -l value                               the language to use when describing images (default: "en_US") [$ALLALT_LANGUAGE]
   --context value, -c value                                the context around the image to use when describing images [$ALLALT_CONTEXT]
   --keyword value, -K value [ --keyword value, -K value ]  potential keywords relevant to the image
   --help, -h                                               show help
   --version, -v                                            print the version
```

See _allalt(1)_ after installing for more information.

## Contributing

Anyone can help make `allalt` better. Send patches on the [mailing list](https://lists.sr.ht/~jamesponddotco/allalt-devel) and report bugs on the [issue tracker](https://todo.sr.ht/~jamesponddotco/allalt).

You must sign-off your work using `git commit --signoff`. Follow the [Linux kernel developer's certificate of origin](https://www.kernel.org/doc/html/latest/process/submitting-patches.html#sign-your-work-the-developer-s-certificate-of-origin) for more details.

All contributions are made under [the GPL-2.0 license](LICENSE.md).

## Resources

The following resources are available:

- [Support and general discussions](https://lists.sr.ht/~jamesponddotco/allalt-discuss).
- [Patches and development related questions](https://lists.sr.ht/~jamesponddotco/allalt-devel).
- [Instructions on how to prepare patches](https://git-send-email.io/).
- [Feature requests and bug reports](https://todo.sr.ht/~jamesponddotco/allalt).

---

Released under the [GPL-2.0 license](LICENSE.md).
</readme_example>

Please read the code carefully and make sure you fully understand its purpose, functionality, dependencies, and any other key aspects needed to write a good README.

Then, complete the README by using the example as inspiration. Be sure to follow the example exactly and do not skip any sections, even if you think they may not be applicable. If a section truly does not apply, write "N/A" for that section.

When referring to the code in the README, use inline code blocks with backticks to format any code, variable names, function names, etc.

After completing the README, please output the result with no additional commentary. The user just need the completed README file.
````

### User

```text
Can you write a README file for my command-line application, please?

<code>
{{CODE}}
</code>
```

The content of `{{CODE}}` is omitted for brevity, but it's basically the
entire output of the [janus
repository](https://sr.ht/~jamesponddotco/janus/), minus `README.md` and
manpage, processed through
[llmctx](https://sr.ht/~jamesponddotco/llmctx).

## Example output

### Parameters

- **Model:** claude-3-opus-20240229
- **Temperature:** 1

### Output

````text
# `janus`

`janus` is a simple and easy-to-use command-line utility for comparing files and finding differences between them.

## Installation

### From source

First, ensure that you have Go installed on your system.

Then, you can install `janus` by running:

```bash
go install git.sr.ht/~jamesponddotco/janus@latest
```

## Usage

```bash
$ janus --help
Usage: janus [options] <oldFile> <newFile>
Options:
  -no-color
        do not colorize the output
  -version
        display version information
```

See _janus(1)_ after installing for more information.

## Contributing

Anyone can help make `janus` better. Follow the [contribution guidelines](CONTRIBUTING.md) to get started.

All contributions are made under [the EUPL-1.2 license](LICENSE.md).

## Resources

The following resources are available:

- [Source code](https://git.sr.ht/~jamesponddotco/janus)
- [Issue tracker](https://todo.sr.ht/~jamesponddotco/janus)

---

Released under the [EUPL-1.2 license](LICENSE.md).
````

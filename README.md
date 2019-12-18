<!-- vim: set ai si sta et sw=4 sts=4 fenc=utf-8 nobomb eol ff=unix ft=markdown: -->

# [@oliveiraev][user:oliveiraev]'s template repository and community files

## What are community files?

Community files are "metacontent" that provide help to users on how to use the
project, where to find help, how to contribute and how to report issues.

Repository services such as [Github][site:github] and [Gitlab][site:gitlab]
also make use of specific files as templates like [issue][help:issues] and
[pull request][help:pull-request] templates.

## Why are they important?

Cuz they give **you** autonomy to get started by yourself without needing of
another human to guide you. Since every project has potential to become
worldwide at anytime, the core maintainers couldn't be available to help you
due to business-times or different timezones. Also, if a small project become
famous, the sole single maintainer wouldn't be able to answer all the people
questions, including the repeated ones.

Here comes files like [README][src:readme.md], that explains the project
purposes and give you directions about how to go further.
[CONTRIBUTING][src:contributing.md], containing coding-standards,
[pull-request policies][src:pull-request-template.md],
how to run the tests and all the other development cool stuff.
[LICENSE][src:license.md], that explains what you can and - even more important
\- **can't** do with the code and the software that it produces.
[SUPPORT][src:support.md] files provide information about the community
channels where you can get (and offer) help.

## Where are they from?

Github team started a project called [OpenSource Guide][guide:home] with tips
about [how to build welcoming communities][guide:communities],
[leadership and governance][guide:leadership],
[code of conduct][guide:code-of-conduct] and [legal stuff][guide:legal] for
maintainers among other things and [how to contribute][guide:contribute] for
people looking for existent projects that need some help.

## What about *"git files"*?

Mainly: [.gitignore][src:.gitignore] and [.gitattributes][src:.gitattributes].

[.gitignore][help:gitignore] provides a list of files that shouldn't be
versioned through the repository. Sample of these files are build artifacts and
temporary-intermediary files like cache or tempfiles and IDE/editors settings.

[.gitattributes][help:gitattributes] tells git how to behave with versioned
files, like how to parse them, show its diffs, if it should apply any
filter/algorithm and also helps handling linebreaks between different
operational systems.

## Usage

This repository intent is to be used as a boilerplate to other
repositories/projects offering files mentioned in
*[why are they important?][anchor:why-are-they-important]* and
*[what about git files?][anchor:what-about-git-files]* sections. Linter start
packs will also be provided here, alongside with a Makefile with jobs that may
be common among maintained projects (like the above mentioned *lint* task).

If this repo be [forked][action:fork] and the fork enables [pull][app:pull] app
on Github, updates made here will be automatically reflected on the forked
repository, inheriting updates, fixes, settings, new linters and additional
configs.

## Branching model

- [Master][branch:master] should keep the latest stable code and the latest
stable tag should point to its HEAD

- [Staging][branch:staging] holds the RCs and Beta versions. A human - usually,
the reporter - had already verified the feature at
[development][branch:dev]

- [Development][branch:dev] contains Alpha and Canary builds. Commits are
automatically tested and conflict-free but weren't validated by a person

## Versioning system

**The core should be kept like [semver 2.0.0][site:semver]**

- Breaking changes increment MAJOR and reset MINOR and PATCH to 0

- New features increment MINOR and reset PATCH to 0, keeping MAJOR version

- Bugfixes, Typo, Docs, Developer tools, Build/CI System, tests and refactor
increments PATCH version, keeping MAJOR and MINOR values

- [Development][branch:dev] commits triggers tags that ends with *-alpha*

- The last commit @[dev][branch:dev] on the previous day is tagged as
*-nightly*

- [Staging][branch:staging] commits triggers tags that ends with *-beta*

- If the release cycle contains a *feature freeze* schedule, during the feature
freeze period, [staging][branch:staging] commits are tagged as *-RC*

- [Master][branch:master] commits are always tagged as final versions

## License

This project is licensed under [Lesser GNU Public License v3][src:license.md]

![LGPLv3 Logo](docs/assets/img/lgplv3.svg)

[user:oliveiraev]: ../../../../oliveiraev

[site:github]: https://github.com
[site:gitlab]: https://gitlab.com
[site:semver]: https://semver.org

[action:fork]: ../../fork

[branch:master]: ../../tree/master
[branch:staging]: ../../tree/staging
[branch:dev]: ../../tree/dev

[help:issues]: https://help.github.com/en/github/building-a-strong-community/configuring-issue-templates-for-your-repository
[help:pull-request]: https://help.github.com/en/articles/creating-a-pull-request-template-for-your-repository
[help:gitignore]: https://git-scm.com/docs/gitignore
[help:gitattributes]: https://git-scm.com/docs/gitattributes

[guide:home]: https://opensource.guide
[guide:communities]: https://opensource.guide/building-community/
[guide:leadership]: https://opensource.guide/leadership-and-governance/
[guide:code-of-conduct]: https://opensource.guide/code-of-conduct/
[guide:legal]: https://opensource.guide/legal/
[guide:contribute]: https://opensource.guide/how-to-contribute/

[src:.gitignore]: .gitignore
[src:.gitattributes]: .gitattributes
[src:readme.md]: README.md
[src:license.md]: LICENSE.md
[src:contributing.md]: docs/CONTRIBUTING.md
[src:support.md]: docs/SUPPORT.md
[src:pull-request-template.md]: docs/pull_request_template.md

[anchor:why-are-they-important]: #why-are-they-important
[anchor:what-about-git-files]: #what-about-git-files

[app:pull]: https://wei.github.io/pull/

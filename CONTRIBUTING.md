# Contributing

Do you want to contribute? This page will help you along the way!

## The obvious info that no one reads

When contributing to open source projects, we need to care about
ourselfs and the people around! If you not sure about what I'm
saying, consider reading our [CODE OF CONDUCT].

[CODE OF CONDUCT]: CODE_OF_CONDUCT.md

## Branches and tags

Before start contributing, you need to know about this projects git
tree. There are:

- branches
- tags
- releases

### 1. Branch doc

We have only one branch ([main](https://github.com/nasccped/dwm-fulltag-indicator)).
It's responsible for project guidelines (no code here)!

### 2. tags

There's two kind of tags:

1. base:

    The entrypoint for feature implementation. Consider the base branch
    as the source minimal setup (default source code + usefull patches
    before feat. building). It's usefull when the feature synergizes
    with other patches but this last aren't intendet to by added to the
    feat. itself.

    All base tags should have the following name format:

    ```txt
    base-<DWM_VERSION>
    ```

    ie, the latest base tag was `base-6.5` (built under `6.5` DWM version).

2. _"feature implementation"_:

    The finished feature implementation. This tag should be built
    under it's respective `base` tag, ie:

    ```txt
    base tag: base-6.5
    feat tag: dwm-fulltagindicator-6.5.x
    ```

    Where `x` corresponds to the patch version.

### Releases

All releases are built from a **feature tag**. It will contain:
- A relatively short description ( + `bug fixes` and
  `feat. implementations`)
- The feature diff file

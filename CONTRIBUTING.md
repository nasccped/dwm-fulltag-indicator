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
    with other patches but this last aren't intended to by added to the
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

### 3. Releases

All releases are built from a **feature tag**. It will contain:
- A relatively short description ( + `bug fixes` and
  `feat. implementations`)
- The feature diff file

## Build a base tag

To contribute with a base tag, keep in mind that the dwm source
version should be different from all available base tags (otherwise,
it means duplicate base tags).

### Branch prepare

To push a base tag you'll certainly need to clone the source from a
official repository. Here's how:

1. fork this repository
2. clone your forked repo:
```sh
# the command bellow consider that you have not changed the repo name
git clone git@github.com:<your_username>/dwm-fulltag-indicator && \
cd dwm-fulltag-indicator
```
3. create a new empty base branch:
```sh
# checkout to branch + remove all files
git checkout --orphan base-<version> && \
git rm -rf .
```
4. clone the source code by:
    - adding remote url:
    ```sh
    git remote add sourcerepo <source_link>
    ```
    - fetching content:
    ```sh
    git fetch sourcerepo
    ```
    - checkout to source file tree
    ```sh
    git checkout sourcerepo/main -- .
    ```
    - run the init commit:
    ```sh
    git commit -m "chore: initial commit"
    ```
5. add patches that you think usefull (not intended to be added to
   the final release)

## Build a release tag

All release tags should be built under it's respective base tag (ie,
build release `6.5` from `base-6.5`):

1. clone the base tag:
```sh
git fetch base-<version>
# or the command bellow to fetch all tags
# git fetch --tags
```
2. checkout to base tag:
```sh
git checkout tags/base-<version>
```
3. create a new branch for release impl:
```sh
git checkout -b tags/dwm-fulltagindicator-<base_version>-1
```
4. do all the code stuff
5. add your changes and commit:
```sh
git add <changed_or_new_files> && git commit -m "changes message"
```

> [!IMPORTANT]
>
> Before contributing, make sure that your code compiles
> (`rm config.h -f && sudo make clean install`) and it does what it's
> supposed to do!

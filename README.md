<h1 align='center'>

![DWM Logo](dwm.png)

Full Tag Indicator Patch

</h1>

A **DWM patch** that mimics the [activetagindicatorbar patch].

[activetagindicatorbar patch]: https://dwm.suckless.org/patches/activetagindicatorbar/

> [!CAUTION]
>
> This isn't the original README file and project _(it's just for
> issue/PR tracking, instead...)_. You can find them at
> [README.old.txt] and the [official dwm repo], respectively!

[README.old.txt]: README.old.txt
[official dwm repo]: https://git.suckless.org/dwm

Table of contents
-----------------

1. [What and why]
2. [Install]
    - [Version]
3. [Tips]
4. [Customization]
5. [Contributors]

[What and why]: #what-and-why
[Tags Changelog]: #tags-changelog
[Install]: #install
[Version]: #version
[Tips]: #tips
[Customization]: #customization
[Contributors]: #contributors

> [!WARNING]
>
> All this doc is related to the latest patch version (`6.5.1`)!

What and why
------------

This project is based on the [activetagindicatorbar patch], which
looks like this:

<div align='center'>

![activetagindicatorbar image sample](activetagindicatorbar.png)

</div>

[activetagindicatorbar patch]: https://dwm.suckless.org/patches/activetagindicatorbar/

It's a cool way to personalize the occupied monitor but it fails in
terms of customization:

- [ ] Customize bar height
- [ ] Customize bar color
- [ ] Customize bar border
- [ ] Customize bar padding _(from tag sides)_

So, I've decided to implement all of these features, turning vanilla
**DWM** into a more _'[riceable]'_ environment!

[riceable]: https://www.reddit.com/r/unixporn/comments/45l5if/what_is_the_etymology_of_the_word_rice/

Then, the default patch implementation will looks like this: _(take a
look to [customization])_

<div align='center'>

![patch feature image](default-patch.jpg)

</div>

[customization]: #customization

Install
-------

Before diving deep into the install steps, we need to take a look at
dwm/patches versions and it's importance!

### Version

By reading the [suckless hacking page] _(which provides a ton of
contribution guides)_, we find the following mention:

[suckless hacking page]: https://suckless.org/hacking/

> For release versions:
>
> > toolname-patchname-RELEASE.diff
> > dwm-allyourbase-6.1.diff
>
> The RELEASE should correspond to the tool release version, ie 6.1
> for dwm-6.1.

Basically, there are a lot of versions for DWM software, but this
patch was built under the `6.5` version. Applying this patch to a
smaller version can cause **(compile/run)time errors**.

#### Which major/minor version should I use?

To avoid merge conflicts and unexpected bugs, you must always choose
like:

| Your DWM version            | Patch version |
| :-------------------------: | :-----------: |
| `6.5`                       | `6.5.x`       |
| `6.6` (for future versions) | `6.6.x`       |
| `...`                       | `...`         |

#### How can I know my DWM version?

Just run this command:

```sh
dwm -v
```

It will print something like `dwm-6.4`. So, the number following
`"dwm"` is your dwm version.

#### Which revision/patch version should I use?

If there's different patches for the same dwm version (like `6.5.1`,
`6.5.2`, `...`) it probably means a `bug-fix` or
`feature implementation`. You should read the page of the given
release.

#### About major/minor versions (before installing)

Some major/minor version can be missing (ie latest dwm version is
`6.6` but latest patch version is `6.5.x`). This means:

- `A)` The updated patch version has not been built/pushed yet
- `B)` There are no changes in the source code that justify an
       update in the patch implementation.

> [!TIP]
>
> I strongly recommend to always consider the `A` option before
> adding this patch.
>
> All update changelog will be disposed at the release page.

You can also create a backup of your current dwm setup before
patching.

You can do this with:

1. dir. copying:
```sh
cp path/to/your/DWM-SETUP ./DWM-SETUP.bak
```

2. tar:
```sh
tar -cvf dwm.bak.tar path/to/your/DWM-SETUP/
```

Tips
----

_Lorem..._

Customization
-------------

_Lorem..._

Contributors
------------

> [!TIP]
>
> If you have contributed with this project in any way, consider
> opening an [issue] with the **"Be a contributor"** template!

[issue]: https://github.com/nasccped/dwm-fulltag-indicator/issues

- Owners:
    - [nasccped](https://github.com/nasccped)
- Contributors:

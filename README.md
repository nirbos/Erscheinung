<p align="center">
  <picture>
    <source srcset=".github/erscheinung-logo.svg">
    <img src=".github/erscheinung-logo.svg" width="160" height="160" alt="Erscheinung">
  </picture>
    <br>
    <strong><i>Erscheinung</i></strong>
</p>

_Erscheinung_ is an open source theme for [Zettlr](https://github.com/Zettlr/Zettlr) that is being developed for all currently supported operating systems (Gnu/Linux, macOS, Windows).

The focus of _Erscheinung_ is currently on the dark theme, but a light theme is planned for the future. All the groundwork has already been laid, but it is not yet ready for use.

## Using _Erscheinung_

0. Please make shure that you use the dark theme. _Erscheinung_ currently only works this way.
1. Choose the css file depending on your OS (GNU/Linux, macOS, Windows), open it and copy all the contents.
2. After that open Zettlr, open the Assets Manager, choose Custom CSS.
3. If there is something, remove it first. Then paste all the code and save it.

## Development

### Building _Erscheinung_

_Erscheinung_ is written to be used with a preprocessor called SASS. [You can get it here](https://sass-lang.com/).

If you want to build the _Erscheinung_ theme yourself you first have to choose your way of installing `SASS` on your system and [install it](https://sass-lang.com/install/).

In these instructions, I assume that you have installed the command line version. If you have installed `SASS` for the command line you can - starting from the root of the project - use, depending on your operating system:

```
sass --no-source-map src/erscheinung.gnulinux.scss erscheinung.gnulinux.css    , or
sass --no-source-map src/erscheinung.macos.scss erscheinung.macos.css          , or
sass --no-source-map src/erscheinung.windows.scss erscheinung.windows.css
```

Or, if you want to compile all of the files at once you can use:

```
sass --no-source-map src/erscheinung.gnulinux.scss:erscheinung.gnulinux.css src/erscheinung.macos.scss:erscheinung.macos.css src/erscheinung.windows.scss:erscheinung.windows.css
```

### Customization

I would love you to use _Erscheinung_ and further extend or customize it to your needs.

Within the src-folder you will find the `src/areas`- and the `src/assets`- and the `src/os`-folder.
If you want to change colors, you can change them within the `src/assets` folder.
If you want to change more than colors, have a look in the `src/areas`- and `src/os`-folder. You can find many files there that belong roughly to the corresponding areas of the program. Pick the one you want to change and start your magic.

Some of these areas need special love depending on your OS. The files within the `src/os`-folder extend/overwrite the files in `src/areas`.

As described in the Building _Erscheinung_ chapter, you must use `SASS` to process the files. However, I recommend that you use a slightly modified version of the console command while editing. This will recreate the files every time you save `SASS` files.

```
sass --watch --no-source-map src/erscheinung.gnulinux.scss:erscheinung.gnulinux.css src/erscheinung.macos.scss:erscheinung.macos.css src/erscheinung.windows.scss:erscheinung.windows.css
```

### Further development of _Erscheinung_

I don't have a specific time when I work on it, I tinker with it as I use it. Please understand that there are some areas that I haven't customized yet - because I haven't used them yet - and also that I don't have a set timeline for doing that.

### Contribute to _Erscheinung_

That would be awesome, thank you!
_Erscheinung_ is open for contributions. If you have found bugs, or areas that do need more care, then go for it!

I use [Prettier](https://prettier.io/) for code formatting.

Please make your pullrequests one topic at a time and as small as possible. I will not accept pullrequests containing hundreds of lines of code spread over multiple topics.

## Known issues

- It seems to me there is currently a bug in the tab-area when many files are opened and the user is clicking the scroll buttons. The window itself breaks and part of the window is not usable anymore. Due to changes to the tab-area this bug is getting a bit worse.

## Todo

There is still a lot to do.

- Preview Overlay
- Embed ````
- Embedded files?
- Filter no result view
- File-Tree extended
- Text Search
  - Text Search Folder Overlay
- Buttons (Image Embed)
- Tag Cloud
- Toolbar buttons active
- Toolbar
  - Export
  - Comments
  - Timer thingy inputs
- Editor
  - Links
  - Images
  - Search and Replace
- Right Bar
  - Table of contents
  - Literature
  - Files
  - Other files
- Statusbar
  - Console
- Readabillity scores and colors
- Marked Text Overlay Bar
- Lint Warnings Overlay
- Renaming files
- Scrollbars in macOS buggy
- Properties on File Tree items
- More Statistics
  - Calendar
  - Charts
  - FSAL-Stats
  - Graph

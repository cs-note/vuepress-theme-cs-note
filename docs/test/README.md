---
title: test
---
Features
===

Introduction
===
<i class="fa fa-file-text"></i> **HackMD** is a realtime, multi-platform collaborative markdown note editor.
This means that you can write notes with other people on your **desktop**, **tablet** or even on the **phone**.
You can sign-in via multiple auth providers like **Facebook**, **Twitter**, **GitHub** and many more on the [_homepage_](/).

**Thank you very much!**

Workspace
===
## Modes
**Desktop & Tablet**

<i class="fa fa-edit fa-fw"></i> Edit: See only the editor.
<i class="fa fa-eye fa-fw"></i> View: See only the result.
<i class="fa fa-columns fa-fw"></i> Both: See both in split view.

**Mobile**

<i class="fa fa-toggle-on fa-fw"></i> View: See only the result.
<i class="fa fa-toggle-off fa-fw"></i> Edit: See only the editor.

## Image Upload:
You can upload an image simply by clicking on the camera button <i class="fa fa-camera"></i>.
Alternatively, you can **drag-n-drop** an image into the editor. Even **pasting** images is possible!
This will automatically upload the image to **[imgur](http://imgur.com)**, nothing to worry. :tada:
![](https://i.imgur.com/9cgQVqD.png)

## Share Notes:
If you want to share an **editable** note, just copy the URL.
If you want to share a **read-only** note, simply press publish button <i class="fa fa-share-square-o"></i> and copy the URL.

## Save a Note:
Currently, you can save to **Dropbox** <i class="fa fa-dropbox"></i> or save an `.md` file <i class="fa fa-file-text"></i> locally.

## Import Notes:
Similarly to the _save_ feature, you can also import an `.md` file from **Dropbox** <i class="fa fa-dropbox"></i>,
or import content from your **clipboard** <i class="fa fa-clipboard"></i>, and that can parse some **html** which might be useful :smiley:

## Permissions:
It is possible to change the access permission to a note through the little button on the top right of the view.
There are six possible options:

|                              |Owner read/write|Signed-in read|Signed-in write|Guest read|Guest write|
|:-----------------------------|:--------------:|:------------:|:-------------:|:--------:|:---------:|
|<span class="text-nowrap"><i class="fa fa-leaf fa-fw"></i> **Freely**</span>               |✔|✔|✔|✔|✔|
|<span class="text-nowrap"><i class="fa fa-pencil fa-fw"></i> **Editable**</span>           |✔|✔|✔|✔|✖|
|<span class="text-nowrap"><i class="fa fa-id-card fa-fw"></i> **Limited**</span>           |✔|✔|✔|✖|✖|
|<span class="text-nowrap"><i class="fa fa-lock fa-fw"></i> **Locked**</span>               |✔|✔|✖|✔|✖|
|<span class="text-nowrap"><i class="fa fa-umbrella fa-fw"></i> **Protected**</span>        |✔|✔|✖|✖|✖|
|<span class="text-nowrap"><i class="fa fa-hand-stop-o fa-fw"></i> **Private**</span>       |✔|✖|✖|✖|✖|


**Only the owner of the note can change the note's permissions.**

## Embed a Note:
Notes can be embedded as follows:

```xml
<iframe width="100%" height="500" src="https://hackmd.io/features" frameborder="0"></iframe>
```

View
===
## Table of Contents:
You can look at the bottom right section of the view area, there is a _ToC_ button <i class="fa fa-bars"></i>.
Pressing that button will show you a current _Table of Contents_, and will highlight which section you're at.
ToCs support up to **three header levels**.

## Permalink
Every header will automatically add a permalink on the right side.
You can hover and click <i class="fa fa-chain"></i> to anchor on it.

Edit:
===
## Shortcut Keys:
Just like Sublime text, which is pretty quick and convenient.
> For more infomation, see [here](https://codemirror.net/demo/sublime.html).

## Auto-Complete:
This editor provides full auto-complete hints in markdown.
- Emojis: type `:` to show hints.
- Code blocks: type ` ``` ` and plus a character to show hint. <i hidden>```</i>
- Headers: type `#` to show hint.
- Referrals: type `[]` to show hint.
- Externals: type `{}` to show hint.
- Images: type `!` to show hint.

## Title:
This will take the first **level 1 header** as the note title.

## Tags:
Using tags as follows, the specified tags will show in your **history**.
###### tags: `features` `cool` `updated`

## [YAML Metadata](/yaml-metadata)
You can provide advanced note information to set the browser behavior (visit above link for details):
- title: set note title
- description: set note description
- image: set note default image (for link preview)
- tags: set note tags
- robots: set web robots meta
- lang: set browser language
- dir: set text direction
- breaks: set to use line breaks
- GA: set to use Google Analytics
- disqus: set to use Disqus
- slideOptions: setup slide mode options

## ToC:
Use the syntax `[TOC]` to embed table of content into your note.

[TOC]

## Emoji
You can type any emoji like this :smile: :smiley: :cry: :wink:
> See full emoji list [here](http://www.emoji-cheat-sheet.com/).

## ToDo List:
- [ ] ToDos
  - [x] Buy some salad
  - [ ] Brush teeth
  - [x] Drink some water

## Code Block:
We support many programming languages, use the auto complete function to see the entire list.
```javascript=
var s = "JavaScript syntax highlighting";
alert(s);
function $initHighlight(block, cls) {
  try {
    if (cls.search(/\bno\-highlight\b/) != -1)


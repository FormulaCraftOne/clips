# How to add clips

## Minimal Instruction

You only need two things:
1. Any public link to a mp4 clip. GitHub releases is great for hosting large files publicly so the instructions uses that, but you can host it anywhere.
2. A `<uniquename>.md` file in the `docs/_clips` folder of the docs branch, with the following frontmatter accordingly filled-in (or follow the examples of the existing files in there):

```
---
layout: video
src: "url-to-mp4-file"
width: "video-width-in-px"
height: "video-height-in-px"
title: "title-of-the-clip--this-line-is-optional"
description: "description-for-the-clip--this-line-is-optional"
---
```

Whatever you put underneath the frontmatter will also be included in the page as raw html.

Once committed to the docs branch, the Jekyll page will build and your clip will be available at `https://formulacraftone.github.io/clips/<uniquename>` and a link to it will be listed at `https://formulacraftone.gitub.io/clips`

Do please make sure your created filename is unique, or you'll overwrite the existing file with the same name.

## Detailed Instruction (using this repo's Releases)

### Step 1 - upload mp4 to releases
- go to https://github.com/FormulaCraftOne/clips/releases/new
- click on the "Choose a tag" drop-down, type in or select your desired tag. Click "create a new tag" if it did not exist. If a release for the tag already exists, click "edit the existing notes" to edit the existing release.
- upload your mp4 file to the attachment box.
- (optional) check the "set as pre-release" box to keep the page tidy.
- in the published release, right-click the attachment and copy the target link to the mp4.

### Step 2 - create a clips entry
- go to https://github.com/FormulaCraftOne/clips/tree/docs/docs/_clips
- click on the "Add file" dropdown and select "Create new file".
- at the "Name your file..." field, put in a unique filename followed by `.md` (a quick way to get a short and likely-unique random filename is copying the 7-digit hex of the most recent commit), for example `d69fd20.md`
- fill in the frontmatter as described in the [Minimal Instructions](#minimal-instructions) section, with the src field being the link to your mp4 file attached in step 1.
- Click "Commit changes...", make sure that it's committing to the `docs` branch, and click "Commit Changes" to confirm.

Wait for GitHub to finish rebuilding the website, you will see that it has completed when a green checkmark appears next to the most recent commit in the docs branch. Your clip will now be available at `https://formulacraftone.github.io/clips/<uniquename>` where `<uniquename>` is the filename (without the .md part) you specified in step 2.

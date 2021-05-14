---
title: Editing the Wiki
section: Help:Editing the Wiki
---

This page explains how to write and edit wiki pages. The simplest way to create
or modify a page is using GitHub's online file editor. Each page has an "Edit
page" link at the top right with a direct link to this interface.

{% include tech content="Advanced users can make edits via a local installation of jekyll and a local clone of the site repository; see the [advanced editing guide](/help/editing/advanced) for setup instructions." %}

# Creating a new page

Let's dive in to how to create a new page on the site.
If you are looking to edit an existing page, skip to
[adding and editing page content](#adding-and-editing-page-content) below.

1.  Navigate to the
    [pages section](https://github.com/imagej/imagej.github.io/tree/main/_pages)
    of the repository.
    Click {% include button label="Add file" %} then
    {% include button label="Create new file" %} from the drop-down:

    {% include img align="center" name="create-page" src="/media/help/create-page-etw.png" %}

2.  Add a name for your file. **Note: this is not the page title;** the page
    title will be applied in the next section, front matter. File names should
    be all lower case, use the file extension `.md`, avoid symbols and spaces,
    and separate words using dashes (`-`):

    {% include img align="center" name="name-your-file" src="/media/help/name-your-file.png" classes="grey-border" %}

## Front matter

Every page begins with a block of *front matter*: a sequence of parameters that
configure your page. Without the front matter, your page will not render
correctly. The following tables lists front matter fields you can use:

|       **Field** | **Purpose** |
|----------------:|:------------|
|       **title** | The title of your page. This is the only required field. |
| **description** | A short description of your page. Also used for the site's search engine. When omitted, the first sentence of the page content is used. |
|     **section** | Main menu section that should be open when this page first loads, if any. Nested sections to expand should be separated by colons (`:`). For example, this page's section is `Help:Editing the Wiki`. |
|  **categories** | List of categories to which the page belongs. Must be enclosed in square brackets (`[` and `]`). |
|       *statbox* | The "Vital statistics" sidebar supports quite a few fields; see [this comment](https://github.com/imagej/imagej.github.io/blob/main/_includes/statbox#L30-L72) for a list. Including at least one of these fields will cause the statbox to appear; otherwise, there will be no statbox for the page. |

Below is a minimal example front matter block. You can copy and paste this code
into the editor of a new page (see above). Replace `My Awesome Page` with the
title for the new page.

```
---
title: My Awesome Page
---
```

# Adding and editing page content

Pages on this site are optimized to be written in git markdown, but will also
read `html` syntax. This section will cover how to populate the *content* of
your page, including: links to GitHub markdown resources, as well as guides on
how to use this site's includes.

## Markdown

{% include wikipedia title="Markdown" %} is plain-text syntax formatting,
allowing you to easily and cleanly modify text with italics, bold, ordered
or bulleted lists, etc. As a GitHub Pages hosted website, this wiki uses
[GitHub Flavored Markdown](https://github.github.com/gfm/) (GFM).
A basic GFM guide can be found
[here](https://guides.github.com/features/mastering-markdown/).

## Using includes

*Includes* provide more robust formatting options and are unique to this site
(think of this as: "I would like to *include* an image," etc). With includes,
you can insert menus, images, tables, sideboxes, figures, math, warnings, etc
with pre-formatted settings into a page. For a full list of includes with
utilization instructions, [see below](/help/editing#available-includes).

### Available includes

#### Linking

| Include                           | Purpose                      |
|:---------------------------------:|:-----------------------------:
| [github](linking#github)          | Link to a resource on GitHub |
| [javadoc](linking#javadoc)        | Link to a javadoc resource   |
| [wikipedia](linking#wikipedia)    | Link to a Wikipedia page     |
| [person](people)                  | Link to a person's user page |
| [person-list](people#lists)       | Link to a list of user pages |

big-link

#### Symbols

| Include                           | Purpose                      |
|:---------------------------------:|:-----------------------------:
| [bc](menu-paths)                  | Insert a menu breadcrumb     |
| [button](buttons)                 | Insert a button              |
| [key](keys)                       | Insert a keyboard shortcut   |
| [logo](logos)                     | Insert logos                 |
| [math](math)                      | Insert math                  |
| [symbol](symbols)                 | Insert a symbol              |

arrow
yes
no

#### Media

| [figure](images#figures)                     | Insert a figure              |
| [gallery](images#image-galleries)            | Insert an image gallery      |
| [img](images#images)                         | Insert an image              |
| [youtube](videos#youtube)                    | Embed a YouTube video        |
| [youtube-playlist](videos#youtube-playlists) | Embed a playlist of videos |

#### Blocks

| [notice](notices)                 | Insert a notice              |
| [table](tables)                   | Insert a table               |
| [sidebox](sideboxes)              | Insert a sidebox             |

ambox
info-box
box
biginfo-box
sidebox-left
sidebox-right
tech-box
tip
minibox
warning-box

#### Other

| [citation](citations)             | Insert a citation            |
| [conference](conferences)         | Insert conference info       |

#### Internal

listnews
hamburger-menu
main-menu
menu-divider
menu-item
menu-section
menu-section-end

avoidprogramfiles
base-scripts
bc
book
cip
citation
cite
clear
communication
downloadfiji
example
extendingtrackmatetutorials
fiji
file
fullpagename
fullurl
github
github-embed
guidetask
ides
imagej1
imglib1-deprecation-info-box
importing-classes
license-links
linux
list-of-update-sites
logo
macos
matlab
maven
onebox-info
outdated
page-info
path
person
person-list
plugin-index-icon
plugin-index-section
pluginremoved
project
publication
quiz
recommendedcontact
scholar
search-results
sntdeprecation
sntnavbar
statbox
statbox-row
statbox-team-members
stub
tech
template
testimonial
thumbnail
thumbnail-link
timeline
tooltip
top-bar
unmaintained
unreleased
updatesiteswarning-box
windows
wip

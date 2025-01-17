---
switcher-label: Device
---

# How do I contribute?

It takes a little effort to get started, but once you do, it's fairly easy to make changes to the site.

## Part 0: Terminology

This is very important to know, as a lot of these words will be used throughout the page.

Repository
: A place where code is put.
One can be created at any time, for any purpose, for free.

Git
: A source control framework.
Usually used for updating repositories, and is the backend of GitHub.

GitHub (GH)
: Frontend for Git & Repositories.

Github Pages
: A way to host free sites on GitHub. It's what we're using right now.

Branch
: A repository usually has one, two, or any amount of Branches.
Each one stores different code, but all must have some similar base to be useful.
Can be used for testing versions, higher major releases, etc.

Commit
: A change to a branch, whether local or online.

Push
: Push a change to a remote branch.
For example, you commit to a local clone of a repository, then push that commit to the origin so everyone else now has it.

Fetch
: Looks at what commits have been made and compares it to your local clone.

Pull
: Amends all changes from the target branch to your local clone.

Fork
: A fork is someone's own repository, pulled from another.
It's under the working of the forker, not the original maintainer.
Can be used for Pull Requests

Pull Request
: A request to merge a branch / fork back into the main repository.
Must be reviewed by the original maintainers and slowly worked through until it all is fine, and then merging is available.
Pull Requests can only be merged if the target and higher branch have commonalities and no conflicts.

Conflicts
: Problems with the merging process that would result in weird files are relayed to the maintainer before merging is available.
Must be fixed if at all possible.

Merging
: Commits from the higher fork / branch are made to the target branch.

## Part 1: Initial Setup

### 1.1: The Universal Things

<procedure>

For everyone, go to [GitHub](https://github.com) and make yourself an account.
If you already have one, just use that.

Afterward, go to [the repository](https://github.com/Interval0043/KTE-MD-Docs), and click the `Fork` button at the top.
You don't have to change the name, then just hit `Create Fork`.

> You only need to make one fork. It can be pull requested as many times as you need.
> {style=note}

</procedure>

### 1.2: Not-so-Universal

Select which device you have at the top, and which method below.
If you don't know what they mean, just go with anything labelled `Desktop GUI`.

#### iOS Setup {switcher-key="iPhone / iPad (iOS)"}



#### Windows Setup {switcher-key="Computer (Windows)"}

<tabs>

<tab id="windg1" title="Desktop GUI" group-key="dgui">
<procedure>
<step>

Go to [Github Desktop](https://desktop.github.com/download), and get it.
</step>
<step>
Sign into GH Desktop, and clone the repository from your list.
</step>
<step>

Go to [Visual Studio Code](https://code.visualstudio.com/download), and get it.
</step>
<step>
No need to sign into anything in VS Code. Just run the installer and get it set up.
</step>
<step>

Once that's done, head back into GH Desktop, and go to `Settings > Integrations`, making sure to set the Editor to `Visual Studio Code`
</step>
<step>

Fetch and Pull the repository.
</step>
<step>

Either press <shortcut>Ctrl+Shift+A</shortcut>, or click the button on the home screen to open the repository in VS Code.
</step>
</procedure>

</tab>
<tab id="wing1" title="VS Code GUI">

If you're against using GH desktop for whatever reason, then you can only use VS Code for editing the pages.
I don't advise it, however, since commits and pushes are a little worse through VS Code.

I'll finish this part later.

</tab>
</tabs>

<!-- #### Debian / Debian-Based Setup {switcher-key="Computer (Debian / Debian-Based)}

This is if you aren't against package systems.
I know how linux users can be, and I'm only writing documentation for Debian Distributions.
Sorry Arch users, but I don't care.
I'm also only writing for a GUI.
Someone else can handle the CLI instructions.

<tabs>
<tab id="debfg1" title = "Flatpak + APT GUI" group-key="debfg">
<procedure>
<step>

Hit <shortcut>Ctrl+Alt+T</shortcut> to open a terminal  
</step>
<step>

Type `sudo apt install code`
</step>
</tab>
</tabs> -->

### 1.3: Congratulations!

And, you've done the worst part of it already.
Granted the whole "opening the git app" is going to happen every time, but still, you've got the initial setup down which you shouldn't have to do again.

## Part 2: Editing

<note>

Here are some things to note.

* All files must end with the `.md` file extension
* Each filename must be unique.
* Each file needs a top-level heading.

All of this will be explained later in the guide.
</note>

### 2.1: Code Overview

Most of this is written in two very similar languages: Markdown (MD) and Semantic Markup (SM).
A snippet of this is below, this is actually the top part of this page.

```markdown
### 1.1: The Universal Things

<procedure>

For everyone, go to [GitHub](https://github.com) and make yourself an account.
If you already have one, just use that.

Afterward, go to [the repository](https://github.com/Interval0043/KTE-MD-Docs), and click the `Fork` button at the top.
You don't have to change the name, then just hit `Create Fork`.

> You only need to make one fork. It can be pull requested as many times as you need.
{style=note}

</procedure>

```

Let's take this line-by-line to examine what this is.
You might recognize some things, like the first line being a level-3 heading, if you're familiar with Discord's Markdown.
MD supports 6 heading levels, though.

The tags, being `<procedure>...</procedure>` is Semantic Markup, with its own tag system.
Each tag needs an opening and a closing for it to function.

Line breaks are very important, none of these aren't there just for fun.
In order for MD and SM to play nice, there must be a one-line gap between the tag and all other MD content.
Shown below is what would happen if line 4 was removed (which is the whitespace between the tag and the text).

<procedure>

![An image of improper Markdown & Semantic Markup usage.](Screenshot 2025-01-16 203613.png)
</procedure>

Note that the link in the first part of the `procedure` block is non-functional, but the rest is.
Whitespace is very important.
It's also what separates paragraphs, a more obvious example is this block, which is the entire piece between the prior code-block to right here.

```markdown
Let's take this line-by-line to examine what this is.
You might recognize some things, like the first line being a level-3 heading, if you're familiar with Discord's Markdown.
MD supports 6 heading levels, though.

The tags, being `<procedure>...</procedure>` is Semantic Markup, with its own tag system.
Each tag needs an opening and a closing for it to function.

Line breaks are very important, none of these aren't there just for fun.
In order for MD and SM to play nice, there must be a one-line gap between the tag and all other MD content.
Shown below is what would happen if line 4 was removed (which is the whitespace between the tag and the text).

![An image of improper Markdown & Semantic Markup usage.](Screenshot 2025-01-16 203613.png)

Note that the link in the first part of the `procedure` block is non-functional, but the rest is.
Whitespace is very important.
It's also what separates paragraphs, a more obvious example is this block, which is the entire piece between the prior code-block to right here.
```

Each new paragraph is separated well, which is absolutely required for it to not become a word salad.
Also, only full whitespace makes a new paragraph.
Hitting Enter once won't do it, I do that so it doesn't turn into one gigantic line for every paragraph.

### 2.2: The Table of Contents

> The TOC is a very crucial thing, it's the thing on the left (or at the top hamburger menu if you're on mobile).
> Make sure not to mess it up completely.
> {style="note"}

#### 2.2a: Compiler Jank

Each entry has its own name, but that's NOT its filename.

Just make sure they're unique and end with `.md`.
For the two people who don't know, that's a file extension, and it tells Writerside, and every other programming program what the file even is, and how to interpret it.

But, the TOC entry is dictated from the file's initial heading.
The page you're reading right now has a filename of `Development.md`, but has a top-level heading of `# How do I contribute?`.
The compiler will reject a file if it doesn't have this heading, so it MUST be at the top.

#### 2.2b: The TREE.

There is a file in the root of the repository called `kte.tree`.
You will become very acquainted with it, very soon. 
Since neither programs I've given are JetBrains Writerside, editing this one file is the only way to add TOC entries for y'all.

There's a good reason why I went over tags briefly in 2.1, because it's going to be very important here too. The tree consists of whatever this is.
```xml
        <toc-element topic="OC-List.md">
            <toc-element topic="Aether.md"/>
            <toc-element topic="Coded.md"/>
            <toc-element topic="Ebony.md"/>
            <toc-element topic="Gympie.md"/>
            <toc-element topic="Helios.md"/>
            <toc-element topic="Isa.md"/>
            <toc-element topic="Kallisto.md"/>
            <toc-element topic="Levi.md"/>
            <toc-element topic="Lilac.md"/>
            <toc-element topic="Ruby.md"/>
            <toc-element topic="Sapphire.md"/>
            <toc-element topic="Teegan.md"/>
            <toc-element topic="Viper.md"/>
        </toc-element>
```

> This is the abridged version of the tree, it's much longer than this.
> I will have the full version as a collapsible element.
> {style="note"}

> Do not touch any of the instance information, just the table of contents pieces.
> Yes, I review every single one of your changes, and I will call you out if you mess with anything but the TOC information.
> {style="warning"}

```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE instance-profile
        SYSTEM "https://resources.jetbrains.com/writerside/1.0/product-profile.dtd">

<instance-profile id="kte"
                  name="KTE"
                  start-page="starter-topic.md">

    <toc-element topic="starter-topic.md">
        <toc-element topic="OC-List.md">
            <toc-element topic="Aether.md"/>
            <toc-element topic="Coded.md"/>
            <toc-element topic="Ebony.md"/>
            <toc-element topic="Gympie.md"/>
            <toc-element topic="Helios.md"/>
            <toc-element topic="Isa.md"/>
            <toc-element topic="Kallisto.md"/>
            <toc-element topic="Levi.md"/>
            <toc-element topic="Lilac.md"/>
            <toc-element topic="Ruby.md"/>
            <toc-element topic="Sapphire.md"/>
            <toc-element topic="Teegan.md"/>
            <toc-element topic="Viper.md"/>
        </toc-element>
        <toc-element topic="Foundations.md">
            <toc-element topic="Factions.md">
                <toc-element topic="IADR.md"/>
            </toc-element>
            <toc-element topic="History.md"/>
            <toc-element topic="Species.md">
                <toc-element topic="Code-Shifter.md"/>
                <toc-element topic="Entreos.md"/>
                <toc-element topic="Frisk.md"/>
                <toc-element topic="Glitch.md"/>
                <toc-element topic="Hedron.md"/>
                <toc-element topic="Leith.md"/>
                <toc-element topic="Manifold.md"/>
                <toc-element topic="Protogen.md"/>
                <toc-element topic="Sprinklekit.md"/>
            </toc-element>
            <toc-element topic="Widespread-Species.md">
                <toc-element topic="Arachnid.md"/>
                <toc-element topic="Dinosaur.md"/>
                <toc-element topic="Dragon.md"/>
                <toc-element topic="Human.md"/>
                <toc-element topic="Insect.md"/>
            </toc-element>
            <toc-element topic="Theories.md">
                <toc-element topic="AltW.md"/>
                <toc-element topic="Limit.md"/>
                <toc-element topic="DimT.md"/>
                <toc-element topic="Format.md"/>
                <toc-element topic="HypCom.md"/>
            </toc-element>
            <toc-element topic="Things.md">
                <toc-element topic="ODR.md"/>
            </toc-element>
        </toc-element>
        <toc-element topic="Ramblings.md">
            <toc-element topic="Modifiers.md"/>
        </toc-element>
        <toc-element topic="Development.md"/>
    </toc-element>
</instance-profile>
```
{collapsible="true" collapsed-title="kte.tree"}

Categories for the TOC are formatted as `<toc-element topic="[insert filename without the brackets]">...</toc-element>`, 
but single entries without anything under them are formatted as `<toc-element topic="[insert filename without the brackets]"/>`.
Whenever you add a new file, put the single entry within the category you're looking to have it in, or make the new category if you so choose.
That's the beauty of collaboration.

### 2.3: Making Changes

#### iOS Edits {switcher-key="iPhone / iPad (iOS)"}

<!-- <procedure>

Beginning for a new file:

<step>

Go to `Writerside -> topics`
</step>
<step>

Click the pad icon in the top right, and hit `New File`.
Make sure the new file has a decent name, one that fits well.
</step>
<step>

Add its entry into `kte.tree`
</step>

In order to edit a file, click on the file you want to edit, and begin typing in accordance to MD & SM rules.
Typing on iOS is a little more difficult, but it's possible.
</procedure> -->

I need to update this, it'll be fixed later. Figure it out yourself for now.

#### Windows Edits {switcher-key="Computer (Windows)"}

<procedure>

Beginning for a new file:

<step>

Right click on the `topics` folder, and click `New File...`, name it whatever.
The name does not have to suit the file, but it's good practice to have it fit.
</step>
<step>

Give it a top level heading.
</step>
<step>

Add its entry into `kte.tree`.
</step>

For any existing files or new ones that you created, write as you need to.
Documentation is present [here](https://www.jetbrains.com/help/writerside/discover-writerside.html), under the `Markup` category.
</procedure>

### 2.4: Committing

The method to commits is a little different based on device, so once again we go to the whole top-of-the-page thing.

#### iOS Commits {switcher-key="iPhone / iPad (iOS)"}

<!-- <procedure>
<step>
Once you're done editing, hit the back arrow
</step>
<step>

Click the part at the bottom bar that says `Status`
</step>
<step>

Hit `Stage All`
</step>
<step>

Hit `Commit`
</step>

PolyGit has a maximum of 3 pushes per day on the free side of things, so only push any commits that you have to.
If you need any minor changes made and pushed, I or someone else could do that for you, if your pushes are up.

</procedure> -->

Same as before. Figure it out.

#### Windows Commits {switcher-key="Computer (Windows)"}

<procedure>
<step>
Open GH Desktop
</step>
<step>
Write the commit message as well as the summary, keep it brief and readable.
I'd like it to be helpful.
</step>
<step>
Hit "Commit", and then hit "Push".
Now, your changes will be in your forked repository.
</step>
</procedure>

### 2.5: Pull Requests

To submit a pull request, navigate to the main repository's GitHub page, and go to Pull Requests.
I'm not exactly sure how to do it at the moment, I'll figure it out with one of the other page maintainers and then put it here.

I will review the requests, send comments for the maintainer to change so they can, and then I'll merge it once it's ready.
If I need to, I'll clone the PR and preview it in Writerside, since while it's free now, there's no guarantees it'll be free later, but I'll pay for it so you don't have to.
Reason being, Writerside allows for live previews of what you're working on, as well as detailed error analysis.
If we're stuck, I'll step in, but this is a community project anyway.

## Part 3: Fruits of Your Labor

This page, after about two minutes will Build, Test, and Deploy once a change is pushed / merged.
Since there's no caching issues unlike the first test wiki, after it's done deploying, you can see your changes.

## Part 4: Conclusion

That just about does it, really.
This entire article is over 400 lines of SM & MD, and has taken roughly an hour to write.
But this is useful for everyone, so it's necessary.

I hope to see people contributing, and using this page so I don't have to manually send guides.

**-Interval**
---
layout: post
title: "How to get rid of the tab bar on firefox"
usemathjax: true
---
This is a post mainly for my reference, since I always seem to get a bit lost figuring out how to do this. Essentially, I prefer using a Firefox extension for a side tab bar (I use [Sidebery](https://addons.mozilla.org/en-US/firefox/addon/sidebery/)) and its shortcuts to manage my tabs. My browser setup looks a little bit like this:

![tabbar-ss](/media/tabbar/tabbar_ss.png)

While its pretty easy to add a tab manager extension, the annoying part was to figure out how to get rid of the tabs on top to make good use of the vertical real estate. I'll be documenting how to do that in a series of steps here!

---

I am currently running Firefox version 134.0.2, but it should still work for most previous versions of Firefox. If your Firefox version is _really_ old (pre 2019), I think you might get better mileage out of an older guide.

## Step 1: Choose your Tab Manager Alternative
It's better to activate your alternative tab bar manager before disabling the default tab bar. Personally, I use Sidebery, but alternative extensions exist that you can try.

## Step 2: Allowing Firefox Customization via Stylesheets
We will need to write a tiny bit of CSS to disable tabs, and so we need to inform Firefox to enable CSS customization. To do this:
1. Search `about:config` on Firefox. It may give you a warning, but proceed to the next page.
2. In the search bar, search for `toolkit.legacyUserProfileCustomizations.stylesheets`. When the field pops up, set it to `true`.

## Step 3: Hiding The Tab Bar via CSS
Now that Firefox accepts styles via CSS, we need to write the CSS and store it somewhere Firefox can easily find.

1. Search `about:support` on Firefox. Search for the words "Profile Folder" in the page.
2. You'll find a directory path next to "Profile Folder" that ends in something like `abcd1234.default-release`. Navigate to the directory using Finder/File Explorer/terminal
3. Create a new directory named `chrome` in that directory. In the `chrome` directory, create a file called `userChrome.css`. These names are case sensitive, so be careful. 
4. In `userChrome.css`, paste the following:
```
#tabbrowser-tabs {
    visibility: collapse;
}
#titlebar {
    max-height: 0px;
}
#TabsToolbar .titlebar-buttonbox-container {
    display: none;
}
```
and close the file.

---

On restarting your browser, you shouldn't be able to see the default Firefox tab bar! In case its still there, you'll have to Google around, because of version or platform differences. Thanks for reading!

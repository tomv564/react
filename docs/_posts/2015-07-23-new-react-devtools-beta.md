---
title: "New React Devtools Beta"
author: jaredly
---

We've made an entirely new version of the devtools, and we want you to try it
out!

![The full devtools gif](/react/img/blog/devtools-full.gif)

## Why entirely new?

Perhaps the biggest reason was to create a defined API for dealing with
internals, so that other tools could benefit as well and not have to depend on
implementation details. This gives us more freedom to refactor things
internally without worrying about breaking tooling.

The current version of the devtools is a fork of blink's "Elements" pane, and
is imperative, mutation-driven, and tightly integrated with chrome-specific
APIs. The new devtools are much less coupled to chrome, and easier to reason
about&mdash;thanks to React.

## What are the benefits?

- 100% react
- firefox compatible
- react-native compatible
- more extensible &amp; hackable

## Are there any new features?

Yeah!

### The Tree View

![The new tree view of the devtools](/react/img/blog/devtools-tree-view.png)

- Much richer view of your props, including the contents of objects and arrays
- Custom components are emphasized, native components are de-emphasized
- Stateful components have a red collapser
- Improved keyboard navigation (hjkl or arrow keys)
- Selected component is available in the console as `$r`
- Props that change highlight in green
- Right-click menu

  - Scroll node into view
  - Show the source for a component in the "Sources" pane
  - Show the element in the "Elements" pane

### Searching

Select the search bar (or press "/"), and start searching for a component by
name.

![](/react/img/blog/devtools-search.gif)

### The Side Pane

- Now shows the `context` for a component
- Right-click to store a prop/state value as a global variable

![](/react/img/blog/devtools-side-pane.gif)

## How do I install it?

For the beta, you need to [download the .crx](https://github.com/facebook/react-devtools/releases)
and drag it into your `chrome://extensions` page. You will also need to
disable the version you got from the chrome web store.

Once we've determined that there aren't any major regressions, we'll update
the official version, and everyone will be automatically upgraded.

Let us know what issues you run into [on github](https://github.com/facebook/react-devtools/issues), and check out [the Readme](https://github.com/facebook/react-devtools/tree/devtools-next) for more info.

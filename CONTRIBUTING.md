Thanks for helping build new.css! When contributing, here are the general guidelines to follow.

- Update the primary file `new.css` first. I like to comment inline how/why any changes are made, so please try to add a comment about what the change does and why it's helpful.
- To make `lite.css`, remove the font-face `@import` in the beginning.

And you're ready to submit! I'll publish a new version to npm when a numerical release seems needed, such as `1.0.2`.

jsDelivr generates minified versions such as `new.min.css` automatically.

Basic guide for release numbers-

**X.Y.Z**
- X updates when an older version introduces components that conflict with older ones, or something else is changed that will break compatibility with older elements/themes
- Y updates when new features or styles are added
- Z updates when there's a bug fix or very minor update, such as a typo
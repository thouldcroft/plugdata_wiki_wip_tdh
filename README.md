# plugdata documentation

## Building the documentation

[Honkit](https://github.com/honkit/honkit) is used to build static pages from the markdown. The format for multi-language books is used as described in the [Honkit documentation](https://honkit.netlify.app/).

Install honkit

`$ npm install honkit --save-dev`

Serve static pages for testing (from docs/):

`$ npx honkit serve`

Build static pages for production:

`$ npx honkit build`


## Style Guide

When writing plugdata documentation use the [Google Developer Documentation Style Guide](https://developers.google.com/style).

### Project specific style guide notes

plugdata is always written in lower case, even when it is at the beginning of a sentence.

Names of Pd objects and Pd specific terminology should be left untranslated.



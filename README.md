# anima-figma-sdk

An SDK for Figma plugins that need to convert Figma to HTML.

# Installation

```
npm install @animaapp/anima-figma-sdk
```

# Usage

## Hosted

To get a url of a Figma design converted to HTML with images hosted on s3 use `Target.Hosted`. Best for opening in a browser.

```
Import * as AnimaFigmaSDK from "@animaapp/anima-figma-sdk"
Import { Target, Options } from "@animaapp/anima-figma-sdk-types"

AnimaFigmaSDK.exportNodeAsHTML({ "target": Target.Hosted } as Options, (url: URL) => {
  // your success call back code
},
(error) => {
  // your failure call back code
});
```

## Inline

To get Figma design converted to HTML as a string with inline images as binaries use `Target.Inline`. Best for presenting in an iframe inside your Figma plugin.

```
Import * as AnimaFigmaSDK from "@animaapp/anima-figma-sdk"
Import { Target, Options } from "@animaapp/anima-figma-sdk-types"

AnimaFigmaSDK.exportNodeAsHTML({ "target": Target.Inline } as Options, (html: string) => {
  // your success call back code
},
(error) => {
  // your failure call back code
});

```

## Zip

To get a zip `Target.Zip`. Best for downloading a package that includes html, css, images, and fonts.

```
Import * as AnimaFigmaSDK from "@animaapp/anima-figma-sdk"
Import { Target, Options } from "@animaapp/anima-figma-sdk-types"

AnimaFigmaSDK.exportNodeAsHTML({ "target": Target.Zip } as Options, (zipUrl: URL) => {
  // your success call back code
},
(error) => {
  // your failure call back code
});

```



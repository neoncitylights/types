# neoncitylights/css-types

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square)](https://opensource.org/licenses/MIT)
[![NPM package](https://img.shields.io/npm/v/@neoncitylights/css-types?style=flat-square)](https://www.npmjs.com/package/@neoncitylights/css-types)

This library provides a set of utilities extending the `csstype` package to help you write typed CSS in TypeScript.

Currently, there's basic support for the following W3C standards:

 - **CSS Conditionals Level 3** (`css-conditional-3`): [Editor's Draft](https://drafts.csswg.org/css-conditional-3/), [CRS](https://www.w3.org/TR/css-conditional-3/)
 - **CSS Media Queries Level 5** (`mediaqueries-5`): [Editor's Draft](https://drafts.csswg.org/mediaqueries-5/), [WD](https://www.w3.org/TR/mediaqueries-5/)

## Install

```
npm install @neoncitylights/css-types
```

## Documentation

[Auto-generated API documentation is available](https://neoncitylights.github.io/css-types/).

### API reference
>
> **Note**: The public API below is an excerpt and shows the *main* symbols that a developer is likely to use.

 - `fn`: <a href="#cssSupports">#</a> **cssSupports**(*property*, *value*): *boolean* • [source](./src/cssSupports.ts), [docs](https://neoncitylights.github.io/css-types/types/cssSupports.html)
 - `fn`: <a href="#matchMediaFeature">#</a> **matchMediaFeature**(*mediaFeature*, *value*): MediaQueryList • [source](./src/matchMedia.ts), [docs](https://neoncitylights.github.io/css-types/types/matchMediaFeature.html)
 - `T`: <a href="#CSSProperty">#</a> cssSupports.**CSSProperty** • [source](./src/cssSupports.ts), [docs](https://neoncitylights.github.io/css-types/types/CSSProperty.html)
 - `T`: <a href="#CSSPropertyValue">#</a> cssSupports.**CSSPropertyValue** • [source](./src/cssSupports.ts), [docs](https://neoncitylights.github.io/css-types/types/CSSPropertyValue.html)
 - `T`: <a href="#MqFeature">#</a> matchMedia.**MqFeature** • [source](./src/matchMedia.ts), [docs](https://neoncitylights.github.io/css-types/types/MqFeature.html)
 - `T`: <a href="#MqFeatureValue">#</a> matchMedia.**MqFeatureValue** • [source](./src/matchMedia.ts), [docs](https://neoncitylights.github.io/css-types/types/MqFeatureValue.html)
 - `I`: <a href="#MediaQueries">#</a> matchMedia.**MediaQueries** • [source](./src/matchMedia.ts), [docs](https://neoncitylights.github.io/css-types/types/MediaQueries.html)

## Usage

Using TypeScript, you can receive type intelliSense, which provides autocomplete suggestions for:

 - CSS property names and values (through `csstype`)
 - Media feature names (e.g `prefers-color-scheme`, `aspect-ratio`)

```ts
import { matchMediaFeature, cssSupports } from '@neoncitylights/css-types';

// equivalent to window.matchMedia('(prefers-color-scheme: dark)');
const userPrefersDark: MediaQueryList = matchMediaFeature('prefers-color-scheme', 'dark');

// TypeScript support, which provides strongly typed CSS property
// names and values using the `csstype` package
const supportsGrid: boolean = cssSupports('display', 'grid');
const supportsFlex: boolean = cssSupports('display', 'flex');
```

## License

This library is licensed under the [MIT License](./LICENSE).

### Contribution

Unless you explicitly state otherwise, any contribution intentionally submitted for inclusion in the work by you, as defined in the MIT license, shall be licensed as above, without any additional terms or conditions.

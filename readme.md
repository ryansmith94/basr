<div align="center">
  <h1>🦘</br>baseroo</h1>
	<p>Converts positive & negative float values from one base to another between 2-64</p>
	<a href="https://opensource.org/licenses/MIT"><img src="https://img.shields.io/badge/License-MIT-d9207b.svg" alt="License: MIT"></a>
	<a href="https://github.com/semantic-release/semantic-release"><img src="https://img.shields.io/badge/%F0%9F%93%A6%F0%9F%9A%80%20-semantic%20release-d9207b.svg" alt="Uses Semantic Release to correctly bump versions especially for breaking changes"></a>
	<a href="https://renovatebot.com/"><img src="https://img.shields.io/badge/%F0%9F%94%84%F0%9F%A4%96%20-renovate%20bot-d9207b.svg" alt="Uses Renovate to keep dependencies updated"></a>
	<a href="https://codecov.io/gh/ryasmi/baseroo"><img alt="Main branch coverage percentage from Codecov" src="https://codecov.io/gh/ryasmi/baseroo/branch/main/graph/badge.svg" /></a>
	<a href="https://bundlephobia.com/result?p=baseroo"><img alt="Package size from BundlePhobia" src="https://img.shields.io/bundlephobia/minzip/baseroo.svg" /></a>
	<div>
	</div>
</div>

```ts
// Install it with `npm i baseroo`
import { convertBase, customAlphabet } from 'baseroo'

const base16Value = '8f.3333333333'

// Works for floating point numbers to a precision of 10 places.
const base10Value = convertBase(base16Value, 16, 10) // '143.1999999999'

// Supports base conversion using custom alphabet
const convertBaseWithUserAlphabet = customAlphabet(
	'0123456789abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ+/'
)
const base32Value = convertBase(base16Value, 16, 32) // '4f.6cpj6cpj'
```

### Background

Baseroo was created from a [2015 Stack Overflow Answer](https://stackoverflow.com/a/32480941/1221906) from a question asking "How do you convert numbers between different bases in JavaScript?". This answer and [the Gist code snippet](https://gist.github.com/ryasmi/91d7fd30710264affeb9) received some comments requesting some changes, so it was converted to a package with tests and documentation in January 2023 to continue its development and make it easier to use as bug fixes and improvements are made.

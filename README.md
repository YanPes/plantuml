[![npm version][npm-badge]][npm-link]
[![Build Status][travis-badge]][travis-link]

# plantuml

Convert [PlantUML] diagram text to SVG.

## Installation

```bash
$ npm install plantuml
```

## Usage

```js
const plantuml = require('plantuml');
const svg = await plantuml(`
  @startuml
  Bob -> Alice : hello
  Alice -> Wonderland: hello
  Wonderland -> next: hello
  next -> Last: hello
  Last -> next: hello
  next -> Wonderland : hello
  Wonderland -> Alice : hello
  Alice -> Bob: hello
  @enduml
`);

require('fs').writeFileSync('image.svg', svg);
```

## License

MIT

[PlantUML]: https://plantuml.com
[npm-badge]: https://badge.fury.io/js/plantuml.svg
[npm-link]: https://badge.fury.io/js/plantuml
[travis-badge]: https://travis-ci.org/agirorn/plantuml.svg?branch=master
[travis-link]: https://travis-ci.org/agirorn/plantuml

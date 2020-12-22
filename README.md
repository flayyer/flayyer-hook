# useFlayyer (flayyer-hook)

[![styled with prettier](https://img.shields.io/badge/styled_with-prettier-ff69b4.svg)](https://github.com/prettier/prettier)

To create a Flayyer template please refer to: [flayyer.com](https://flayyer.com?ref=flayyer-hook)

## Installation

React Hook to memoize a [Flayyer](https://github.com/flayyer/flayyer-js) instance to prevent unnecessary renderings.

```sh
yarn add @flayyer/flayyer-hook @flayyer/flayyer qs

# or with npm:
npm install --save @flayyer/flayyer-hook @flayyer/flayyer qs
```

Types for [TypeScript](https://www.typescriptlang.org) are included, but if you have any issues try installing `qs` types:

```sh
yarn add --dev @types/qs

# or with npm:
npm install --save-dev @types/qs
```

## Usage

After installing this module you can format URLs just like this example:

```js
import { useFlayyer } from "@flayyer/flayyer-hook";

function SEO() {
  const flayyer = useFlayyer({
    tenant: "tenant",
    deck: "deck",
    template: "template",
    variables {
      title: "Hello world!",
    },
  });

  return (
    <head>
      <meta property="og:image" content={flayyer.href()} />
    </head>
  )
}
```

## Development

Prepare the local environment:

```sh
yarn install
```

To run tests:

```sh
yarn test
```

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/flayyer/flayyer-hook.

## License

The module is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).

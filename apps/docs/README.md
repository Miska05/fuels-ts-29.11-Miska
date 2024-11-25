# `docs`

**docs** is a private package for the Fuel documentation site.

## Table of contents

- [`docs`](#docs)
- [Table of contents](#table-of-contents)
  - [Building](#building)
  - [Testing](#testing)

## Building

The build process will build out our snippets and the documentation.

```sh
pnpm build
```

The build process generates testable scripts from the snippets and outputs them alongside the snippets. The corresponding typegen types are also generated and outputted in the `src/snippets/typegend` folder. All test scripts end with a `.test.ts` suffix.

## Testing

This will build the snippets and run the generated tests. To test a specific environment (`node` or `browser`), the snippet should contain one of the following tags:

```ts
/**
 * @group browser
 */
```

or

```ts
/**
 * @group node
 */
```

If no environment is specified, it will run in the browser and node environments by default.

```sh
pnpm test
```
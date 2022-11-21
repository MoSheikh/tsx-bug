# esbuild-kit/tsx Bug Reproduction

## Description

When watching a project from a specified root, any `dotenv` configs that should be loaded from that root are ignored.

## Steps

1. Run the project using `npx tsx watch main.ts` - note that the `TSX_TEST` environment variable is not loaded, despite the `main.ts` module successfully outputting a log message.
2. Run the project using `npx ts-node-dev main.ts` - note that the `TSX_TEST` environment variable is loaded correctly.


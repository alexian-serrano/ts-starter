# ts-starter

A minimal TypeScript starter (TypeScript + Jest + ESLint + Prettier) used as the
starting point for the Gojob technical interview.

## Requirements

- **Node 20** — pinned in [`.nvmrc`](.nvmrc) and via [Volta](https://volta.sh) in
  `package.json`. With `nvm`, run `nvm use`; with Volta it is picked up
  automatically.
- **Yarn 1.x** — the repo ships a `yarn.lock`.

Node 18 and below will not work: the TypeScript config extends
`@tsconfig/node20`.

## Getting started

```bash
yarn install
yarn test
```

You should see the example test pass. If it does, your environment is ready.

### Using the dev container (optional)

The repo ships a [dev container](.devcontainer/devcontainer.json). Opening the
folder in VS Code ("Reopen in Container") or in GitHub Codespaces gives you Node
20 with dependencies already installed, plus the recommended extensions.

## Commands

| Command           | Description                                  |
| ----------------- | -------------------------------------------- |
| `yarn test`       | Run the test suite once                      |
| `yarn test:watch` | Run the tests in watch mode (handy for TDD)  |
| `yarn build`      | Type-check and compile to `dist/`            |
| `yarn lint`       | Lint every `.ts` file                        |

## Writing tests

Tests are picked up from any file matching `*.spec.ts`, and live next to the
code they cover:

```
src/
  sum.ts
  sum.spec.ts
```

`src/sum.ts` and `src/sum.spec.ts` are a throwaway example so that a fresh clone
builds, tests and lints green. **Delete them when you start the exercise** — but
keep at least one `.ts` file in `src/`, otherwise `yarn build` fails with
`TS18003: No inputs were found in config file`.

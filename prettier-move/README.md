# Prettier Move Action

A GitHub Action to check formatting of Move files using [`@mysten/prettier-plugin-move`](https://www.npmjs.com/package/@mysten/prettier-plugin-move).

## Inputs

| Name              | Description                       | Default     |
| ----------------- | --------------------------------- | ----------- |
| working-directory | Directory with your Move packages | `.`         |
| pattern           | Glob pattern for Move files       | `**/*.move` |

## Simple Use

Add this into a CI job:

```yaml
- uses: your-name/prettier-move-action@v1
  with:
      working-directory: path/to/move/code
```

## Example

Full example using this action:

```yaml
jobs:
    check-formatting:
        runs-on: ubuntu-latest
        steps:
            - uses: actions/checkout@v4
            - uses: your-name/prettier-move-action@v1
              with:
                  working-directory: "." # optional
                  pattern: "**/*.move" # optional
```

## License

Apache-2.0

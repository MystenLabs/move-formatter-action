# Move Formatter Action

A GitHub Action to check (or fix) formatting of Move files using [`@mysten/prettier-plugin-move`](https://www.npmjs.com/package/@mysten/prettier-plugin-move).

## Inputs

| Name                         | Description                                  | Default     |
| ---------------------------- | -------------------------------------------- | ----------- |
| working-directory            | Directory with your Move packages            | `.`         |
| pattern                      | Glob pattern for Move files                  | `**/*.move` |
| prettier-plugin-move-version | Version of the plugin to use                 | `latest`    |
| write-changes                | Whether to fix changes (instead of checking) | `false`     |

## Simple Use

Add this into a CI pipeline:

```yaml
steps:
    - uses: MystenLabs/actions/prettier-move@v1
      with:
          working-directory: path/to/move/code # eg packages
```

## Using Options

Full example using this action:

```yaml
jobs:
    check-formatting:
        runs-on: ubuntu-latest
        steps:
            - uses: actions/checkout@v4
            - uses: MystenLabs/actions/prettier-move@v1
              with:
                  prettier-plugin-move-version: "latest" # optional
                  working-directory: "." # optional
                  pattern: "**/*.move" # optional
                  write-changes: false # optional
```

## License

Apache-2.0

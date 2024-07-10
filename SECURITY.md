# Severity vulnerability on html-minifier (nodeJS dependency)

The node package manager use the package "html-minifier" as a dependency, and it can install dependencies becuase found a severity vulneravility.
And it seems the last release on npm is from 5 years ago: https://www.npmjs.com/package/html-minifier and here's the github repo https://github.com/kangax/html-minifier.

The auditory says "no fix available". Here's the issue from 2022 on the [html-minifier repo on GitHub](https://github.com/kangax/html-minifier/issues/1135).

- Runnning command for installing dependencies locally:
```sh
 ╭─user@sys
╰─λ npm install

up to date, audited 527 packages in 988ms

140 packages are looking for funding
  run `npm fund` for details

1 high severity vulnerability

Some issues need review, and may require choosing
a different dependency.

Run `npm audit` for details.
```

- Runnning command for building 11ty website locally:

```sh
 ╭─user@sys
 ╰─λ npm audit
# npm audit report

html-minifier  *
Severity: high
kangax html-minifier REDoS vulnerability - https://github.com/advisories/GHSA-pfq8-rq6v-vf5m
No fix available
node_modules/html-minifier

1 high severity vulnerability

Some issues need review, and may require choosing
a different dependency.
```

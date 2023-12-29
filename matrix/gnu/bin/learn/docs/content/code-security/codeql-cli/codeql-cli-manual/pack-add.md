---
title: pack add
versions: # DO NOT MANUALLY EDIT. CHANGES WILL BE OVERWRITTEN BY A 🤖
  fpt: '*'
  ghae: '*'
  ghec: '*'
  ghes: '*'
topics:
  - Advanced Security
  - Code scanning
  - CodeQL
type: reference
product: '{% data reusables.gated-features.codeql %}'
autogenerated: codeql-cli
intro: |-
  [Experimental] Adds a list of QL library packs with optional version
  ranges as dependencies of the current package, and then installs them.
redirect_from:
  - /code-security/codeql-cli/manual/pack-add
---


<!-- Content after this section is automatically generated -->

{% data reusables.codeql-cli.man-pages-version-note %}

## Synopsis

```shell copy
codeql pack add <options>... -- <scope/name[@range]>...
```

## Description

\[Experimental] Adds a list of QL library packs with optional version
ranges as dependencies of the current package, and then installs them.

This command modifies the qlpack.yml file of the current package.
Formatting and comments will be removed.

Available since `v2.6.0`.

## Options

### Primary Options

#### `<scope/name[@range]>...`

\[Mandatory] The scope, name, and optional version range of the pack to
add to the dependency list.

If no version range is specified, or if the version range is specified
as 'latest', the latest version of the pack is downloaded, and a
dependency is added to qlpack.yml that allows any version that is
compatible with the downloaded version.

If a single version is specified, that version of the pack is
downloaded, and a dependency is added to qlpack.yml that allows any
version that is compatible with the specified version.

If a version range is specified, the latest version of the pack that
satisfies the specified range is downloaded, and a dependency is added
to qlpack.yml with the specified version range.

#### `--dir=<dir>`

The root directory of the package.

#### `--registries-auth-stdin`

Authenticate to GitHub Enterprise Server Container registries by passing
a comma-separated list of \<registry\_url>=\<token> pairs.

For example, you can pass
`https://containers.GHEHOSTNAME1/v2/=TOKEN1,https://containers.GHEHOSTNAME2/v2/=TOKEN2`
to authenticate to two GitHub Enterprise Server instances.

This overrides the CODEQL\_REGISTRIES\_AUTH and GITHUB\_TOKEN environment
variables. If you only need to authenticate to the github.com Container
registry, you can instead authenticate using the simpler
`--github-auth-stdin` option.

#### `--github-auth-stdin`

Authenticate to the github.com Container registry by passing a
github.com GitHub Apps token or personal access token via standard
input.

To authenticate to GitHub Enterprise Server Container registries, pass
`--registries-auth-stdin` or use the CODEQL\_REGISTRIES\_AUTH environment
variable.

This overrides the GITHUB\_TOKEN environment variable.

#### `--[no-]allow-prerelease`

Allow packs with pre-release version qualifiers (e.g.,
`X.Y.Z-qualifier`) to be used. Without this flag, pre-release packs will
be ignored.

Available since `v2.11.3`.

### Common options

#### `-h, --help`

Show this help text.

#### `-J=<opt>`

\[Advanced] Give option to the JVM running the command.

(Beware that options containing spaces will not be handled correctly.)

#### `-v, --verbose`

Incrementally increase the number of progress messages printed.

#### `-q, --quiet`

Incrementally decrease the number of progress messages printed.

#### `--verbosity=<level>`

\[Advanced] Explicitly set the verbosity level to one of errors,
warnings, progress, progress+, progress++, progress+++. Overrides `-v`
and `-q`.

#### `--logdir=<dir>`

\[Advanced] Write detailed logs to one or more files in the given
directory, with generated names that include timestamps and the name of
the running subcommand.

(To write a log file with a name you have full control over, instead
give `--log-to-stderr` and redirect stderr as desired.)

#### `--common-caches=<dir>`

\[Advanced] Controls the location of cached data on disk that will
persist between several runs of the CLI, such as downloaded QL packs and
compiled query plans. If not set explicitly, this defaults to a
directory named `.codeql` in the user's home directory; it will be
created if it doesn't already exist.

Available since `v2.15.2`.
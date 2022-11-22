# gh-mergeprs  - merge multiple Pull Requests easily

`gh mergeprs` helps you merge multiple PR easily. It is a wrapper around `gh pr merge` allowing you to merge multiple PRs at once by selecting them from a list with fzf.

This usually useful when used with dependabot PRs, to merge them all at once.

## Installation

```shell
gh extension install chmouel/gh-mergeprs
```

### Requirements

- [GH](https://github.com/cli/cli)
- [FZF](https://github.com/junegunn/fzf)
- [JQ](https://stedolan.github.io/jq/) - ***Optional***

## Usage

```shell
gh mergeprs
```

if you add a `-l` it will filter the pr that has the label you specify

example:

```shell
gh mergeprs -l "dependencies"
```

If you add the flag `-c` it will use the `gh pr checks` command to check if the PR has any failing checks and will not merge it if it does.

by default it will ask you if you want to merge the pr, unless you specify the option `-s`

## Copyright

[Apache-2.0](./LICENSE)

## Authors

Chmouel Boudjnah

- Fediverse - <[@chmouel@fosstodon.org](https://fosstodon.org/@chmouel)>
- Twitter - <[@chmouel](https://twitter.com/chmouel)>
- Blog  - <[https://blog.chmouel.com](https://blog.chmouel.com)>

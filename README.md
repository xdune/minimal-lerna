# Lerna tutorial

## TLDR;

* `yarn` (installs lerna etc)
* `lerna bootstrap` (connects all the packages)
* `npm -C ./packages/usage run start` (console logs "alpha" and "beta" from combind use example module)

* Tree Structure

* `packages`
  * `alpha` (`deps: []`)
  * `beta` (`deps: []`)
  * `usage` (`deps: ["alpha", "beta"]`)

## Commands

```shell
# publish your new tag and packages
lerna publish

# change just the version
lerna version

# show current repo tags
git tag -l
```

## Independant versioning

[How Does Independent Versioning Work?](https://samhogy.co.uk/2018/08/lerna-independent-mode-with-semver.html#how-does-independent-versioning-work)

## Github Packages

[How to use the GitHub Package Registry](https://youtu.be/2-77KhGWlRg)

## Private

Pay attention to the fact that usage package is set to `private: true`. The consequence is that `lerna publish` will never publish it to the registry.

## Automated workflows

[Introduction to Semantic Release](https://blog.greenkeeper.io/introduction-to-semantic-release-33f73b117c8)

[Semantic Release](https://github.com/semantic-release)
[Commitizen](https://github.com/commitizen/cz-cli)

## Git multiple accounts

[How to manage multiple GitHub accounts on a single machine with SSH keys](https://www.freecodecamp.org/news/manage-multiple-github-accounts-the-ssh-way-2dadc30ccaca/)

It's working but the packages are pushed to their own repo `https://npm.pkg.github.com/@xdune/usage`

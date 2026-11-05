<p align="center">
  <a href="https://solophp.github.io/">
    <img src="https://solophp.github.io/logo.svg" width="96" height="96" alt="SoloPHP logo">
  </a>
</p>

<h1 align="center">SoloPHP</h1>

<h2 align="center">Independent PHP packages that work together</h2>

<p align="center">
  <a href="https://solophp.github.io/">Documentation</a> ·
  <a href="https://solophp.github.io/packages.html">Package catalog</a> ·
  <a href="https://packagist.org/packages/solophp/">Packagist</a>
</p>

Install a single package in an existing app, or start with the SoloPHP components already wired together. The packages use PSR interfaces where available and share a small set of [SoloPHP contracts](https://github.com/SoloPHP/Contracts) for the rest.

## Start a project

Both starters require PHP 8.4+ and Composer. The web starter also needs Node.js.

### JSON API

A working CRUD module with SQLite, typed request validation, error handling and feature tests.

```bash
composer create-project solophp/skeleton my-app
cd my-app
composer serve
```

[Build your first module](https://solophp.github.io/guide/getting-started.html) · [View source](https://github.com/SoloPHP/Skeleton)

### Inertia.js + Svelte

Server-side routes and controllers with an Inertia.js 3 and Svelte 5 frontend.

```bash
composer create-project solophp/inertia-svelte-skeleton my-app
```

[Set up PHP and Vite](https://solophp.github.io/guide/inertia.html) · [View source](https://github.com/SoloPHP/Inertia-Svelte-Skeleton)

## Add a package

```bash
composer require solophp/router
```

Most packages support PHP 8.3+. The Container requires PHP 8.4+.

| Package | Use it for |
| --- | --- |
| **[Router](https://github.com/SoloPHP/Router)** | HTTP routes, groups and named URLs |
| **[Application](https://github.com/SoloPHP/Application)** | A PSR-15 middleware pipeline |
| **[Container](https://github.com/SoloPHP/Container)** | PSR-11 dependency injection and autowiring |
| **[Input](https://github.com/SoloPHP/Input)** | Typed, validated request DTOs |
| **[Validator](https://github.com/SoloPHP/Validator)** | Field validation with structured errors |
| **[Repository](https://github.com/SoloPHP/Repository)** | Typed repositories over Doctrine DBAL |
| **[Cache](https://github.com/SoloPHP/Cache)** | PSR-16 caching with files or Redis |
| **[Inertia](https://github.com/SoloPHP/Inertia)** | An Inertia.js adapter for PSR-7 and PSR-15 |

[See all packages and versions](https://solophp.github.io/packages.html) · [Find replacements for legacy packages](https://solophp.github.io/packages.html#legacy)

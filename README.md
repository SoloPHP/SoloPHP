# SoloPHP

**Small, independent PSR packages for PHP. Use one, or all of them together.**

Solo is not a framework. Each package does one job: a router, a container, request DTOs, a validator, repositories, a logger. They meet at PSR interfaces, and at [solophp/contracts](https://github.com/SoloPHP/Contracts) where PSR has none, so you can take one package into any project or replace one with another implementation. Two starter applications show how they fit together.

[Website](https://solophp.github.io/) · [Getting started](https://solophp.github.io/guide/getting-started.html) · [Packages](https://solophp.github.io/packages.html) · [Packagist](https://packagist.org/packages/solophp/)

## Start a project

```bash
# A JSON API: one CRUD module, validation, SQLite, error handling, logging and tests
composer create-project solophp/skeleton my-app

# Inertia.js 3 and Svelte 5: server-side routing and controllers, a single-page front end
composer create-project solophp/inertia-svelte-skeleton my-app
```

Both starters need PHP 8.4 and Composer, and the Inertia one also needs Node.js. They pass PHPUnit, PHPStan at level max and PSR-12 out of the box. See [Skeleton](https://github.com/SoloPHP/Skeleton), [Inertia-Svelte-Skeleton](https://github.com/SoloPHP/Inertia-Svelte-Skeleton) and the [tutorial](https://solophp.github.io/guide/getting-started.html).

## Packages

Every package runs on PHP 8.3 or later, except Container, which needs 8.4.

### HTTP kernel

| Package | What it does | Docs | Packagist |
|---|---|---|---|
| [solophp/application](https://github.com/SoloPHP/Application) | PSR-15 kernel: service providers, a middleware pipeline, routing and a route cache | [Docs](https://solophp.github.io/Application/) | [![solophp/application](https://img.shields.io/packagist/v/solophp/application?label=)](https://packagist.org/packages/solophp/application) |
| [solophp/router](https://github.com/SoloPHP/Router) | Routes, groups and parameter patterns, compiled for matching; URLs built from route names | [Docs](https://solophp.github.io/Router/) | [![solophp/router](https://img.shields.io/packagist/v/solophp/router?label=)](https://packagist.org/packages/solophp/router) |
| [solophp/container](https://github.com/SoloPHP/Container) | PSR-11 container with autowiring, interface binding and lazy services | [Docs](https://solophp.github.io/Container/) | [![solophp/container](https://img.shields.io/packagist/v/solophp/container?label=)](https://packagist.org/packages/solophp/container) |
| [solophp/http-emitter](https://github.com/SoloPHP/HTTP-Emitter) | Sends a PSR-7 response: status line, headers and a streamed body | [README](https://github.com/SoloPHP/HTTP-Emitter#readme) | [![solophp/http-emitter](https://img.shields.io/packagist/v/solophp/http-emitter?label=)](https://packagist.org/packages/solophp/http-emitter) |
| [solophp/contracts](https://github.com/SoloPHP/Contracts) | The interfaces the packages share where PSR has none | [README](https://github.com/SoloPHP/Contracts#readme) | [![solophp/contracts](https://img.shields.io/packagist/v/solophp/contracts?label=)](https://packagist.org/packages/solophp/contracts) |

### Input

| Package | What it does | Docs | Packagist |
|---|---|---|---|
| [solophp/input](https://github.com/SoloPHP/Input) | Typed, immutable request DTOs, validated, cast and processed by attributes | [Docs](https://solophp.github.io/Input/) | [![solophp/input](https://img.shields.io/packagist/v/solophp/input?label=)](https://packagist.org/packages/solophp/input) |
| [solophp/validator](https://github.com/SoloPHP/Validator) | Rule strings compiled once, one structured error per field | [Docs](https://solophp.github.io/Validator/) | [![solophp/validator](https://img.shields.io/packagist/v/solophp/validator?label=)](https://packagist.org/packages/solophp/validator) |

### Data

| Package | What it does | Docs | Packagist |
|---|---|---|---|
| [solophp/repository](https://github.com/SoloPHP/Repository) | Typed table repositories over Doctrine DBAL, with translations, batch-loaded relations, stable pages and transactions | [Docs](https://solophp.github.io/Repository/) | [![solophp/repository](https://img.shields.io/packagist/v/solophp/repository?label=)](https://packagist.org/packages/solophp/repository) |
| [solophp/cache](https://github.com/SoloPHP/Cache) | PSR-16 cache with file and Redis adapters | [README](https://github.com/SoloPHP/Cache#readme) | [![solophp/cache](https://img.shields.io/packagist/v/solophp/cache?label=)](https://packagist.org/packages/solophp/cache) |

### Infrastructure

| Package | What it does | Docs | Packagist |
|---|---|---|---|
| [solophp/logger](https://github.com/SoloPHP/Logger) | PSR-3 logger for files shared across processes and for standard error, in line, JSON or logfmt | [Docs](https://solophp.github.io/Logger/) | [![solophp/logger](https://img.shields.io/packagist/v/solophp/logger?label=)](https://packagist.org/packages/solophp/logger) |
| [solophp/dotenv](https://github.com/SoloPHP/Dotenv) | Zero-dependency `.env` loader with typed accessors | [README](https://github.com/SoloPHP/Dotenv#readme) | [![solophp/dotenv](https://img.shields.io/packagist/v/solophp/dotenv?label=)](https://packagist.org/packages/solophp/dotenv) |
| [solophp/event-dispatcher](https://github.com/SoloPHP/Event-Dispatcher) | PSR-14 event dispatcher with priorities, subscribers, listeners matched by class or interface, and stoppable events | [Docs](https://solophp.github.io/Event-Dispatcher/) | [![solophp/event-dispatcher](https://img.shields.io/packagist/v/solophp/event-dispatcher?label=)](https://packagist.org/packages/solophp/event-dispatcher) |
| [solophp/job-queue](https://github.com/SoloPHP/Job-Queue) | Database-backed job queue: leased claims with ownership tokens, per-job retry policies, a long-running worker | [Docs](https://solophp.github.io/Job-Queue/) | [![solophp/job-queue](https://img.shields.io/packagist/v/solophp/job-queue?label=)](https://packagist.org/packages/solophp/job-queue) |
| [solophp/http-client](https://github.com/SoloPHP/HTTP-Client) | Immutable PSR-18 client on Guzzle, with safe retries and credentials bound to their origin | [README](https://github.com/SoloPHP/HTTP-Client#readme) | [![solophp/http-client](https://img.shields.io/packagist/v/solophp/http-client?label=)](https://packagist.org/packages/solophp/http-client) |
| [solophp/session](https://github.com/SoloPHP/Session) | Secure session handling: idle timeout, fixation protection, integrity checks | [README](https://github.com/SoloPHP/Session#readme) | [![solophp/session](https://img.shields.io/packagist/v/solophp/session?label=)](https://packagist.org/packages/solophp/session) |

### Frontend

| Package | What it does | Docs | Packagist |
|---|---|---|---|
| [solophp/inertia](https://github.com/SoloPHP/Inertia) | Inertia.js 3 server adapter for PSR-7 and PSR-15: partial reloads, deferred props, flash data, SSR, Precognition | [Docs](https://solophp.github.io/Inertia/) | [![solophp/inertia](https://img.shields.io/packagist/v/solophp/inertia?label=)](https://packagist.org/packages/solophp/inertia) |

## Legacy

Archived repositories are no longer maintained; their replacements are listed under [Legacy](https://solophp.github.io/packages.html#legacy).

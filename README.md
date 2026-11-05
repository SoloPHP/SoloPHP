# SoloPHP

**Small, independent PSR packages for PHP. Use one, or all of them together.**

Solo is not a framework. Each package does one job: a router, a container, request DTOs, a validator, repositories, a logger. They meet at PSR interfaces, and at [solophp/contracts](https://github.com/SoloPHP/Contracts) where PSR has none, so you can take one package into any project or replace one with another implementation. Two starter applications show how they fit together.

[Website](https://solophp.github.io/) · [Getting started](https://solophp.github.io/guide/getting-started.html) · [Packages](https://solophp.github.io/packages.html) · [Packagist](https://packagist.org/packages/solophp/)

## Start a project

Both starters need PHP 8.4 and Composer. They include tests and are set up for PHPUnit, PHPStan at level max and PSR-12.

### Skeleton · JSON API

[Skeleton](https://github.com/SoloPHP/Skeleton) is a ready-to-run JSON API with one CRUD module, request validation, SQLite, error handling, logging and tests.

1. Create the project with `composer create-project solophp/skeleton my-app`.
2. Enter the project directory with `cd my-app`.
3. Start the API with `composer serve`.

[Build your first module](https://solophp.github.io/guide/getting-started.html)

### Inertia Svelte Skeleton · Web app

[Inertia Svelte Skeleton](https://github.com/SoloPHP/Inertia-Svelte-Skeleton) combines server-side routing and controllers with an Inertia.js 3 and Svelte 5 frontend. It also needs Node.js.

Create the project with `composer create-project solophp/inertia-svelte-skeleton my-app`.

[Set up PHP and Vite](https://solophp.github.io/guide/inertia.html)

## Packages

Every package runs on PHP 8.3 or later, except Container, which needs 8.4.

<table>
  <thead>
    <tr><th scope="col">Package</th><th scope="col">What it does</th><th scope="col">Docs</th><th scope="col">Latest version</th></tr>
  </thead>
  <tbody>
    <tr><th colspan="4" scope="rowgroup" align="left"><a name="http-kernel"></a>HTTP kernel</th></tr>
    <tr>
      <td nowrap="nowrap"><a href="https://github.com/SoloPHP/Application">solophp/application</a></td>
      <td>PSR-15 kernel: service providers, a middleware pipeline, routing and a route cache</td>
      <td><a href="https://solophp.github.io/Application/">Docs</a></td>
      <td><a href="https://packagist.org/packages/solophp/application"><img src="https://img.shields.io/packagist/v/solophp/application?label=" alt="Latest version of solophp/application"></a></td>
    </tr>
    <tr>
      <td nowrap="nowrap"><a href="https://github.com/SoloPHP/Router">solophp/router</a></td>
      <td>Routes, groups and parameter patterns, compiled for matching; URLs built from route names</td>
      <td><a href="https://solophp.github.io/Router/">Docs</a></td>
      <td><a href="https://packagist.org/packages/solophp/router"><img src="https://img.shields.io/packagist/v/solophp/router?label=" alt="Latest version of solophp/router"></a></td>
    </tr>
    <tr>
      <td nowrap="nowrap"><a href="https://github.com/SoloPHP/Container">solophp/container</a></td>
      <td>PSR-11 container with autowiring, interface binding and lazy services</td>
      <td><a href="https://solophp.github.io/Container/">Docs</a></td>
      <td><a href="https://packagist.org/packages/solophp/container"><img src="https://img.shields.io/packagist/v/solophp/container?label=" alt="Latest version of solophp/container"></a></td>
    </tr>
    <tr>
      <td nowrap="nowrap"><a href="https://github.com/SoloPHP/HTTP-Emitter">solophp/http-emitter</a></td>
      <td>Sends a PSR-7 response: status line, headers and a streamed body</td>
      <td><a href="https://github.com/SoloPHP/HTTP-Emitter#readme">README</a></td>
      <td><a href="https://packagist.org/packages/solophp/http-emitter"><img src="https://img.shields.io/packagist/v/solophp/http-emitter?label=" alt="Latest version of solophp/http-emitter"></a></td>
    </tr>
    <tr>
      <td nowrap="nowrap"><a href="https://github.com/SoloPHP/Contracts">solophp/contracts</a></td>
      <td>The interfaces the packages share where PSR has none</td>
      <td><a href="https://github.com/SoloPHP/Contracts#readme">README</a></td>
      <td><a href="https://packagist.org/packages/solophp/contracts"><img src="https://img.shields.io/packagist/v/solophp/contracts?label=" alt="Latest version of solophp/contracts"></a></td>
    </tr>
  </tbody>
  <tbody>
    <tr><th colspan="4" scope="rowgroup" align="left"><a name="input"></a>Input</th></tr>
    <tr>
      <td nowrap="nowrap"><a href="https://github.com/SoloPHP/Input">solophp/input</a></td>
      <td>Typed, immutable request DTOs, validated, cast and processed by attributes</td>
      <td><a href="https://solophp.github.io/Input/">Docs</a></td>
      <td><a href="https://packagist.org/packages/solophp/input"><img src="https://img.shields.io/packagist/v/solophp/input?label=" alt="Latest version of solophp/input"></a></td>
    </tr>
    <tr>
      <td nowrap="nowrap"><a href="https://github.com/SoloPHP/Validator">solophp/validator</a></td>
      <td>Rule strings compiled once, one structured error per field</td>
      <td><a href="https://solophp.github.io/Validator/">Docs</a></td>
      <td><a href="https://packagist.org/packages/solophp/validator"><img src="https://img.shields.io/packagist/v/solophp/validator?label=" alt="Latest version of solophp/validator"></a></td>
    </tr>
  </tbody>
  <tbody>
    <tr><th colspan="4" scope="rowgroup" align="left"><a name="data"></a>Data</th></tr>
    <tr>
      <td nowrap="nowrap"><a href="https://github.com/SoloPHP/Repository">solophp/repository</a></td>
      <td>Typed table repositories over Doctrine DBAL, with translations, batch-loaded relations, stable pages and transactions</td>
      <td><a href="https://solophp.github.io/Repository/">Docs</a></td>
      <td><a href="https://packagist.org/packages/solophp/repository"><img src="https://img.shields.io/packagist/v/solophp/repository?label=" alt="Latest version of solophp/repository"></a></td>
    </tr>
    <tr>
      <td nowrap="nowrap"><a href="https://github.com/SoloPHP/Cache">solophp/cache</a></td>
      <td>PSR-16 cache with file and Redis adapters: atomic file writes, isolated Redis namespaces and typed values</td>
      <td><a href="https://solophp.github.io/Cache/">Docs</a></td>
      <td><a href="https://packagist.org/packages/solophp/cache"><img src="https://img.shields.io/packagist/v/solophp/cache?label=" alt="Latest version of solophp/cache"></a></td>
    </tr>
  </tbody>
  <tbody>
    <tr><th colspan="4" scope="rowgroup" align="left"><a name="infrastructure"></a>Infrastructure</th></tr>
    <tr>
      <td nowrap="nowrap"><a href="https://github.com/SoloPHP/Logger">solophp/logger</a></td>
      <td>PSR-3 logger for files shared across processes and for standard error, in line, JSON or logfmt</td>
      <td><a href="https://solophp.github.io/Logger/">Docs</a></td>
      <td><a href="https://packagist.org/packages/solophp/logger"><img src="https://img.shields.io/packagist/v/solophp/logger?label=" alt="Latest version of solophp/logger"></a></td>
    </tr>
    <tr>
      <td nowrap="nowrap"><a href="https://github.com/SoloPHP/Dotenv">solophp/dotenv</a></td>
      <td>Strict <code>.env</code> loader: layered files, server variables first, all-or-nothing loading and typed accessors</td>
      <td><a href="https://solophp.github.io/Dotenv/">Docs</a></td>
      <td><a href="https://packagist.org/packages/solophp/dotenv"><img src="https://img.shields.io/packagist/v/solophp/dotenv?label=" alt="Latest version of solophp/dotenv"></a></td>
    </tr>
    <tr>
      <td nowrap="nowrap"><a href="https://github.com/SoloPHP/Event-Dispatcher">solophp/event-dispatcher</a></td>
      <td>PSR-14 event dispatcher with priorities, subscribers, listeners matched by class or interface, and stoppable events</td>
      <td><a href="https://solophp.github.io/Event-Dispatcher/">Docs</a></td>
      <td><a href="https://packagist.org/packages/solophp/event-dispatcher"><img src="https://img.shields.io/packagist/v/solophp/event-dispatcher?label=" alt="Latest version of solophp/event-dispatcher"></a></td>
    </tr>
    <tr>
      <td nowrap="nowrap"><a href="https://github.com/SoloPHP/Job-Queue">solophp/job-queue</a></td>
      <td>Database-backed job queue: leased claims with ownership tokens, per-job retry policies, a long-running worker</td>
      <td><a href="https://solophp.github.io/Job-Queue/">Docs</a></td>
      <td><a href="https://packagist.org/packages/solophp/job-queue"><img src="https://img.shields.io/packagist/v/solophp/job-queue?label=" alt="Latest version of solophp/job-queue"></a></td>
    </tr>
    <tr>
      <td nowrap="nowrap"><a href="https://github.com/SoloPHP/Rate-Limiter">solophp/rate-limiter</a></td>
      <td>Atomic per-key rate limits: fixed or renewable windows in Redis, with an in-memory twin for tests</td>
      <td><a href="https://github.com/SoloPHP/Rate-Limiter#readme">README</a></td>
      <td><a href="https://packagist.org/packages/solophp/rate-limiter"><img src="https://img.shields.io/packagist/v/solophp/rate-limiter?label=" alt="Latest version of solophp/rate-limiter"></a></td>
    </tr>
    <tr>
      <td nowrap="nowrap"><a href="https://github.com/SoloPHP/Tokens">solophp/tokens</a></td>
      <td>Tokens for reset links, invitations and sessions: random secrets stored only as hashes, in Redis or in memory</td>
      <td><a href="https://solophp.github.io/Tokens/">Docs</a></td>
      <td><a href="https://packagist.org/packages/solophp/tokens"><img src="https://img.shields.io/packagist/v/solophp/tokens?label=" alt="Latest version of solophp/tokens"></a></td>
    </tr>
    <tr>
      <td nowrap="nowrap"><a href="https://github.com/SoloPHP/HTTP-Client">solophp/http-client</a></td>
      <td>Immutable PSR-18 client on Guzzle: safe retries, credentials bound to their origin and redacted logs</td>
      <td><a href="https://solophp.github.io/HTTP-Client/">Docs</a></td>
      <td><a href="https://packagist.org/packages/solophp/http-client"><img src="https://img.shields.io/packagist/v/solophp/http-client?label=" alt="Latest version of solophp/http-client"></a></td>
    </tr>
  </tbody>
  <tbody>
    <tr><th colspan="4" scope="rowgroup" align="left"><a name="frontend"></a>Frontend</th></tr>
    <tr>
      <td nowrap="nowrap"><a href="https://github.com/SoloPHP/Inertia">solophp/inertia</a></td>
      <td>Inertia.js 3 server adapter for PSR-7 and PSR-15: partial reloads, deferred props, flash data, SSR, Precognition</td>
      <td><a href="https://solophp.github.io/Inertia/">Docs</a></td>
      <td><a href="https://packagist.org/packages/solophp/inertia"><img src="https://img.shields.io/packagist/v/solophp/inertia?label=" alt="Latest version of solophp/inertia"></a></td>
    </tr>
  </tbody>
</table>

## Legacy

Archived repositories are no longer maintained; their replacements are listed under [Legacy](https://solophp.github.io/packages.html#legacy).

# Changelog

All notable changes to this project are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.1] - 2026-04-01

### Added
- Client requirements and contributing guidance (`#68`).
- Apache license headers across the source tree (`#19`).
- Tools for interacting with Colab VMs and Jupyter kernels (`#20`).
- Proxy token support as a WebSocket query parameter (`#15`).

### Changed
- Bumped the minimum `fastmcp` version from 2.2.0 to 2.14.5 (`#57`).
- Switched to the official upstream Jupyter kernel client and restored `openid`
  to the OAuth scopes list (`#34`).
- Startup WebSocket port is now dynamic instead of fixed (`#30`).
- Browser open now happens on tool call rather than at server startup (`#28`).
- OAuth2 service moved to a separate port and `openid` dropped from that flow (`#26`).
- Hooks relocated to `.githooks` (`#16`).

### Fixed
- Corrected `pyproject.toml` formatting (`#59`).
- Allowed both Colab domains as trusted origins (`#37`).
- Handled a race condition where the client-start task resolved after the
  connection event went live (`#33`).
- Corrected tool-call overwrite behavior (`#31`).
- Avoided a pickle error by not passing the asyncio event into the serializer (`#29`).
- Removed incorrect auth initialization (`#25`).
- Fixed miscellaneous session-proxy startup issues (`#23`).
- Logger now defaults to a tempfile path instead of a hard-coded logs directory (`#21`).

### Security
- Bumped `cryptography` 46.0.4 → 46.0.5 (`#22`).
- Bumped `pyasn1` 0.6.2 → 0.6.3 (`#44`), `authlib` 1.6.6 → 1.6.9 (`#42`),
  `pyjwt` 2.11.0 → 2.12.0 (`#39`), and `tornado` 6.5.4 → 6.5.5 (`#38`).

[1.0.1]: https://github.com/googlecolab/colab-mcp/compare/1.0.0...1.0.1
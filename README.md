<p align="center">
  <a href="https://gitea.io/">
    <img alt="Gitea" src="https://raw.githubusercontent.com/go-gitea/gitea/main/public/img/gitea.svg" width="220"/>
  </a>
</p>
<h1 align="center">Gitea - Git with a cup of tea</h1>

<p align="center">
  <a href="https://drone.gitea.io/go-gitea/gitea" title="Build Status">
    <img src="https://drone.gitea.io/api/badges/go-gitea/gitea/status.svg?ref=refs/heads/main">
  </a>
  <a href="https://discord.gg/Gitea" title="Join the Discord chat at https://discord.gg/Gitea">
    <img src="https://img.shields.io/discord/322538954119184384.svg">
  </a>
  <a href="https://codecov.io/gh/go-gitea/gitea" title="Codecov">
    <img src="https://codecov.io/gh/go-gitea/gitea/branch/main/graph/badge.svg">
  </a>
  <a href="https://goreportcard.com/report/code.gitea.io/gitea" title="Go Report Card">
    <img src="https://goreportcard.com/badge/code.gitea.io/gitea">
  </a>
  <a href="https://godoc.org/code.gitea.io/gitea" title="GoDoc">
    <img src="https://godoc.org/code.gitea.io/gitea?status.svg">
  </a>
  <a href="https://github.com/go-gitea/gitea/releases/latest" title="GitHub release">
    <img src="https://img.shields.io/github/release/go-gitea/gitea.svg">
  </a>
  <a href="https://www.codetriage.com/go-gitea/gitea" title="Help Contribute to Open Source">
    <img src="https://www.codetriage.com/go-gitea/gitea/badges/users.svg">
  </a>
  <a href="https://opencollective.com/gitea" title="Become a backer/sponsor of gitea">
    <img src="https://opencollective.com/gitea/tiers/backers/badge.svg?label=backers&color=brightgreen">
  </a>
  <a href="https://opensource.org/licenses/MIT" title="License: MIT">
    <img src="https://img.shields.io/badge/License-MIT-blue.svg">
  </a>
  <a href="https://crowdin.com/project/gitea" title="Crowdin">
    <img src="https://badges.crowdin.net/gitea/localized.svg">
  </a>
  <a href="https://www.tickgit.com/browse?repo=github.com/go-gitea/gitea&branch=main" title="TODOs">
    <img src="https://badgen.net/https/api.tickgit.com/badgen/github.com/go-gitea/gitea/main">
  </a>
  <a href="https://www.bountysource.com/teams/gitea" title="Bountysource">
    <img src="https://img.shields.io/bountysource/team/gitea/activity">
  </a>
</p>

<p align="center">
  <a href="README_ZH.md">View the chinese version of this document</a>
</p>

## Purpose

The goal of this project is to make the easiest, fastest, and most
painless way of setting up a self-hosted Git service.
Using Go, this can be done with an independent binary distribution across
**all platforms** which Go supports, including Linux, macOS, and Windows
on x86, amd64, ARM and PowerPC architectures.
Want to try it before doing anything else?
Do it [with the online demo](https://try.gitea.io/)!
This project has been
[forked](https://blog.gitea.io/2016/12/welcome-to-gitea/) from
[Gogs](https://gogs.io) since 2016.11 but changed a lot.

## Building

From the root of the source tree, run:

    TAGS="bindata" make build

or if SQLite support is required:

    TAGS="bindata sqlite sqlite_unlock_notify" make build

The `build` target is split into two sub-targets:

- `make backend` which requires [Go 1.16](https://golang.org/dl/) or greater.
- `make frontend` which requires [Node.js LTS](https://nodejs.org/en/download/) or greater and Internet connectivity to download npm dependencies.

When building from the official source tarballs which include pre-built frontend files, the `frontend` target will not be triggered, making it possible to build without Node.js and Internet connectivity.

Parallelism (`make -j <num>`) is not supported.

More info: https://docs.gitea.io/en-us/install-from-source/

## Using

    ./gitea web

NOTE: If you're interested in using our APIs, we have experimental
support with [documentation](https://try.gitea.io/api/swagger).

## Further information

For more information and instructions about how to install Gitea, please look at our [documentation](https://docs.gitea.io/en-us/).
If you have questions that are not covered by the documentation, you can get in contact with us on our [Discord server](https://discord.gg/Gitea) or create  a post in the [discourse forum](https://discourse.gitea.io/).

We maintain a list of Gitea-related projects at [gitea/awesome-gitea](https://gitea.com/gitea/awesome-gitea).  
The hugo-based documentation theme is hosted at [gitea/theme](https://gitea.com/gitea/theme).  
The official Gitea CLI is developed at [gitea/tea](https://gitea.com/gitea/tea).
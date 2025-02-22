<a href="https://gohugo.io/"><img src="https://raw.githubusercontent.com/gohugoio/gohugoioTheme/master/static/images/hugo-logo-wide.svg?sanitize=true" alt="Hugo" width="565"></a>

A Fast and Flexible Static Site Generator built with love by [bep](https://github.com/bep), [spf13](https://spf13.com/) and [friends](https://github.com/gohugoio/hugo/graphs/contributors) in [Go](https://go.dev/).

[Website](https://gohugo.io) |
[Forum](https://discourse.gohugo.io) |
[Documentation](https://gohugo.io/getting-started/) |
[Installation Guide](https://gohugo.io/getting-started/installing/) |
[Contribution Guide](CONTRIBUTING.md) |
[Twitter](https://twitter.com/gohugoio)

[![GoDoc](https://godoc.org/github.com/gohugoio/hugo?status.svg)](https://godoc.org/github.com/gohugoio/hugo)
[![Tests on Linux, MacOS and Windows](https://github.com/gohugoio/hugo/workflows/Test/badge.svg)](https://github.com/gohugoio/hugo/actions?query=workflow%3ATest)
[![Go Report Card](https://goreportcard.com/badge/github.com/gohugoio/hugo)](https://goreportcard.com/report/github.com/gohugoio/hugo)

* [Overview](#overview)
* [Banner Sponsors](#banner-sponsors)
* [Supported Architectures](#supported-architectures)
* [Choose How to Install](#choose-how-to-install)
   * [Install Hugo as Your Site Generator (Binary Install)](#install-hugo-as-your-site-generator-binary-install)
   * [Build and Install the Binary from Source (Using the Go toolchain)](#build-and-install-the-binary-from-source-using-the-go-toolchain)
* [The Hugo Documentation](#the-hugo-documentation)
* [Contributing to Hugo](#contributing-code-to-hugo)
* [Dependencies](#dependencies)

## Overview

Hugo is a static HTML and CSS website generator written in [Go](https://go.dev/).
It is optimized for speed, ease of use, and configurability.
Hugo takes a directory with content and templates and renders them into a full HTML website.

Hugo relies on Markdown files with front matter for metadata, and you can run Hugo from any directory.
This works well for shared hosts and other systems where you don’t have a privileged account.

Hugo renders a typical website of moderate size in a fraction of a second.
A good rule of thumb is that each piece of content renders in around 1 millisecond.

Hugo is designed to work well for any kind of website including blogs, tumbles, and docs.

## Banner Sponsors
<p>&nbsp;</p>
<p float="left">
  <a href="https://www.linode.com/?utm_campaign=hugosponsor&utm_medium=banner&utm_source=hugogithub" target="_blank"><img src="https://raw.githubusercontent.com/gohugoio/gohugoioTheme/master/static/images/sponsors/linode-logo_standard_light_medium.png" width="200" alt="Linode"></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<a href="https://esolia.com/post/why-did-esolia-choose-hugo/?utm_campaign=hugosponsor&utm_medium=banner&utm_source=hugogithub" target="_blank"><img src="https://raw.githubusercontent.com/gohugoio/gohugoioTheme/master/static/images/sponsors/esolia-logo.svg?sanitize=true" width="200" alt="eSOLIA"></a>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="https://buttercms.com/hugo-cms/?utm_campaign=sponsorship&utm_medium=banner&utm_source=hugogithub" target="_blank"><img src="https://raw.githubusercontent.com/gohugoio/gohugoioTheme/master/static/images/sponsors/butter-dark.svg?sanitize=true" width="280" alt="ButterCMS"></a>
</p>
<p>&nbsp;</p>

## Supported Architectures

Currently, we provide pre-built Hugo binaries for Windows, Linux, FreeBSD, NetBSD, DragonFly BSD, OpenBSD, macOS (Darwin), and [Android](https://gist.github.com/bep/a0d8a26cf6b4f8bc992729b8e50b480b) for x64, i386 and ARM architectures.

Hugo may also be compiled from source wherever the Go compiler tool chain can run, e.g. for other operating systems including Plan 9 and Solaris.

**Complete documentation is available at [Hugo Documentation](https://gohugo.io/getting-started/).**

## Choose How to Install

If you want to use Hugo as your site generator, simply install the Hugo binaries.

To contribute to the Hugo source code or documentation, you should [fork the Hugo GitHub project](https://github.com/gohugoio/hugo#fork-destination-box) and clone it to your local machine.

Finally, you can install the Hugo source code with `go`, build the binaries yourself, and run Hugo that way.
Building the binaries is an easy task for an experienced `go` getter.

### Install Hugo as Your Site Generator (Binary Install)

Use the [installation instructions in the Hugo documentation](https://gohugo.io/getting-started/installing/).

### Build and Install the Binary from Source (Using the Go toolchain)

#### Prerequisite Tools

* [Go (we test it with the last 2 major versions; but note that Hugo 0.95.0 only builds with >= Go 1.18.)](https://golang.org/dl/)

#### Fetch from GitHub

To fetch, build and install from the Github source:

```bash
go install github.com/gohugoio/hugo@latest
```

If you want to compile with Sass/SCSS support use `--tags extended` and make sure `CGO_ENABLED=1` is set in your go environment. If you don't want to have CGO enabled, you may use the following command to temporarily enable CGO only for hugo compilation:

```bash
CGO_ENABLED=1 go install --tags extended github.com/gohugoio/hugo@latest
```

## The Hugo Documentation

The Hugo documentation now lives in its own repository, see https://github.com/gohugoio/hugoDocs. But we do keep a version of that documentation as a `git subtree` in this repository. To build the sub folder `/docs` as a Hugo site, you need to clone this repo:

```bash
git clone git@github.com:gohugoio/hugo.git
```
## Contributing code to Hugo

**Note  March 16th 2022:** We are currently very constrained on human resources to do code reviews, so we currently require any new Pull Requests to be limited to bug fixes closing an existing issue. Also, we have updated to Go 1.18, but we will currently not accept any generic rewrites, "interface{} to any" replacements and similar.

For a complete guide to contributing to Hugo, see the [Contribution Guide](CONTRIBUTING.md).

We welcome contributions to Hugo of any kind including documentation, themes,
organization, tutorials, blog posts, bug reports, issues, feature requests,
feature implementations, pull requests, answering questions on the forum,
helping to manage issues, etc.

The Hugo community and maintainers are [very active](https://github.com/gohugoio/hugo/pulse/monthly) and helpful, and the project benefits greatly from this activity.

## Asking Support Questions

We have an active [discussion forum](https://discourse.gohugo.io) where users and developers can ask questions.
Please don't use the GitHub issue tracker to ask questions.

## Reporting Issues

If you believe you have found a defect in Hugo or its documentation, use
the GitHub issue tracker to report the problem to the Hugo maintainers.
If you're not sure if it's a bug or not, start by asking in the [discussion forum](https://discourse.gohugo.io).
When reporting the issue, please provide the version of Hugo in use (`hugo version`).

## Dependencies

Hugo stands on the shoulder of many great open source libraries.

If you run `hugo env -v` you will get a complete and up to date list.

In Hugo 0.100.1 that list is, in lexical order:

[![Analytics](https://ga-beacon.appspot.com/UA-7131036-6/hugo/readme)](https://github.com/igrigorik/ga-beacon)

[Go]: https://golang.org/
[Hugo Documentation]: https://gohugo.io/overview/introduction/

## Dependencies

Hugo stands on the shoulder of many great open source libraries, in lexical order:

 | Dependency  | License |
 | :------------- | :------------- |
 | [github.com/alecthomas/chroma](https://github.com/alecthomas/chroma) | MIT License |
 | [github.com/armon/go-radix](https://github.com/armon/go-radix) | MIT License |
 | [github.com/aws/aws-sdk-go](https://github.com/aws/aws-sdk-go) | Apache License 2.0 |
 | [github.com/bep/debounce](https://github.com/bep/debounce) | MIT License |
 | [github.com/bep/gitmap](https://github.com/bep/gitmap) | MIT License |
 | [github.com/bep/golibsass](https://github.com/bep/golibsass) | MIT License |
 | [github.com/bep/tmc](https://github.com/bep/tmc) | MIT License |
 | [github.com/BurntSushi/locker](https://github.com/BurntSushi/locker) | The Unlicense |
 | [github.com/BurntSushi/toml](https://github.com/BurntSushi/toml) | MIT License |
 | [github.com/cpuguy83/go-md2man](https://github.com/cpuguy83/go-md2man) | MIT License |
 | [github.com/danwakefield/fnmatch](https://github.com/danwakefield/fnmatch) | BSD 2-Clause "Simplified" License |
 | [github.com/disintegration/gift](https://github.com/disintegration/gift) | MIT License |
 | [github.com/dustin/go-humanize](https://github.com/dustin/go-humanize) | MIT License |
 | [github.com/fsnotify/fsnotify](https://github.com/fsnotify/fsnotify) | BSD 3-Clause "New" or "Revised" License |
 | [github.com/gobwas/glob](https://github.com/gobwas/glob) | MIT License |
 | [github.com/gorilla/websocket](https://github.com/gorilla/websocket) | BSD 2-Clause "Simplified" License |
 | [github.com/hashicorp/golang-lru](https://github.com/hashicorp/golang-lru) | Mozilla Public License 2.0 |
 | [github.com/hashicorp/hcl](https://github.com/hashicorp/hcl) | Mozilla Public License 2.0 |
 | [github.com/jdkato/prose](https://github.com/jdkato/prose) | MIT License |
 | [github.com/kr/pretty](https://github.com/kr/pretty) | MIT License |
 | [github.com/kyokomi/emoji](https://github.com/kyokomi/emoji) | MIT License |
 | [github.com/magiconair/properties](https://github.com/magiconair/properties) | BSD 2-Clause "Simplified" License |
 | [github.com/markbates/inflect](https://github.com/markbates/inflect) | MIT License |
 | [github.com/mattn/go-isatty](https://github.com/mattn/go-isatty) | MIT License |
 | [github.com/mattn/go-runewidth](https://github.com/mattn/go-runewidth) | MIT License |
 | [github.com/miekg/mmark](https://github.com/miekg/mmark) | Simplified BSD License |
 | [github.com/mitchellh/hashstructure](https://github.com/mitchellh/hashstructure) | MIT License |
 | [github.com/mitchellh/mapstructure](https://github.com/mitchellh/mapstructure) | MIT License |
 | [github.com/muesli/smartcrop](https://github.com/muesli/smartcrop) | MIT License |
 | [github.com/nicksnyder/go-i18n](https://github.com/nicksnyder/go-i18n) | MIT License |
 | [github.com/niklasfasching/go-org](https://github.com/niklasfasching/go-org) | MIT License |
 | [github.com/olekukonko/tablewriter](https://github.com/olekukonko/tablewriter) | MIT License |
 | [github.com/pelletier/go-toml](https://github.com/pelletier/go-toml) | MIT License |
 | [github.com/pkg/errors](https://github.com/pkg/errors) | BSD 2-Clause "Simplified" License |
 | [github.com/PuerkitoBio/purell](https://github.com/PuerkitoBio/purell) | BSD 3-Clause "New" or "Revised" License |
 | [github.com/PuerkitoBio/urlesc](https://github.com/PuerkitoBio/urlesc) | BSD 3-Clause "New" or "Revised" License |
 | [github.com/rogpeppe/go-internal](https://github.com/rogpeppe/go-internal) | BSD 3-Clause "New" or "Revised" License |
 | [github.com/russross/blackfriday](https://github.com/russross/blackfriday)  | Simplified BSD License |
 | [github.com/rwcarlsen/goexif](https://github.com/rwcarlsen/goexif) | BSD 2-Clause "Simplified" License |
 | [github.com/spf13/afero](https://github.com/spf13/afero) | Apache License 2.0 |
 | [github.com/spf13/cast](https://github.com/spf13/cast) | MIT License |
 | [github.com/spf13/cobra](https://github.com/spf13/cobra) | Apache License 2.0 |
 | [github.com/spf13/fsync](https://github.com/spf13/fsync) | MIT License |
 | [github.com/spf13/jwalterweatherman](https://github.com/spf13/jwalterweatherman) | MIT License |
 | [github.com/spf13/pflag](https://github.com/spf13/pflag) | BSD 3-Clause "New" or "Revised" License |
 | [github.com/spf13/viper](https://github.com/spf13/viper) | MIT License |
 | [github.com/tdewolff/minify](https://github.com/tdewolff/minify) | MIT License |
 | [github.com/tdewolff/parse](https://github.com/tdewolff/parse) | MIT License |
 | [github.com/yosssi/gohtml](https://github.com/yosssi/gohtml) | MIT License |
 | [github.com/yuin/goldmark](https://github.com/yuin/goldmark) | MIT License |
 | [github.com/yuin/goldmark-highlighting](https://github.com/yuin/goldmark-highlighting) | MIT License |
 | [go.opencensus.io](https://go.opencensus.io) | Apache License 2.0 |
 | [go.uber.org/atomic](https://go.uber.org/atomic) | MIT License |
 | [gocloud.dev](https://gocloud.dev) | Apache License 2.0 |
 | [golang.org/x/image](https://golang.org/x/image) | BSD 3-Clause "New" or "Revised" License |
 | [golang.org/x/net](https://golang.org/x/net) | BSD 3-Clause "New" or "Revised" License |
 | [golang.org/x/oauth2](https://golang.org/x/oauth2) | BSD 3-Clause "New" or "Revised" License |
 | [golang.org/x/sync](https://golang.org/x/sync) | BSD 3-Clause "New" or "Revised" License |
 | [golang.org/x/sys](https://golang.org/x/sys) | BSD 3-Clause "New" or "Revised" License |
 | [golang.org/x/text](https://golang.org/x/text) | BSD 3-Clause "New" or "Revised" License |
 | [golang.org/x/xerrors](https://golang.org/x/xerrors) | BSD 3-Clause "New" or "Revised" License |
 | [google.golang.org/api](https://google.golang.org/api) | BSD 3-Clause "New" or "Revised" License |
 | [google.golang.org/genproto](https://google.golang.org/genproto) | Apache License 2.0 |
 | [gopkg.in/ini.v1](https://gopkg.in/ini.v1) | Apache License 2.0 |
 | [gopkg.in/yaml.v2](https://gopkg.in/yaml.v2) | Apache License 2.0 |

# Hyas Bootstrap starter theme

Bootstrap starter theme for Hyas sites.

## Status

[![npm (scoped)](https://img.shields.io/npm/v/@hyas/themes-starter-bootstrap?style=flat-square)](https://www.npmjs.com/package/@hyas/themes-starter-bootstrap) [![GitHub Workflow Status](https://img.shields.io/github/workflow/status/h-enk/hyas-themes-starter-bootstrap/CodeQL?style=flat-square)]((https://github.com/h-enk/hyas-themes-starter-bootstrap/actions/workflows/codeql.yml))

## Requirements

- [hyas](https://www.npmjs.com/package/hyas)

### Optional, recommended

- [@hyas/seo](https://www.npmjs.com/package/@hyas/seo)
- [@hyas/images](https://www.npmjs.com/package/@hyas/images)

## Installation

```bash
npm i @hyas/themes-starter-bootstrap -D
```

## Setup

Add to `./config/_default/module.toml`:

```toml
[[mounts]]
  source = "node_modules/@hyas/themes-starter-bootstrap/archetypes"
  target = "archetypes"

[[mounts]]
  source = "node_modules/@hyas/themes-starter-bootstrap/assets"
  target = "assets"

[[mounts]]
  source = "node_modules/@hyas/themes-starter-bootstrap/layouts"
  target = "layouts"

[[mounts]]
  source = "archetypes"
  target = "archetypes"

[[mounts]]
  source = "assets"
  target = "assets"

[[mounts]]
  source = "layouts"
  target = "layouts"
```

Add to `./config/_default/config.toml`:

```toml
[taxonomies]
  category = "categories"

[permalinks]
  blog = "/:title/"

[related]
  threshold = 80
  includeNewer = true
  toLower = false
    [[related.indices]]
    name = "categories"
    weight = 100
    [[related.indices]]
    name = "date"
    weight = 10
```

Add to `./config/_default/params.toml`:

```toml
# Footer
footer = "Powered by <a href=\"https://www.netlify.com/\">Netlify</a>, <a href=\"https://gohugo.io/\">Hugo</a>, and <a href=\"https://gethyas.com/\">Hyas</a>"

# Alert
alert = false
alertDismissable = true
alertText = "Deliver web projects 10x faster. <a class=\"alert-link\" href=\"https://www.netlify.com/whitepaper/\" target=\"_blank\" rel=\"noopener\">Get the free enterprise paper →</a>"
```

## Usage

See the Hyas docs: [Themes](https://gethyas.com/docs/reference-guides/themes/)

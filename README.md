# TMF API Commons

A shared commons of scripts and actions supporting the TM Forum API ecosystem.

The authoritative source of all API information is the [TM Forum API Directory](https://www.tmforum.org/oda/open-apis/directory).

## GitHub Actions

This repository hosts the reusable GitHub actions used by the other repositories in the org.

### Action: Release TM Forum API

Accepts a TM Forum API identity (e.g. TMF123), and creates a release with any un-tagged version it finds in the online directory.

Use this action in a repository:

```yaml
name: API release

on:
  workflow_dispatch:

permissions:
  contents: write

jobs:
  call-api-release-workflow:
    uses: tmforum-apis/tmf-api-commons/.github/workflows/release-api.yml@main
    with:
      api_name: TMF123 # Edit this line and set the API to fetch and publish
```




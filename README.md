# repo2static
A GitHub action to give your repository a static Pages website.

## Usage

Create a GitHub workflow @ `.github/workflows/deploy-readme.yml`:

```yaml
name: Deploy to Pages

on:
  push:
    branches: [ "main", "master" ]
    paths:
      - "README.md"
      - "readme.md"
  workflow_dispatch:

jobs:
  deploy:
    uses: uukelele-scratch/repo2static/.github/workflows/deploy.yml@v1
```
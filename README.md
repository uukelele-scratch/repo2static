# repo2static
A GitHub action to give your repository a static Pages website.

## Usage

1. Enable Pages for your repo @ https://github.com/user/repo/settings/pages

2. Create a GitHub workflow @ `.github/workflows/deploy-readme.yml`:

```yaml
name: Deploy to Pages

on:
  push:
    branches: [ "main", "master" ]
    paths:
      - "README.md"
      - "readme.md"
  workflow_dispatch:

permissions:
  pages: write
  id-token: write
  contents: read

jobs:
  deploy:
    uses: uukelele-scratch/repo2static/.github/workflows/deploy.yml@main
```

3. Go to Actions and trigger a workflow run for Deploy.

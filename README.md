## github-actions (shared)

It contains the composite actions used by:
- `app/.github/workflows/*`
- `terraform/.github/workflows/terraform.yml`

### Why
So every service repo doesn’t have to copy/paste 80 lines of YAML.

### How to use it:
In a workflow:

- `uses: cosminmcnoprea-pixel/gh-actions/.github/actions/<action-name>@main`

### WIF secrets expected
Most workflows assume:
- `WIF_PROVIDER_DEV` / `WIF_SERVICE_ACCOUNT_DEV`
- `WIF_PROVIDER_PROD` / `WIF_SERVICE_ACCOUNT_PROD`

### Cloud Build (optional)
Dev deploy supports building the container via Cloud Build.

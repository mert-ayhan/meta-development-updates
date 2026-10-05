# Meta Development Updates

Public version catalog for Meta Development FiveM resources.

[Read the version catalog](https://raw.githubusercontent.com/mert-ayhan/meta-development-updates/main/versions.json).

## Catalog format

Each key is a resource name. Its version must match the published package's fxmanifest.lua version.

```json
{
  "meta-slots": {
    "version": "2.0.0"
  }
}
```

Add other products as additional keys in the same file. Use stable major.minor.patch versions; publish preview and prerelease information separately.

## Publishing an update

1. Finish and publish the customer package.
2. Update only that product's version in versions.json.
3. Commit and push to main.

Scripts read their own entry at startup and print an update notice when a newer version is available. Customers obtain the package through their purchase download.

This repository contains public release information. Runtime checks do not install or replace customer resource files.
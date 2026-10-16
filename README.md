# Zaptec
[![Validate Homey App](https://github.com/PatrickE94/com.zaptec/actions/workflows/homey-app-validate.yml/badge.svg)](https://github.com/PatrickE94/com.zaptec/actions/workflows/homey-app-validate.yml)
[![Build Homey App](https://github.com/PatrickE94/com.zaptec/actions/workflows/homey-build-release.yml/badge.svg)](https://github.com/PatrickE94/com.zaptec/actions/workflows/homey-build-release.yml)

Adds support for Zaptec charging products.

This repository is a fork of the Homey Zaptec app maintained at
[W3BNVR/Homey.zaptec](https://github.com/W3BNVR/Homey.zaptec).

## Charging session authorization

The Charger widget includes an **Authorize** button for authorizing the connected
charging session. This is separate from the existing **Access** control, which
changes whether the installation requires authentication for charging.

The session button calls Zaptec's `POST /api/chargers/{id}/authorizecharge`
endpoint. Zaptec does not list this endpoint in its public API reference, so it
may change without notice. Authorization is intended for installations using
Zaptec's native authentication; it does not change the installation's
authentication settings.

## Documentation
Integration guide is found [here](https://zaptec.readme.io/)

## Github actions
Homey validate the code automatically when pushing to the main branch.

To use the github action for versioning, tagging, changelog and publishing, one need to aquire a personal access token (PAT) from [Developer portal](https://tools.developer.homey.app/me) and save it as a secret in your repository named `HOMEY_PAT`.

## Links
[Homey App](https://homey.app/a/com.zaptec)  
[Homey Community](https://community.homey.app/t/app-pro-zaptec-charging/118631)

Using [Material Web](https://github.com/material-components/material-web) for components.
Import modules in index.js
And bundle using rollup:
```
npm run build:widget
```

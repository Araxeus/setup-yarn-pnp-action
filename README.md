# Yarn PnP setup action

## Behavior

- runs [actions/checkout](https://github.com/actions/checkout)

- runs [actions/setup-node](https://github.com/actions/setup-node)

- install yarn@stable using `corepack enable && corepack prepare yarn@stable --activate`

- cache the yarn cache using [actions/cache](https://github.com/actions/cache), with support for yarn PnP using `yarn config get cacheFolder`

- run `yarn install --immutable` to install the dependencies

## Inputs

- node-version: the node version to use (default to the system one)

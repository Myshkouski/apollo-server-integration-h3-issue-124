# Nuxt 3 with `@apollo/server` and `@as-integrations/h3`

This project was created to resolve issues with dependency misconfiguration of `@as-integrations/h3`. See [issue](https://github.com/apollo-server-integrations/apollo-server-integration-h3/issues/124) for details.

`npm run build:cloudflare` will fail due to `graphql-ws` imported as runtime dependency, but configured as optional peer dependency in (package.json)[node_modules/@as-integrations/h3/package.json].

> `@as-integrations/h3@1.2.1` not published yet, so `@as-integrations/h3@1.2.1` was [patched](patches/@as-integrations+h3+1.2.1.patch) to use dynamic import of `graphql-ws`.

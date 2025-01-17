# actix-web-middleware-keycloak-auth

[![LICENSE](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
![Build and test](https://github.com/dsferruzza/actix-web-middleware-keycloak-auth/workflows/Build%20and%20test/badge.svg)
![Lint](https://github.com/dsferruzza/actix-web-middleware-keycloak-auth/workflows/Lint/badge.svg)
[![Crates.io Version](https://img.shields.io/crates/v/actix-web-middleware-keycloak-auth.svg)](https://crates.io/crates/actix-web-middleware-keycloak-auth)
[![Documentation](https://docs.rs/actix-web-middleware-keycloak-auth/badge.svg)](https://docs.rs/actix-web-middleware-keycloak-auth)

A middleware for [Actix Web](https://actix.rs/) that handles authentication with a JWT emitted by [Keycloak](https://www.keycloak.org/).

## Features

- Actix Web middleware
- deny HTTP requests that do not provide a valid JWT
- require one or several Keycloak realm or client roles to be included in the JWT
- error HTTP responses sent from the middleware can have generic bodies as well as detailed error reasons
- access JWT claims from handlers (for example: get the ID of the authenticated user)
- access parsed roles from handlers (every Keycloak role contained in the JWT)
- compatible with [paperclip](https://crates.io/crates/paperclip) using the `paperclip_compat` feature
- store auth status in request-local data instead of returning a HTTP response (so that the next middleware/handler can try another auth mechanism, for example)

## Usage

- [Documentation](https://docs.rs/actix-web-middleware-keycloak-auth)
- [Examples](examples/)

## License

MIT License Copyright (c) 2020 David Sferruzza

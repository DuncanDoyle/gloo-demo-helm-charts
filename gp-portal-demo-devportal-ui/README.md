# Gloo Platform Portal Demo DevPortal-UI

## Running the chart:

Install using the following Helm command.

```
$ helm install gp-portal-demo-devportal-ui .
```

To uninstall, simply run:
```
$ helm uninstall gp-portal-demo-devportal-ui .
```

## Configuring the DevPortal UI
You can use the following helm values to configure the DevPortal-UI```
* `portal_server.url`: Endpoint of the Gloo Platform Portal REST API. Defaults to `http://developer.example.com/v1`.
* `oauth.client_id`: Client-ID of the OAuth client used for the Authorization Code Flow with PKCE. Defaults to `portal-client`.
* `oauth.token_endpoint`: OAuth token endpoint on the IDP. Defaults to `http://keycloak.example.com/realms/master/protocol/openid-connect/token`.
* `oauth.auth_endpoint`: OAuth auth endpoint on the IDP. Defaults to `http://keycloak.example.com/realms/master/protocol/openid-connect/auth`.
* `oauth.logout_endpoint`: OAuth logout endpoint on the IDP. Defaults to `http://keycloak.example.com/realms/master/protocol/openid-connect/logout`/
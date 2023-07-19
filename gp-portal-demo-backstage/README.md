# Gloo Platform Portal Demo Backstage

A simple Helm chart which installs the Gloo Platform Portal Backstage developer platform for PoC, Workshops and Demo environments.

## Install

First, add the `ddoyle-gloo-demo` Helm repo to your repository list:
```
helm repo add ddoyle-gloo-demo https://duncandoyle.github.io/gloo-demo-helm-charts
```

And install using the following command:
```
helm install gp-portal-demo-backstage ddoyle-gloo-demo/gp-portal-demo-backstage --namespace backstage --version 0.1.0
```

## Uninstall

To uninstall, simply run:
```
$ helm uninstall gp-portal-demo-backstage --namespace backstage
```

## Configuring Backstage
You can use the following helm values to configure Backstage:

* `portal_server.url`: Endpoint of the Gloo Platform Portal REST API. Defaults to `http://developer.example.com/v1`.
* `oauth.client_id`: Client-ID of the OAuth client used for the Authorization Code Flow with PKCE. Defaults to `portal-client`.
* `oauth.token_endpoint`: OAuth token endpoint on the IDP. Defaults to `http://keycloak.example.com/realms/master/protocol/openid-connect/token`.
* `oauth.auth_endpoint`: OAuth auth endpoint on the IDP. Defaults to `http://keycloak.example.com/realms/master/protocol/openid-connect/auth`.
* `oauth.logout_endpoint`: OAuth logout endpoint on the IDP. Defaults to `http://keycloak.example.com/realms/master/protocol/openid-connect/logout`/

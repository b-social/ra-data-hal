# @kroo-web/ra-data-hal

A HAL data provider for react-admin.

This supersedes the unscoped `ra-data-hal` package, which is no longer
maintained and stops at 2.7.1.

## Installation

```bash
npm install --save @kroo-web/ra-data-hal
```

## Query parameters

Pass a `queryParams` object in the params to send extra query parameters with a
request. It is merged into the params used to resolve the link, so anything the
link declares as a template variable is expanded into the URL and anything else
is sent as a query string.

```js
dataProvider(GET_ONE, 'accounts', {
  id: accountId,
  queryParams: { includeBalances: 'true' }
})
// GET /accounts/<id>?includeBalances=true
```

Supported on `GET_LIST`, `GET_ONE`, `GET_MANY`, `GET_MANY_REFERENCE` and
`DELETE`. On `GET_LIST` and `GET_MANY_REFERENCE` it is merged alongside the
pagination, sort and filter parameters.

## Development

To run all tests:

```bash
npm run test
```

To run all pre-publish checks:

```bash
npm run prepublishOnly
```

To publish:

```bash
npm publish
```
# reproduce-tsx-338

tsx not work with yarn

## expected

No error.

## actual

```sh
$ yarn test

node:internal/process/esm_loader:40
      internalBinding('errors').triggerUncaughtException(
                                ^
TypeError [ERR_INVALID_RETURN_PROPERTY_VALUE]: Expected array buffer, or typed array to be returned for the "source" from the "transformSource" function but got undefined.
    at __node_internal_captureLargerStackTrace (node:internal/errors:497:5)
    at new NodeError (node:internal/errors:406:5)
    at assertBufferSource (node:internal/modules/esm/translators:84:9)
    at stringify (node:internal/modules/esm/translators:94:3)
    at createCJSModuleWrap (node:internal/modules/esm/translators:219:12)
    at ModuleLoader.commonjsStrategy (node:internal/modules/esm/translators:297:10) {
  code: 'ERR_INVALID_RETURN_PROPERTY_VALUE'
}

Node.js v20.8.0
$ 
```
# Wait For Response docker action

This action makes a HEAD requests to a given URL until the required response code is retrieved or the timeout is met.  Initially created to allow test containers to startup before executing tests against them.

## Versions
GO => 1.17

## Inputs

### `url`

The URL to poll. Default `"http://localhost/"`


### `responseCode`

Response code to wait for. Default `"200"`

### `timeout`

Timeout before giving up in milliseconds. Default `"30000"`

### `interval`

Interval between polling in ms. Default `"200"`
        default: 200

## Example usage
```
uses: APina03/wait_for_response@master
with:
  url: 'http://localhost:8081/'
  responseCode: 200
  timeout: 2000
  interval: 500
```

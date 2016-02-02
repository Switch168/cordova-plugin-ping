
# cordova-plugin-ping

This plugin defines a global `ping` object.
Although the object is in the global scope, it is not available until after the `deviceready` event.

```js
document.addEventListener('deviceready', onDeviceReady, false);
function onDeviceReady() {
  var p = new ping(['github.com', 'undefineddomain.com']);
  console.log(p.results);
}
```

## Installation

> cordova plugin add https://github.com/t1st3/cordova-plugin-ping.git

## Properties

- ping.results

## ping.results

Get the the results of the`ping`.

Results look like this:

```json
[
  {
    "ip": "github.com",
    "ping": "success",
    "avg": 40.131
  },
  {
    "ip": "undefineddomain.com",
    "ping": "timeout",
    "avg": 0
  }
]
```

### Supported Platforms

- Android

# memory-store [![build status][1]][2]

Session store in memory, for use with [routil-session][3]

## Example

    var store = require("memory-store")
        , assert = require("assert")

    store.set("foo", "bar")
    assert.equal(store.get("foo"), "bar")
    store.delete("foo")
    assert.equal(store.get("foo"), null)
  
    var data = store.getAll();
    
    for(key in data) {
      console.log(key, data[key]);
    }

    var otherStore = store.createStore()

## Installation

`npm install memory-store`

## Tests

`make test`

## Contributors

 - Raynos
 - Felipe Barros Cruz

## MIT Licenced

  [1]: https://secure.travis-ci.org/Raynos/memory-store.png
  [2]: http://travis-ci.org/Raynos/memory-store
  [3]: http://github.com/Raynos/routil-session
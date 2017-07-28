# state-manager

A Polymer Element that manages search and filter states saved in an elasticsearch index.

### Example
```js
var buildPopupDataFunction = function(collection) {
  return collection;
};

var buildStateDataFunction = function(collection) {
  return {
    property1: collection.property1 || [],
    property2: collection.property2 || [],
    property3: collection.property3 || [],
    property4: collection.property4 || [],
    property5: collection.property5 || []
  };
};

var collection = {
  property1: [],
  property2: ['item1'],
  property3: ['item2', 'item3'],
  property4: ['item4']
};

var processRequest = true;
```

```html
<state-manager
  build-popup-data-function="[[buildPopupDataFunction]]"
  build-state-data-function="[[buildStateDataFunction]]"
  client="[[elasticsearchClient]]"
  state-index="states"
  state-type="state"
  collection="{{collection}}"
  has-history="{{hasHistory}}"
  process-request="{{processRequest}}"
  state-history="{{stateHistory}}"
  state-id="{{stateId}}">
</state-manager>
```

### Dependencies

Dependencies are installed using [Bower](http://bower.io/):

    npm install -g bower
    bower install

### Testing

Tests are run using [web-component-tester](https://github.com/Polymer/web-component-tester):

    npm install -g web-component-tester
    wct

### Demonstration & Documentation

Demonstration and documentation are viewed using [polyserve](https://github.com/PolymerLabs/polyserve):

    npm install -g polyserve
    polyserve


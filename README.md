# super-db-crud
You don't need to implement your db-interface more than once

## intent

Creating a usable db service should be as easy as:

```javascript
var rethinkdbCrud = require('super-db-crud').rethinkdb; //or .mongodb

var UserCrud = module.exports = rethinkdbCrud({
  collectionName: 'users',
  requiredFields: ['email'],
  checkFormat: {
    email: ['email']
  }
});
```

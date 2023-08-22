# Node.js

## require / importing

require = importing what module or file exports

Importing always resolves to one single valid js value

So the imported value it will always represent a single value

- an array
- an object
- a function
- a number
- a string
- undefined
- null

You can require a file path or the name of module
example

```
const value1 = require('./file_name');
const value2 = require('../nested_folder/file_name');
const value3 = require('module_name');
```

## module.exports / exporting

From a javascript file you can export a single value using
`module.exports = `

The common pattern is to export a single object with key-values such as

```
module.exports = {
  string_value: "1234"
  function_key: function () {},
  object_key: {
    a1: 12341
  },
  array_key: [
    1,
    2,
    3,
    5
  ]
};
```

So even though we may only export a single value

We can export many values by exporting an object with many key-values

## module patterns

It is quite common to group together code by its functionality, responsibility or purpose.

We put all routes in routes folder.

Each file in the routes folder exports a single router.

We put all controllers in a controllers folder.

Each file in the controllers folder exports a single controller.

We put all models in the models folder.

Each file in the models folder exports a single model.

Though each module is only allowed to export a single value such as an object.

We can define many key-values on that exported single object.

For models we can add methods(keys on an object where the value is a function). This will allow us to group together methods together into a model module that is easily consumed from the controllers we define.

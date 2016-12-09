# meanie-multer-mime-types-filter

[![npm version](https://img.shields.io/npm/v/meanie-multer-mime-types-filter.svg)](https://www.npmjs.com/package/meanie-multer-mime-types-filter)
[![node dependencies](https://david-dm.org/meanie/multer-mime-types-filter.svg)](https://david-dm.org/meanie/multer-mime-types-filter)
[![github issues](https://img.shields.io/github/issues/meanie/multer-mime-types-filter.svg)](https://github.com/meanie/multer-mime-types-filter/issues)
[![codacy](https://img.shields.io/codacy/c0decdb116194cc9b1e7c1d53b6a8b3d.svg)](https://www.codacy.com/app/meanie/multer-mime-types-filter)


Simple helper to create a mime types filter for Multer given an array of mime types

![Meanie](https://raw.githubusercontent.com/meanie/meanie/master/meanie-logo-full.png)

## Installation

You can install this package using `npm`.

```shell
npm install meanie-multer-mime-types-filter --save
```

## Usage

```js
let multer = require('multer');
let mimeTypesFilter = require('meanie-multer-mime-types-filter');

/**
 * Upload middleware
 */
upload(req, res, next) {

  //Get locals
  const MIME_TYPES = ['image/jpeg', 'image/png', 'image/gif'];

  //Create upload middleware
  let upload = multer({
    storage: multer.memoryStorage(),
    fileFilter: mimeTypesFilter(MIME_TYPES),
  }).single('file');

  //Use middleware
  upload(req, res, next);
}  
```

## Issues & feature requests

Please report any bugs, issues, suggestions and feature requests in the [meanie-multer-mime-types-filter issue tracker](https://github.com/meanie/multer-mime-types-filter/issues).

## Contributing

Pull requests are welcome! If you would like to contribute to Meanie, please check out the [Meanie contributing guidelines](https://github.com/meanie/meanie/blob/master/CONTRIBUTING.md).

## Credits

* Meanie logo designed by [Quan-Lin Sim](mailto:quan.lin.sim+meanie@gmail.com)

## License
(MIT License)

Copyright 2016-2017, [Adam Reis](http://adam.reis.nz)

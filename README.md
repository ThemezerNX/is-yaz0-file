# is-yaz0-file

Checks if the file path is yaz0 file. It does not read the complete file nor does it depend on the file extension

### Installation

<!-- Install with [npm](https://www.npmjs.com/):

```sh
$ npm install is-yaz0-file --save
``` -->

### Usage

```javascript
var yaz0_FILE = require('is-yaz0-file');

// If a valid yaz0 file is provided and exists at path specified
yaz0_FILE.isyaz0('temp.sarc', function (err, is) {
	if (err) {
		console.log('Error while checking if file is yaz0 : ' + err);
	} else {
		console.log('Given file is yaz0 : ' + is);
	}
});
//=> Given file is yaz0 : true

// If a valid yaz0 file is provided and exists at path specified
yaz0_FILE.isyaz0Sync('temp.sarc');
//=> true
```

### Clone the repo

```bash
$ git clone https://github.com/Migushthe2nd/is-yaz0-file.git
```

### API

#### isyaz0(path, cb)

This is asynchronous API for checking if file is yaz0. This API takes two parameters:

1. File path which needs to be checked and
2. callback, which is invoked when it checks the file to be yaz0 or not or in case of errors

It throws

1. TypeError if path is not provided or if provided but not of type String or if callback is not provided or if provided but not of type Function
2. FileNotExists error which specified file does not exists.

Callback has two parameters:

1. First parameter is error which is null in case of success
2. Second parameter is boolean value which indicates if file is yaz0 or not

**Example**

```javascript
var yaz0_FILE = require('is-yaz0-file');

// If a valid yaz0 file is provided and exists at path specified
yaz0_FILE.isyaz0('temp.sarc', function (err, is) {
	if (err) {
		console.log('Error while checking if file is yaz0 : ' + err);
	} else {
		console.log('Given file is yaz0 : ' + is);
	}
});
//=> Given file is yaz0 : true
```

#### isyaz0Sync(path)

This is synchronous API for checking if file is yaz0. This API takes one parameter:

1. File path which needs to be checked

It throws

1. TypeError if path is not provided or if provided but not of type String
2. FileNotExists error which specified file does not exists.

It returns
Boolean indicating if file at specified path is yaz0 or not

**Example**

```javascript
var yaz0_FILE = require('is-yaz0-file');

// If a valid yaz0 file is provided and exists at path specified
yaz0_FILE.isyaz0Sync('temp.sarc');
//=> true
```

### Author

**Migush**

-   [github/Migushthe2nd](https://github.com/Migushthe2nd)

## License

MIT

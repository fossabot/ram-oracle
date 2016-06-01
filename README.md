<h1>
  <img alt="ram-oracle logo" title="Ram-Oracle Project" src="https://i.imgur.com/GH3Xr5e.png"/>
</h1>



## About &nbsp; 
This module hash checks the input password against a schema's password in the Oracle database. **Why?** Some database driven Oracle enterprise applications use database schema authentication as application authentication. This module was developed so that other applications using the same database can mirror the same authentication. The Oracle hash of the schema & database password is stored in the [PASSWORD] column in the [SYS.USER$] table. To check the password you will need the schema, password, and input password.


## Installation

```sh
$ npm install ram-oracle
```

### Usage

```js
var ram = require('ram-oracle');

//.match(<ORACLE SCHEMA>,<ORACLE PASSWORD>,<INPUT PASSWORD>)
var matches = ram.match('JDOE','587F72032A3C828E','password');
console.log('The input matches the Oracle Database password: ' + matches + '.');

var matches = ram.match('JDOE','587F72032A3C828E','incorrect_password');
console.log('The input matches the Oracle Database password: ' + matches + '.');
```

## License

MIT &copy; 2016 Dee Clawson.

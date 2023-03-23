# mysql-error-keys

A list of error keys(string) in Mysql for code assistant

You can handle key of error codes as constants to avoid bugs.

## Usage

```bash
$ npm install --save mysql-error-keys
```
or
```bash
$ yarn add mysql-error-keys
```

### Typescript
```javascript

import { MysqlErrorKeys } from 'mysql-error-keys';

console.log( MysqlErrorKeys.ER_DUP_ENTRY );

```
or
```javascript

import { ER_DUP_ENTRY } from 'mysql-error-keys';

console.log( ER_DUP_ENTRY );

```

### Javascript
```javascript

const MysqlErrorKeys = require('mysql-error-keys')

console.log(MysqlErrorKeys.ER_DUP_ENTRY);

```
or

```javascript

const { ER_DUP_ENTRY } = require('mysql-error-keys')

console.log(ER_DUP_ENTRY);
```

## License

MIT

[Error Message Reference](https://dev.mysql.com/doc/refman/8.0/en/error-reference.html)
# mysql-error-codes

A list of error keys in Mysql

## Usage

```bash
$ npm install --save mysql-error-keys
```

### Typescript
```javascript

import { MysqlErrorKeys } from 'mysql-error-keys';

console.log( MysqlErrorKeys.ER_DUP_ENTRY );

```

### Javascript (node)
```javascript

const MysqlErrorKeys = require('mysql-error-keys')

console.log(MysqlErrorKeys.ER_DUP_ENTRY);

```

## License

MIT

[Error Message Reference](https://dev.mysql.com/doc/refman/8.0/en/error-reference.html)
# mysql-error-keys

[![NPM Version](https://img.shields.io/npm/v/mysql-error-keys.svg)](https://www.npmjs.com/package/mysql-error-keys)
[![NPM Downloads](https://img.shields.io/npm/dt/mysql-error-keys.svg?style=flat)](https://www.npmjs.com/package/mysql-error-keys)
[![NPM License](https://img.shields.io/npm/l/mysql-error-keys.svg?style=flat)](https://github.com/prettyblueberry/mysql-error-keys/blob/main/LICENSE)
[![Issues](https://img.shields.io/github/issues-raw/prettyblueberry/mysql-error-keys.svg?maxAge=25000)](https://github.com/prettyblueberry/mysql-error-keys/issues)

[//]: # ([![npm]&#40;https://img.shields.io/github/stars/prettyblueberry/mysql-error-keys.svg&#41;]&#40;https://github.com/prettyblueberry/mysql-error-keys&#41;)
[//]: # ([![fork]&#40;https://img.shields.io/github/forks/prettyblueberry/mysql-error-keys.svg&#41;]&#40;https://github.com/prettyblueberry/mysql-error-keys/fork&#41;)

A list of error key(string, not number) of `MySQL error messages`.

MySQL has lots of error messages, and it makes you to handle many raw key strings or code numbers in your coding.
Here is an example.
```javascript
authController.signUp({name, email, pwd}).then((res)=>{
    console.log("success!");
}).catch((err)=>{
    if(err.response.data.code === "ER_DUP_ENTRY"){ // this is raw string :(
        console.log("error: email duplicated!");
        return;
    }
});
```
As you can see, the code uses raw string "ER_DUP_ENTRY". It is not good for coding style and quality.

If you use this list, you can handle error keys as predefined constants to avoid bugs and for better coding style, and you can experience autocomplete of the list in editor of IDEs like `Visual Studio Code` and `JetBrains WebStorm`.

## Install

```bash
$ npm install --save mysql-error-keys
```
or
```bash
$ yarn add mysql-error-keys
```

## Usage

### Using Import
```javascript
import { mek } from 'mysql-error-keys';

authController.signUp({name, email, pwd}).then((res)=>{
    console.log("success!");
}).catch((err)=>{
    if(err.response.data.code === mek.ER_DUP_ENTRY){
        console.log("error: email duplicated!");
        return;
    }
});
```
or
```javascript
import { ER_DUP_ENTRY } from 'mysql-error-keys';

authController.signUp({name, email, pwd}).then((res)=>{
    console.log("success!");
}).catch((err)=>{
    if(err.response.data.code === ER_DUP_ENTRY){
        console.log("error: email duplicated!");
        return;
    }
});
```

### Using Require
```javascript
const mek = require('mysql-error-keys')
authController.signUp({name, email, pwd}).then((res)=>{
    console.log("success!");
}).catch((err)=>{
    if(err.response.data.code === mek.ER_DUP_ENTRY){
        console.log("error: email duplicated!");
        return;
    }
});
```
or

```javascript
const { ER_DUP_ENTRY } = require('mysql-error-keys')

authController.signUp({name, email, pwd}).then((res)=>{
    console.log("success!");
}).catch((err)=>{
    if(err.response.data.code === ER_DUP_ENTRY){
        console.log("error: email duplicated!");
        return;
    }
});
```

## Error Message Reference
[MySQL Error Message Reference](https://dev.mysql.com/doc/mysql-errors/8.0/en/server-error-reference.html)


## Please Be a Contributor !
As you know, this module always should be same as the latest version of `MySQL Error Messages`. `MySQL Error Messages` might be updated and I might miss it.

So if you find an issue, please feel free to make a **pull request** and [an issue](https://github.com/prettyblueberry/mysql-error-keys/issues/new).

GitHub Repository: [https://github.com/prettyblueberry/mysql-error-keys](https://github.com/prettyblueberry/mysql-error-keys)


## License

MIT

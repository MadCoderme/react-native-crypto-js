# React Native CryptoJS

React native javascript library of crypto js.

## Install

```bash
npm install react-native-crypto-js --save
```

## API

See: https://cryptojs.gitbook.io/docs/

### Example Encryption

#### Plain text encryption

```javascript
import CryptoJS from "react-native-crypto-js";

// Encrypt
let ciphertext = CryptoJS.AES.encrypt('my message', 'secret key 123').toString();

// Decrypt
let bytes  = CryptoJS.AES.decrypt(ciphertext, 'secret key 123');
let originalText = bytes.toString(CryptoJS.enc.Utf8);

console.log(originalText); // 'my message'
```

#### Object encryption

```javascript
import CryptoJS from "react-native-crypto-js";

let data = [{id: 1}, {id: 2}]

// Encrypt
let ciphertext = CryptoJS.AES.encrypt(JSON.stringify(data), 'secret key 123').toString();

// Decrypt
let bytes  = CryptoJS.AES.decrypt(ciphertext, 'secret key 123');
let decryptedData = JSON.parse(bytes.toString(CryptoJS.enc.Utf8));

console.log(decryptedData); // [{id: 1}, {id: 2}]
```
### Important
Remember to use the encrypted and decrypted data correctly. Often the output from the encryption or decryption is not in the format you want. You need to turn them into usable formats

### List of Algorithms

#### Hashers

- [x] ```MD5```
- [x] ```SHA1```
- [x] ```SHA256```
- [ ] ```SHA512```
- [x] ```SHA224```
- [ ] ```SHA384```
- [x] ```SHA3```
- [ ] ```RIPEMD160```
---
#### HMAC
- [x] ```HmacMD5```
- [ ] ```HmacSHA1```
- [ ] ```HmacSHA256```
- [ ] ```HmacSHA224```
- [ ] ```HmacSHA512```
- [ ] ```HmacSHA384```
- [ ] ```HmacSHA3```
- [ ] ```HmacRIPEMD160```
---
#### PBKDF2
- [x] ```PBKDF2```
---
#### Ciphers
- [x] ```AES```
- [ ] ```DES```
- [ ] ```TripleDES```
- [ ] ```RC4```
- [ ] ```RC4Drop```
- [x] ```Rabbit```

## Reporting Issues

[Bugs | New Features](https://github.com/MadCoderme/react-native-crypto-js/issues)


## Contributing
Check the issues and pull requests to see if the idea or bug you want to share about is already present. If you don't see it, do one of the following:

* If it is a small change, just fork the project and create a pull request.
* If it is major, start by opening an issue.


## This is a fork and updated repo of https://github.com/imchintan/react-native-crypto-js


## License

Please see [LICENSE](LICENSE) for more info.

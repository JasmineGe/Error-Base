>const ZERO = BigInt(0)

>ReferenceError: BigInt is not defined
    at Object.<anonymous> (E:\ROYALE\xero_api\node_modules\jose\lib\help\rsa_primes.js:8:14)
    at Module._compile (module.js:624:30)
    at Object.Module._extensions..js (module.js:635:10)
    at Module.load (module.js:545:32)
    at tryModuleLoad (module.js:508:12)
    at Function.Module._load (module.js:500:3)
    at Module.require (module.js:568:17)
    at require (internal/module.js:11:18)
    at Object.<anonymous> (E:\ROYALE\xero_api\node_modules\jose\lib\help\key_utils.js:11:23)
    at Module._compile (module.js:624:30)

解决办法：有可能是node版本过低，升级一下node版本
>UnhandledPromiseRejectionWarning: TypeError [ERR_INVALID_ARG_TYPE]: The "chunk" argument must be one of type string or Buffer. Received type object
    at ServerResponse.end (_http_outgoing.js:690:13)

Nodejs的res.end返回数据只能是字符串类型或者Buffer对象类型,我因为用的对象类型而报错

解决办法：用JSON.stringify()将返回的数据转成JSON字符串
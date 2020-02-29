TypeScript "target: es2020" v.s. "lib: es2020" Demo
===========================

`target: es2020`是指生成的js代码满足es2020的规范，所以像`?.`这样的就不会转换。

`target: es6` + `lib: es2020`，是指生成的js代码满足es6的规范，由于es6不支持`?.`，
所以会自动转换代码。这个语法是由最新的typescript版本支持的，所以并不需要指定`lib: es2020`。

但是由于代码中故意使用了es2019中才有的`.flat()`函数，所以必须加上`lib: es2019`提供相应的typing，
该代码才能通过类型检查。本demo中由于已经添加了es2020，已经足够

```
cd lib-es2020
npm install
npm run compile
```

```
cd target-es2020
npm install
npm run compile
```

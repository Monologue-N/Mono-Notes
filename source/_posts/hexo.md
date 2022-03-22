---
title: Error ENOENT, no such file or directory, scandir
date: 2022-03-22 16:10:20
tags: 'hexo开发'
---
在开发的时候遇到了一个问题，当我在 'themes/archer' 目录下执行
```bash
    npm run build
```
的时候，terminal给我显示了：
```shell script
> hexo-theme-archer@1.6.4 build /Users/Clarisse/Developer/My-Notes/themes/archer
> gulp build --option

Error: ENOENT: no such file or directory, scandir '/Users/Clarisse/Developer/My-Notes/themes/archer/node_modules/node-sass/vendor'
    at Object.readdirSync (fs.js:1021:3)
    at Object.getInstalledBinaries (/Users/Clarisse/Developer/My-Notes/themes/archer/node_modules/node-sass/lib/extensions.js:134:13)
    at foundBinariesList (/Users/Clarisse/Developer/My-Notes/themes/archer/node_modules/node-sass/lib/errors.js:20:15)
    at foundBinaries (/Users/Clarisse/Developer/My-Notes/themes/archer/node_modules/node-sass/lib/errors.js:15:5)
    at Object.module.exports.missingBinary (/Users/Clarisse/Developer/My-Notes/themes/archer/node_modules/node-sass/lib/errors.js:45:5)
    at module.exports (/Users/Clarisse/Developer/My-Notes/themes/archer/node_modules/node-sass/lib/binding.js:15:30)
    at Object.<anonymous> (/Users/Clarisse/Developer/My-Notes/themes/archer/node_modules/node-sass/lib/index.js:13:35)
    at Module._compile (internal/modules/cjs/loader.js:1063:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:1092:10)
    at Module.load (internal/modules/cjs/loader.js:928:32) {
  errno: -2,
  syscall: 'scandir',
  code: 'ENOENT',
  path: '/Users/Clarisse/Developer/My-Notes/themes/archer/node_modules/node-sass/vendor'
}
npm ERR! code ELIFECYCLE
npm ERR! errno 1
npm ERR! hexo-theme-archer@1.6.4 build: `gulp build --option`
npm ERR! Exit status 1
npm ERR! 
npm ERR! Failed at the hexo-theme-archer@1.6.4 build script.
npm ERR! This is probably not a problem with npm. There is likely additional logging output above.

npm ERR! A complete log of this run can be found in:
npm ERR!     /Users/Clarisse/.npm/_logs/2022-03-22T23_02_11_295Z-debug.log

```
这样的报错……

**解决方案：**
删除 'themes/archer' 目录下的 node_modules，并重新执行：
```bash
    npm install
    npm run build
```
Reference: [Error: ENOENT: no such file or directory, scandir '**/node_modules/node-sass/vendor' #1579](https://github.com/sass/node-sass/issues/1579)

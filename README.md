https://web.dev/commonjs-larger-bundles/


| lodash<br>package & version | webpack<br>version                 | CommonJS<br>bundle size | ES Modules<br>bundle size |
|-----------------------------|:-----------------------------------|------------------------:|--------------------------:|
| lodash-es@4.17.21           | webpack@4.46.0, webpack-cli@3.3.12 |                  102284 |                      9576 |
| lodash-es@4.17.21           | webpack@5.74.0, webpack-cli@4.10.0 |                   14511 |                        38 |
| lodash@4.17.21              | webpack@5.74.0, webpack-cli@4.10.0 |                   70908 |                     70851 |
```shell
# webpack-cli v3
$ node_modules/.bin/webpack --mode production --entry ./commonjs/index.js --output ./dist/cjs.js
$ node_modules/.bin/webpack --mode production --entry ./esmodules/index.js --output ./dist/esm.js
# webpack-cli v4
$ node_modules/.bin/webpack --mode production --entry ./commonjs/index.js --output-path ./dist --output-filename cjs.js
$ node_modules/.bin/webpack --mode production --entry ./esmodules/index.js --output-path ./dist --output-filename esm.js
$ ls -l dist/
```

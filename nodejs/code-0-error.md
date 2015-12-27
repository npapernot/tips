# Code 0 error on `npm install`

```
> phantomjs@1.9.19 install
> node install.js

sh: 1: node: not found
npm WARN This failure might be due to the use of legacy binary "node"
npm WARN For further explanations, please read
/usr/share/doc/nodejs/README.Debian
 
npm ERR! weird error 127
npm ERR! not ok code 0
```

solved by created a sym link

```
sudo ln -s /usr/bin/nodejs /usr/bin/node
```

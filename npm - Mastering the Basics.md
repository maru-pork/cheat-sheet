**npm** 
- [ ] package manager for javascript  
- [ ] reusable code -- modules  

```
npm --help
npm install -help
npm help --search install
```

***package.json***
- [ ] manage dependencies
- [ ] scripts (initial build)

```
npm init
npm init --yes
npm config set init-author-name shajeemaru
npm config set init-license MIT
```

**Local Packages**
*see project/node_modules*
```
npm install/uninstall moment
```
*Production dependencies*
```
npm install moment --save
npm uninstall moment --save
```
*Development dependencies*
```
npm install lodash --save-dev
npm uninstall lodash --save-dev
```

**Global Packages**  *see nodejs/node_modules*
```
npm install moment -g
npm uninstall/remove/rm/un moment -g
```

**List dependencies**
```
npm list
npm list --depth 1
npm list --global --depth 0
```

**Versioning**
```
npm install moment@2.23.0 --save
npm install moment@2.22 --save
npm install moment@2 --save
```

***Package.json***
```
npm install
```

```
"lodash": "^4.14.1"  // 4.16.1
"lodash": "~4.14.1"  // 4.14.2
"lodash": "4.14.1"  // 4.14.1
"lodash": "*"
```

update specific module
```
npm update moment --save
```

update dev dependencies
```
npm update --dev --save-dev
```

update all dependencies
```
npm update
```

update global packages
```
npm update -g
```

update specific global package
```
npm update -g gulp
```

update npm version to latest
```
npm install npm@latest -g
```

remove extraneous modules from the project/node_modules
```
npm prune
```


**See:**  
https://docs.npmjs.com/misc/config


**npm Scripts**
```
"scripts": {
    "start": "node app.js"
  },
```

```
npm run start
```



*Reference:* [Udemy](https://www.udemy.com/npm-mastering-the-basics/)

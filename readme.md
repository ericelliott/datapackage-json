## datapackage-json

module to manage a package.json for Simple Data Format packages 

### installation

[![NPM](https://nodei.co/npm/datapackage-json.png)](https://nodei.co/npm/datapackage-json/)

```
npm install datapackage-json -g
```

### usage

```
datapackage-json init
datapackage-json default
```

`default` generates a default package.json from the prompt script without using a prompt (just gets default values)

`init` asks the user for values and creates a `package.json` from it

### api

### var pkg = datapackage([promptFile, dir])

both arguments are optional. `promptFile` must be a PromZard prompt script, `dir` is the folder where the magic should happen, default is `cwd`.

#### pkg.init()

prompts CLI user using promzard for package.json fields, and then writes the result out to `package.json`

#### pkg.default(callback)

generates a default package.json from the prompt script without using a prompt (just gets default values)

calls `callback` with `(err, defaults)`

#### pkg.write(obj, [saveTarget, cb])

takes `obj` and writes it as a nicely formatted JSON object to `saveTarget` (default `saveTarget` is just `./package.json`). calls optional `cb` with `(err)`

### license

BSD

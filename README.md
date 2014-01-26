# grunt-crane-builder

Grunt Crane Builder, which is for G.js.

## Installation

```shell
npm install grunt-crane-builder --save-dev
```

## Usage

Once the plugin has been installed, specify your gruntfile like this:

```
grunt.initConfig({
    rootpaths: ["http://sta.yongshei.com"],
    src: "src/",
    dest: "amd/",
    temp: "temp/",
    cacheExpire: 604800000,
    versionTemplate: "<%= url.href.replace(url.ext, '.__' + version + '__' + url.ext) %>",
    builder: [
        ["somefile", require("grunt-crane-builder/builder/nothing")],
    ],
};

grunt.loadNpmTasks('grunt-crane-builder');
```

Then, you can build or watch your files:

```
# to build your files
grunt crane_build
```

```
# to build one file in src
grunt crane_build:some.js
```

```
# to watch changed files
grunt crane_watch
```
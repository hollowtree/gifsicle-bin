# gifsicle-bin ![GitHub Actions Status](https://github.com/imagemin/gifsicle-bin/workflows/test/badge.svg?branch=master)

> gifsicle manipulates GIF image files in many different ways. Depending on command line options, it can merge several GIFs into a GIF animation; explode an animation into its component frames; change individual frames in an animation; turn interlacing on and off; add transparency and much more.

You probably want [`imagemin-gifsicle`](https://github.com/imagemin/imagemin-gifsicle) instead.


## Install

```
$ npm install gifsicle
```

### Downloading From a Custom Source
By default, this package will download gifsicle from GitHub. To use a custom source, set the npm config property `imagemin_local_url`. The downloader will append `/<name>/<version>/vendor/<dist>`.

```
$ npm install gifsicle --imagemin_local_url=https://mymirror.local/path
```

Or add property into your `.npmrc` file([https://docs.npmjs.com/files/npmrc](https://docs.npmjs.com/files/npmrc))

```
imagemin_local_url=https://mymirror.local/path
```

Another option is to use the environment variable `IMAGEMIN_LOCAL_URL`.

```
$ IMAGEMIN_LOCAL_URL=https://mymirror.local/path npm install gifsicle
```


## Usage

```js
const {execFile} = require('child_process');
const gifsicle = require('gifsicle');

execFile(gifsicle, ['-o', 'output.gif', 'input.gif'], err => {
	console.log('Image minified!');
});
```


## CLI

```
$ npm install --global gifsicle
```

```
$ gifsicle --help
```


## License

MIT © [Imagemin](https://github.com/imagemin)

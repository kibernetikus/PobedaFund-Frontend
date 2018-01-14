frontend-boilerplate
====================

[![styled with prettier](https://img.shields.io/badge/styled_with-prettier-ff69b4.svg)](https://github.com/prettier/prettier)

> An ES201X starter with common frontend tasks using [Webpack 3](https://webpack.js.org/) as module bundler and npm scripts as task runner.

For an older version with Gulp 4, see [1.6.2](https://github.com/dmnsgn/frontend-boilerplate/releases/tag/1.6.2).

## Setup
### Requirements

Node `">=5.0.0"` (use brew or install it from [here](http://nodejs.org/download/))

```bash
brew install node
```

### Clone the repository

*OSX & Linux*

```bash
git clone --depth 1 https://github.com/dmnsgn/frontend-boilerplate.git && cd frontend-boilerplate && rm -rf .git && git init
```

*Windows*

```bash
git clone --depth 1 https://github.com/dmnsgn/frontend-boilerplate.git && cd frontend-boilerplate && rd /s /q .git && git init
```

### Dependencies

```bash
npm install
```

### Configuration

Open `config/config.js`:

|Key|Description|Type
|:-|:-|:-:|
|**PATHS**|map of paths to the differents folders needed by `webpack` and `npm scripts`|Map
|**BROWSERS**|the browsers targeted for `babel-preset-env` and `autoprefixer` (see full list [here](https://github.com/ai/browserslist))|Array


Open `package.json`:

|Key|Description|Type
|:-|:-|:-:|
|**description**|title used for metas, favicons and banner|String
|**homepage**|absolute url used for metas, robotstxt, sitemap and banner|String
|**license**|license acronym used for banner|String
|**author.name**|author name used for favicons|String
|**author.url**|author url used for favicons|String
|**config.title**|title used for metas and favicons|String
|**config.handle**|twitter handle for metas|String
|**config.analyticsUA**|google analytics UA|String

## Develop

```bash
npm run dev
```

## Production

```bash
npm run prod
```

## Features

### Webpack [loaders](https://webpack.js.org/loaders/):

* [Babel](https://babeljs.io/)
* [Typescript](https://www.typescriptlang.org/)
* [PostCSS](https://github.com/postcss/postcss): see [postcss.config.js](./config/postcss.config.js)
* [Sass](http://sass-lang.com/)
* [Less](http://lesscss.org/)
* [Stylus](http://stylus-lang.com/)
* fonts via [file-loader](https://github.com/webpack-contrib/file-loader)
* optimised images via [file-loader](https://github.com/webpack-contrib/file-loader)
* [html-loader](https://github.com/webpack-contrib/html-loader)
* [glslify](https://github.com/stackgl/glslify)

### Webpack [plugins](https://webpack.js.org/plugins/):

* [DefinePlugin](https://webpack.js.org/plugins/define-plugin/): create global constants which can be configured at compile time
* [HotModuleReplacementPlugin](https://webpack.js.org/plugins/hot-module-replacement-plugin/): enable Hot Module Replacement
* [NamedModulesPlugin](https://webpack.js.org/guides/caching/#deterministic-hashes)
* [HtmlWebpackPlugin](https://webpack.js.org/plugins/html-webpack-plugin/) with [.ejs](http://ejs.co/) templates: simplify creation of HTML files
* [ExtractTextWebpackPlugin](https://webpack.js.org/plugins/extract-text-webpack-plugin/): extract text from a bundle, or bundles, into a separate file.
* [SpritesmithPlugin](https://github.com/mixtur/webpack-spritesmith): convert a set of images into a spritesheet and SASS/LESS/Stylus mixins
* [CommonsChunkPlugin](https://webpack.js.org/plugins/commons-chunk-plugin/): opt-in feature that creates a separate file (known as a chunk), consisting of common modules shared between multiple entry points.
* [UglifyjsWebpackPlugin](https://webpack.js.org/plugins/uglifyjs-webpack-plugin/) from webpack
* [BannerPlugin](https://webpack.js.org/plugins/banner-plugin/): add a banner to the top of each generated chunk.
* [NpmInstallWebpackPlugin](https://webpack.js.org/plugins/npm-install-webpack-plugin/): speed up development by automatically installing & saving dependencies with Webpack.
* [WebpackStatsPlugin](https://github.com/FormidableLabs/webpack-stats-plugin): ingest the webpack stats object, process / transform the object and write out to a file for further consumption.

### npm scripts:

* `npm run clean`: remove all the files from the `dist` directory
* `npm run favicons`: generate [favicons](https://github.com/evilebottnawi/favicons) files and `/src/templates/_favicons.ejs`
* `npm run robotstxt`: generate [robots.txt](https://github.com/itgalaxy/generate-robotstxt) file
* `npm run sitemap`: generate [sitemap.xml](https://github.com/ekalinin/sitemap.js) file

### Prettier [formatter](https://github.com/prettier/prettier):

* [Prettier](https://github.com/prettier/prettier)
* [ESLint Prettier Plugin](https://github.com/prettier/eslint-plugin-prettier)
* [ESLint Prettier Config](https://github.com/prettier/eslint-config-prettier)

## Licence

MIT

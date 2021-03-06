# ng2-vizabi

Native Angular2 directive for [Vizabi](https://github.com/vizabi/vizabi) component.

[Vizabi](https://github.com/Gapminder/vizabi) is a framework for building visual data exploration tools freely provided by Gapminder. WARNING: Vizabi is in alpha. Don't expect too much!

- - -

## Quick start

1. A recommended way to install ***ng2-vizabi*** is through [npm](https://www.npmjs.com/search?q=ng2-vizabi) package manager using the following command:

  `npm i ng2-vizabi --save`

  Alternatively, you can [download it in a ZIP file](https://github.com/vizabi/ng2-vizabi/archive/master.zip).

2. More information regarding using of ***ng2-vizabi*** is located in
  [demo](http://vizabi.github.io/ng2-vizabi/) and [demo sources](https://github.com/vizabi/ng2-vizabi/tree/master/demo).

  To view the demo: clone the repo, run `npm i`, `npm run build`, `npm start`

## API

### Inputs (Properties)

  * `order` (`?number`) - tab order could be useful to indicate tab number in set of tabs
  * `readerModuleObject` (`?any`) - object (separate module that contains method to get reader's object); undefined by default
  * `readerGetMethod` (`?string`) - method name (to get reader's object) in `readerModuleObject`; undefined by default
  * `readerPlugins` (`?any[]`) - parameters for `readerGetMethod` as different kind of objects depending on reader functionality
  * `readerName` (`?string`) - reader's name; undefined by default
  * `chartType` (`string`) - chart type for current `Vizabi` instance
  * `stopUrlRedirect (`?boolean`) - prevents any `window.location` activity
  * `model` (`any`) - model for current `Vizabi` instance
  * `modelHash` (`?string`) - hash (url encoded) with extra data for `model`; undefined by default
  * `active (`?boolean`) - this flag could be useful to indicate active tab of many tabs
  * `language (`?string`) - current language, it might be passed to `Vizabi` as-is
  * `additionalItems` (?any[]) - additional items that should be added as `data_...` section of model: it will be an additional csv file or DDF folder
  * `reloadTime` (`?number`) - put reload time, after that current chart will be reloaded
  * `restoreAfterReload` (`?boolean`) - current chart state will be restored after `reloadTime` activity

### Outputs (Events)

  * `onCreated` - it fires during Vizabi based chart was created successfully
  * `onChanged` - it fires during Vizabi based chart was changed (additional data was added, for example)
  * `onReadyOnce` - happens once on the load when both DOM and MODEL are ready
  * `onClick` - it fires during click was occurred on Vizabi based chart
  * `onError` - it fires during an error was occurred on Vizabi based chart

## NPM Publishing

```
npm run build
cd dist
npm publish
```

Important note. Don't publish this project from root directory.

## gh-pages

If you need to publish demo examples to `gh-pages` you should follow next steps:

```
npm run build
npm run demo.build
cd demo/dist
```

Put content from `demo/dist` to your `gh-pages` branch.

## Troubleshooting

Known problems:
> `npm run build`
> `cp` is not recognized as an internal or external command, operable program or batch file.

You are using windows command prompt that sucks. [Cygwin](http://www.cygwin.com/) solves it. Or use [git bash](https://git-scm.com/). Or use linux/mac.

> `npm run build` fails

try updating your node/npm. Last time i checked the app it was working and i had node v6.10.2, npm v3.10.10

Please follow this guidelines when reporting bugs and feature requests:
1. Use [GitHub Issues](https://github.com/vizabi/ng2-vizabi/issues) board to report bugs and feature requests (not our email address)
2. Please **always** write steps to reproduce the error. That way we can focus on fixing the bug, not scratching our heads trying to reproduce it.

Thanks for understanding!

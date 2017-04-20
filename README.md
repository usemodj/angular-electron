# NPM vs Yarn Cheat Sheet
<https://shift.infinite.red/npm-vs-yarn-cheat-sheet-8755b092e5cc>

npm install taco --save === yarn add taco 
npm uninstall taco --save === yarn remove taco
npm install taco --save-dev === yarn add taco --dev
npm update --save === yarn upgrade 
npm install taco@latest --save === yarn add taco
npm install taco --global === yarn global add taco 

npm init === yarn init
npm link === yarn link
npm outdated === yarn outdated
npm publish === yarn publish
npm run === yarn run
npm cache clean === yarn cache clean
npm login === yarn login (and logout)
npm test === yarn test
npm install --production === yarn --production

- Things yarn has that NPM doesn’t:
`yarn licenses ls`    —  Allows you to inspect the licenses of your dependencies
`yarn licenses generate-disclaimer`   —  Automatically create your license dependency disclaimer
`yarn why taco`   —  Identify why ‘taco’ package is installed, detailing which other packages depend upon it (thanks Olivier Combe).
`yarn upgrade-interactive`   —  Allows you to selectively upgrade specific packages in a simple way



# Angular 2 electron starterkit featuring webpack

A working demo of [electron] with [angular] using [Webpack], [ngrx] and [material2]

This is a starter of angular (2 and above) and electron. Its a demo of oauth with github using angular and electron. It uses [ngrx] to manage state. You should create a config file as following :

```javascript
{
    "github": {
        "client_id": "yourclientID",
        "client_secret": "yoursecretkey",
        "scopes": [
            "user:email",
            "notifications"
        ]
    }
}
```

and place this file inside the "app" folder. Don't use this in production as for production you should have a safe server side URI and not have your secret key in the app folder.  

When running it authenticates the user and goes to a page showing the username received from the authentication oauth workflow.

## Run the example

```bash
$ npm install
$ npm run build
$ npm run watch
$ npm run electron
```
or
```bash
$ yarn 
$ yarn run build
$ yarn run watch
$ yarn run electron
```

## Packaging

The app has support for packaging using 'electron-packager'

```bash
$ npm run package
```

Will run the package for OSX. You can also provide additional options to the package command such as

*  --name : The package name
*  --all : Will packaget the application to all the platforms
*  --arch : Arches to be provided
*  --icon : The icon for the app

## License

[MIT]

[Webpack]: http://webpack.github.io
[MIT]: http://markdalgleish.mit-license.org
[angular]: http://angular.io
[electron]: http://electron.atom.io/
[ngrx]: https://github.com/ngrx/store
[material2]: https://github.com/angular/material2
[electron-packager]: https://github.com/electron-userland/electron-packager

--------------

# Change the following from 'src/app/components/app.theme.scss'
```
// @import '~@angular/material/core/theming/all-theme';
@import '~@angular/material/theming';
```
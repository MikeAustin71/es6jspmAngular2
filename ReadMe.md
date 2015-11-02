# Getting Started With JSPM, Typescript and Angular 2
This is a setup script for a skeleton project.

 * Configuring for ES6, jspm, Typescript and Angular2
 * `jspm Version 0.16.4`
 * `Typescript 1.6.2`
 * `Angular2 2.0.0-alpha.45`

 ## NOTE: ES6 Version Only Works In Chrome


## Setup
 1. mkdir fantasticAppDir && cd fantasticAppDir

 2. Create package.json
    * npm init

 3. Install jspm globally: npm install -g jspm

 4. If you plan to install your jspm packages in a directory other than
    'jspm_packages', create your alternate directory now.
    (Example directory: './lib').

 5. Install jspm locally: npm install jspm --save-dev
    * This allows you to control and lock the version of
        the local jspm installation.
    * Make a note of the local installed jspm version:  jspm -v

 6. Run: jspm init  - Take the defaults except as follows:
    * Source: [https://github.com/jspm/jspm-cli/blob/master/docs/getting-started.md]([https://github.com/jspm/jspm-cli/blob/master/docs/getting-started.md)

    * Take 'Typescript' transpiler option

    * If alternate package installation directory is desired, input new
      directory as per # 5 above.
      (Enter jspm packages folder (.\jspm_packages): RESPOND-> lib<ENTER>)

    * NOTE: If something goes wrong you can always re-run: jspm init -p
    * If you receive an error related to inabililty to access a certificate at
        Program Files\Git\mingw64\libexec\ssl\certs\ca-bundle.crt,
        you may find the certificate at C:\Program Files\Git\mingw64\ssl\certs.
        Just copy the 'ssl' directory to the 'libexec' path.

 7. install dependencies (Note: You may be asked for GitHub Credentials):
    * jspm dl-loader --edge
    * jspm install npm:es6-module-loader
    * jspm install npm:tsd
    * jspm install angular2 reflect-metadata zone.js es6-shim
    * jspm install traceur
    * jspm install npm:@reactivex/rxjs
    * jspm install core-js
    * (optional) jspm install jquery

 8. Modify config.js (ES6 Version)
        * "typescriptOptions" section
            of the config.js file.
        * "packages" section of the config.js file.    
        * "paths" section: note the addtion of
            "app" component.

 9. Create the tsconfig.json file.

 10. Run: tsd init -> setup typings directory

 11. Compile 'main.ts' typescript file.
     * You should receive zero errors.
     * Note I had to add 'use strict' to eliminate the "Block-scoped
       declarations (let, const, function, class) not yet supported
       outside strict mode" error displayed in the Chrome console.

 12. Run the app in your browser. (See below) In the console, you should receive
        zero errors, with two warnings from 'zone'.

***
## Set Up A Server And Run Application
***
### jspm-server
 * make sure jspm-server is installed globally.
jspm install -g jspm-server

 * To display index.html in the Browser->
Run: jspm-server<ENTER>

### http-server
 To display index.html in the Browser->
 * npm install -g http-server

 * (if port 8080 it taken, pick any port that is free)
 * Run: http-server -p 8080<ENTER>

---
## Clone This Repo And Run The Demo App
---
1. Clone the repo to local directory
2. cd localDirectory
3. Run: npm install
4. Run: jspm install
5. See the Section Above: `Set Up A Server And Run Application`

---
## Resources
---
jspm home: [https://jspm.io](https://jspm.io)

jspm and typescript [http://stackoverflow.com/questions/28339100/using-jspm-with-typescript](http://stackoverflow.com/questions/28339100/using-jspm-with-typescript)

typescript angular and jspm samples[https://github.com/Microsoft/TypeScriptSamples](https://github.com/Microsoft/TypeScriptSamples)

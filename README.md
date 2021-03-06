# Base JS App

[![Build Status](https://travis-ci.org/alistairjcbrown/base-js-app.svg?branch=master)](https://travis-ci.org/alistairjcbrown/base-js-app)
[![devDependency Status](https://david-dm.org/alistairjcbrown/base-js-app/dev-status.svg?theme=shields.io)](https://david-dm.org/alistairjcbrown/base-js-app#info=devDependencies)

---

A basic starting point for building a JS app.

 - Third party modules are provided via bower
 - Modules are loaded via RequireJS
 - Testing is provided via Mocha, Chai and Sinon
 - Checks and build are provided via Grunt
 - Application structure is provided via BackboneJS

## Getting started

1. Create a new repositiory in Github


        git@github.com:{username}/{project_name}.git


2. Bare clone this repository


        git clone --bare git@github.com:alistairjcbrown/base-js-app.git


3. Go into the cloned local copy


        cd base-js-app.git


4. Push copy to the newly created repositiory in Github


        git push --mirror git@github.com:{username}/{project_name}.git


5. Remove the local repository which was cloned from


        cd ../
        rm -rf base-js-app.git


6. Clone the new repository


        git clone git@github.com:{username}/{project_name}.git


7. You should now have a new repository which contains source and history from the base repository


## Install

To install the dependencies and run the build, you should have `bower` and `grunt` installed.

```
npm install   # Install build dependencies
bower install # Install app dependencies
grunt build   # Test and build the minified app
```

## Testing

```
grunt go    # Runs linting and tests
# - or -
grunt test  # Runs only tests
```

## Using

 - Add new modules in `js/src/modules/{module_name}`
    - Add tests in `js/tests/modules/{module_name}`
    - Copy the test html file from `js/tests/modules/example/index.test.html`
        - Edit this html file to specify the new test files to run

## Adding a new lib

 - Install from bower - `bower install {lib_name} --save`
 - Update `require.config.js` with a reference from lib name to file location
    - If the lib is non-AMD, consider creating a shim fle in `js/src/core/shim` to remove the lib from the global scope


## Contact

Twitter @alistairjcbrown

Code signed using keybase as alistairjcbrown. Verify with `keybase dir verify`
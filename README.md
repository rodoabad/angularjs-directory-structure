# Directory Structure

*Everything is a module*, well sort of.

## Main

The `main` folder is going to be the folder where you declare your main modules. Think of it as the index folder for a specific part of your application i.e. if you have a user page, then it will be named as the `user` folder and the module's name will be `user`. Every module under this folder will then be have a prefix followed by a dot. Continuing with our example a likely sub module for `user` would be `access` and `settings` which in turn become `user.access` and `user.settings`.

### main.js

```js
import angular from 'angular';
import uiRouter from 'angular-ui-router';

import user from './views/user/index.js';

export default angular.module('main', [uiRouter, user]).name;

```

## User

### index.js

```js
import angular from 'angular';

import config from './config.js';
import template from './index.html';
import controller from './controller.js';

const directive = {
  restrict: 'E',
  template: template
  controller: controller,
  controllerAs: 'vm'
  bindToController: {}
};

export default angular.module('user', [])
  .config(config)
  .directive('user', () => directive)
  .name;

```

### config.js
```js

function config ($stateProvider) {

  const state = {
    name: 'main.user',
    url: 'user',
    views: {
      template: `<user></user>`;
    }
  }
  
  $stateProvider.state(state);

}

export default [
  '$stateProvider',
  config
];

```

## Sample structure

```
src/
├──main/
   │
   ├──common/
   │  │
   │  ├──filters/
   │  │  │
   │  │  ├──filter/
   │  │     │
   │  │     ├──filter.js
   │  │     ├──helpers.js
   │  │   
   │  ├──services/
   │     │
   │     ├──service/
   │        │
   │        ├──service.js
   │        ├──helpers.js
   │  
   │
   ├──views/
   │  │
   │  ├──user/
   │     │
   │     ├──config.js
   │     ├──controller.js
   │     ├──index.js
   │
   ├──main.js
   ├──config.js

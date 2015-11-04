# Directory Structure

*Everything is a module*, well sort of.

## Main

The `main` folder is going to be the folder where you declare your main modules. Think of it as the index folder for a specific part of your application i.e. if you have a user page, then it will be named as the `user` folder and the module's name will be `user`. Every module under this folder will then be have a prefix followed by a dot. Continuing with our example a likely sub module for `user` would be `access` and `settings` which in turn become `user.access` and `user.settings`.

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
   │  │  │
   │  │  ├──service/
   │  │     │
   │  │     ├──service.js
   │  │     ├──helpers.js
   │  │
   ├──packages/
   │  │
   │  ├──package/
   │     │
   │     ├──index.html
   │     ├──package.js
   │     ├──config.js
   │     ├──controller.js
   │     ├──helper.js
   │     ├──service.js
   │
   ├──routes/
   │  │
   │  ├──route/
   │     │
   │     ├──route.js
   │     ├──config.js
   │
   ├──main.js
   ├──config.js

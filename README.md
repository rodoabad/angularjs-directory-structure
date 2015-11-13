# Directory Structure

*Everything is a module*, well sort of.

## The basic structure

An Angular JS web application is mainly driven by views and is either made up of several other views and components. This is the reason why our directory structure will always contain two folders: **components** and **views**. In addition to that, the **views** folder can contain its own set of components and views folder. Think of it as a never ending cycle and will totally depend on how you structure your URLs.

```
src/
├──app/
    ├──components/
    ├──views/
        ├──components/
        ├──views/
            ├──components/
            ├──views/
```

### The components folder

The component folder is your building block for your view, this will usually contain your view's *filters*, *services*, and *directives*.

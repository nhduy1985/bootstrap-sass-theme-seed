bootstrap-sass-theme-seed
=========================

A seed for custom theme for twitter bootstrap with SASS

- Twitter bootstrap: 3.1.1
- Bootstrap SASS: 3.1.1 (https://github.com/twbs/bootstrap-sass)


Installation
============

1. Clone the repo to ``public`` folder
2. Sass compiling

```bash
sass --watch --sourcemap sass:css
```

- ``--watch``: listening for changes and auto-update css files
- ``--sourcemap``: for debuging with Chrome https://coderwall.com/p/tjbktw
- ``sass:css``: compile from directory ``sass`` to directory ``css``

Customize theme
===============

1. Copy a new theme base ``dustin.scss`` from ``sass\themes\base.scss``
2. Create theme folder (same as theme name) at ``sass\themes\``
3. Add override sass files from bootstrap then include it after the bootstrap include in theme base

    ```
    // Core variables and mixins
    @import "../bootstrap/variables";
    @import "basic/variables"; //override some variables of bootstrap
    @import "../bootstrap/mixins";
    ```

*Note that should remove ``!default`` for variables.*
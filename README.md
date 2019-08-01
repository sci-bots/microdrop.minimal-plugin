# Minimal MicroDrop plugin #

This plugin simply logs a message when each step is executed including the
following text:

    doing some work when a step is run

The goal of this plugin is to show the minimum amount of code required to
implement a MicroDrop plugin configured with a callback for step execution.

-------------------------------------------------------------------------------

Install
-------

The latest [`microdrop.minimal-plugin` release][1] is available as a
[Conda][2] package from the [`sci-bots`][2] channel.

To install `microdrop.minimal-plugin` in an **activated Conda environment**, run:

    conda install -c sci-bots -c conda-forge microdrop.minimal-plugin

-------------------------------------------------------------------------------

Develop
-------

 1. Install dependencies listed in `requirements.host` section of
    [`.conda-recipe/meta.yaml`](/.conda-recipe/meta.yaml).
 2. Run the following command from the repository root:
 ```
 python -m mpm.bin.build -p microdrop.minimal-plugin --properties-only -s . -t .
 ```
 3. Select or create directory as root to hold development plugins, e.g.,
 ```
 mkdir %USERPROFILE%\microdrop-dev-plugins
 ```
 4. Create link to repo directory in development root with import-friendly
    **_plugin_** name, e.g.:
 ```sh
 mklink /J %USERPROFILE%\microdrop-dev-plugins\minimal_plugin %REPO_DIR%
 ```
 5. Add development plugins directory to `;`-separated list of paths in
    `MICRODROP_PLUGINS_PATH` environment variable.

-------------------------------------------------------------------------------

License
-------

This project is licensed under the terms of the [BSD license](/LICENSE.md)

-------------------------------------------------------------------------------

Contributors
------------

 - Christian Fobel ([@cfobel](https://github.com/cfobel))


[1]: https://github.com/sci-bots/microdrop.minimal-plugin
[2]: https://anaconda.org/sci-bots/microdrop.minimal-plugin

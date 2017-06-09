[![Project Status: Abandoned – Initial development has started, but there has not yet been a stable, usable release; the project has been abandoned and the author(s) do not intend on continuing development.](http://www.repostatus.org/badges/latest/abandoned.svg)](http://www.repostatus.org/#abandoned)


PyBuilder Header Plugin [![Build Status](https://travis-ci.org/aelgru/pybuilder_header_plugin.svg?branch=master)](https://travis-ci.org/aelgru/pybuilder_header_plugin)
=======================

Ensures that all your source files contain the same file header.

How to use pybuilder_header_plugin
----------------------------------

Add plugin dependency to your `build.py`
```python
use_plugin('pypi:pybuilder_header_plugin')
```

Configure the plugin within your `init` function:
```python
@init
def init(project):
    project.set_property('pybuilder_header_plugin_break_build', True)
    project.set_property('pybuilder_header_plugin_expected_header', "# Copyright\n")
```

This will break the build if one of your source files does not start with the comment line `# Copyright`.

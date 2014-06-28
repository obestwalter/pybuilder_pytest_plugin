pybuilder_header_plugin [![Build Status](https://travis-ci.org/aelgru/pybuilder_header_plugin.svg?branch=master)](https://travis-ci.org/aelgru/pybuilder_header_plugin)
========================

Ensures that all your source files contain the same file header.

How to use pybuilder_header_plugin
----------------------------------

Add plugin dependency to your `build.py`
```
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

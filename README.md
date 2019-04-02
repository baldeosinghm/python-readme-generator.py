<!--
https://pypi.org/project/readme-generator/
https://pypi.org/project/python-readme-generator/
-->

[![](https://img.shields.io/pypi/pyversions/python-readme-generator.svg?longCache=True)](https://pypi.org/project/python-readme-generator/)
[![](https://img.shields.io/pypi/v/python-readme-generator.svg?maxAge=3600)](https://pypi.org/project/python-readme-generator/)
[![Travis](https://api.travis-ci.org/looking-for-a-job/python-readme-generator.py.svg?branch=master)](https://travis-ci.org/looking-for-a-job/python-readme-generator.py/)

#### Installation
```bash
$ [sudo] pip install python-readme-generator
```

#### Features
+   based on [readme-generator](https://pypi.org/project/readme-generator/)
    +   **`<section-name>.md`**, **attrs/methods/props as sections**
    +   **auto headers**
+   python sections: `install`, `classes`, `functions`. `setup.cfg` required by default

#### Classes
class|`__doc__`
-|-
`python_readme_generator.Readme` |methods: `getmodules()`, `getclasses()`, `getfunctions()`. methods as sections: `install()`, `classes()`, `functions()`

#### What's Next?
create custom README class

```python
import python_readme_generator

class Readme(python_readme_generator.Readme):
    headers = {"badges":""}
    locations = python_readme_generator.Readme.locations + [".config/README"]
    order = ['badges','install', 'features', 'classes', 'functions', 'next',...]

    def badges(self):
        ...

Readme().save("README.md")
```

#### Related projects
+   [`readme-generator`](https://pypi.org/project/readme-generator/)
+   [`python-readme-generator`](https://pypi.org/project/python-readme-generator/)
+   [`django-readme-generator`](https://pypi.org/project/django-readme-generator/)

<p align="center">
    <a href="https://pypi.org/project/python-readme-generator/">python-readme-generator</a>
</p>
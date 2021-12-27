# PyPI Template

Python Library Template



## Step

1. Clone this repo

```shell
git clone https://github.com/louisyoungx/pypi-template.git
```

2. Change project name

```shell
mv pypi-template myPic
cd myPic
```

3. Reset `.git`

```shell
rm -rf .git
git init
```

4. Set Github Actions

```shell
mv github .github
```

5. Modify `setup.cfg`

> You need change `[[PROJECT-NAME]]` and `[[DESCRIPTION]]`
>
> Of course, value of `version`, `author`, `email` also need change.

```cfg
[metadata]
name = [[PROJECT-NAME]]
version = 0.0.1
author = louisyoungx
author_email = 1462648167@qq.com
description = [[DESCRIPTION]]
long_description = file: README.md
long_description_content_type = text/markdown
url = https://github.com/louisyoungx/[[PROJECT-NAME]]
project_urls =
    Bug Tracker = https://github.com/louisyoungx/[[PROJECT-NAME]]/issues
classifiers =
    Programming Language :: Python :: 3
    License :: OSI Approved :: MIT License
    Operating System :: OS Independent

[options]
package_dir =
    = src
packages = find:
python_requires = >=3.6

[options.packages.find]
where = src
```

6. Modify `README.md`

```shell
vim README.md
```

7. Append python package to `src`
8. Add test file to `test`
9. Run build and upload to PyPI

```shell
python3 -m build
python3 -m twine upload dist/*
```




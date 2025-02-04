# DeepDiff v 8.1.1

![Downloads](https://img.shields.io/pypi/dm/deepdiff.svg?style=flat)
![Python Versions](https://img.shields.io/pypi/pyversions/deepdiff.svg?style=flat)
![License](https://img.shields.io/pypi/l/deepdiff.svg?version=latest)
[![Build Status](https://github.com/seperman/deepdiff/workflows/Unit%20Tests/badge.svg)](https://github.com/seperman/deepdiff/actions)
[![codecov](https://codecov.io/gh/seperman/deepdiff/branch/master/graph/badge.svg?token=KkHZ3siA3m)](https://codecov.io/gh/seperman/deepdiff)

## Modules

- [DeepDiff](https://zepworks.com/deepdiff/current/diff.html): Deep Difference of dictionaries, iterables, strings, and ANY other object.
- [DeepSearch](https://zepworks.com/deepdiff/current/dsearch.html): Search for objects within other objects.
- [DeepHash](https://zepworks.com/deepdiff/current/deephash.html): Hash any object based on their content.
- [Delta](https://zepworks.com/deepdiff/current/delta.html): Store the difference of objects and apply them to other objects.
- [Extract](https://zepworks.com/deepdiff/current/extract.html): Extract an item from a nested Python object using its path.
- [commandline](https://zepworks.com/deepdiff/current/commandline.html): Use DeepDiff from commandline.

Tested on Python 3.8+ and PyPy3.

- **[Documentation](https://zepworks.com/deepdiff/8.1.1/)**

## What is new?

Please check the [ChangeLog](CHANGELOG.md) file for the detailed information.

DeepDiff 8-2-0

- Small optimizations so we don't load functions that are not needed
- Updated the minimum version of Orderly-set 
- Normalize all datetimes into UTC. Assume timezone naive datetimes are UTC. 

DeepDiff 8-1-0

- Removing deprecated lines from setup.py
- Added `prefix` option to `pretty()`
- Fixes hashing of numpy boolean values.
- Fixes __slots__ comparison when the attribute doesn't exist.
- Relaxing orderly-set reqs
- Added Python 3.13 support
- Only lower if clean_key is instance of str #504
- Fixes issue where the key deep_distance is not returned when both compared items are equal #510
- Fixes exclude_paths fails to work in certain cases
- exclude_paths fails to work #509
- Fixes to_json() method chokes on standard json.dumps() kwargs such as sort_keys
- to_dict() method chokes on standard json.dumps() kwargs  #490
- Fixes accessing the affected_root_keys property on the diff object returned by DeepDiff fails when one of the dicts is empty
- Fixes accessing the affected_root_keys property on the diff object returned by DeepDiff fails when one of the dicts is empty #508


## Installation

### Install from PyPi:

`pip install deepdiff`

If you want to use DeepDiff from commandline:

`pip install "deepdiff[cli]"`

If you want to improve the performance of DeepDiff with certain functionalities such as improved json serialization:

`pip install "deepdiff[optimize]"`

Install optional packages:
- [yaml](https://pypi.org/project/PyYAML/)
- [tomli](https://pypi.org/project/tomli/) (python 3.10 and older) and [tomli-w](https://pypi.org/project/tomli-w/) for writing
- [clevercsv](https://pypi.org/project/clevercsv/) for more rubust CSV parsing
- [orjson](https://pypi.org/project/orjson/) for speed and memory optimized parsing
- [pydantic](https://pypi.org/project/pydantic/)


# Documentation

<https://zepworks.com/deepdiff/current/>

### A message from Sep, the creator of DeepDiff

> 👋 Hi there,
>
> Thank you for using DeepDiff!
> As an engineer, I understand the frustration of wrestling with **unruly data** in pipelines.
> That's why I developed a new tool - [Qluster](https://qluster.ai/solution) to empower non-engineers to control and resolve data issues at scale autonomously and **stop bugging the engineers**! 🛠️
>
> If you are going through this pain now, I would love to give you [early access](https://www.qluster.ai/try-qluster) to Qluster and get your feedback.


# ChangeLog

Please take a look at the [CHANGELOG](CHANGELOG.md) file.

# Survey

:mega: **Please fill out our [fast 5-question survey](https://forms.gle/E6qXexcgjoKnSzjB8)** so that we can learn how & why you use DeepDiff, and what improvements we should make. Thank you! :dancers:

# Contribute

1. Please make your PR against the dev branch
2. Please make sure that your PR has tests. Since DeepDiff is used in many sensitive data driven projects, we strive to maintain around 100% test coverage on the code.

Please run `pytest --cov=deepdiff --runslow` to see the coverage report. Note that the `--runslow` flag will run some slow tests too. In most cases you only want to run the fast tests which so you wont add the `--runslow` flag.

Or to see a more user friendly version, please run: `pytest --cov=deepdiff --cov-report term-missing --runslow`.

Thank you!

# Authors

Please take a look at the [AUTHORS](AUTHORS.md) file.

Overview
========

DAG is a Fortran 2018 library for creating and manipulating directed acyclic graphs (DAGs).
It includes a topological sort feature, and it generates files in the [GraphViz] "dot" format.

Prerequisites
-------------
The recommended versions below are the versions used in developing dag.  Earlier versions
might work also.

1. A Fortran 2018 compiler (Recommended: [gfortran] 10 or later).
2. [OpenCoarrays]  (Recommended: 2.9.0 or later)
3. [fpm]  (downstream of commit [a07bf3])

Building and testing
--------------------
To clone, build, and test, execute the following in a `bash` shell:
```
git clone git@github.com:sourceryinstitute/dag
fpm build --compiler caf
fpm test --compiler caf --runner cafrun
```
Users who prefer a [FoBiS] build system, please see [daglib by Jacob Williams], from which
the current repository was forked.

Example
-------

The [jacob-example] test provides a short example of the use of dag, including checks

for the expected results.  That test also writes the following image to a `.png` file:

<img src="https://raw.githubusercontent.com/sourceryinstitute/dag/master/media/dag_example.png" width="500">

License
-------

This library is released under a [BSD-3 license].

[daglib by Jacob Williams]: https://github.com/jacobwilliams/daglib
[FoBiS]: https://github.com/szaghi/FoBiS
[GraphViz]: https://www.graphviz.org
[jacob-example]: https://github.com/sourceryinstitute/dag/blob/master/tests/integration/jacob-example/test-jacob-example.f90
[OpenCoarrays]: https://github.com/sourceryinstitute/opencoarrays
[CMake]: https://www.cmake.org
[gfortran]: https://gcc.gnu.org
[BSD-3 license]: https://github.com/sourceryinstitute/dag/blob/master/LICENSE
[fpm]: https://github.com/everythingfunctional/fpm
[a07bf3]: https://github.com/everythingfunctional/fpm/commit/a07bf3fb3fc07a2c3bf13f8c36a158108a38cefa

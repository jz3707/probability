# How to Contribute

We'd love to have your patches and contributions! Here are some guidelines.

## Contributor License Agreement

Contributions to this project must be accompanied by a Contributor License
Agreement. You (or your employer) retain the copyright to your contribution;
this simply gives us permission to use and redistribute your contributions as
part of the project. Head over to <https://cla.developers.google.com/> to see
your current agreements on file or to sign a new one.

You generally only need to submit a CLA once, so if you've already submitted one
(even if it was for a different project), you probably don't need to do it
again.

## Code reviews

All submissions, including submissions by project members, require review. We
use GitHub pull requests for this purpose. Consult [GitHub
Help](https://help.github.com/articles/about-pull-requests/) for more
information on using pull requests.

## Unit tests

Please include unit tests when contributing new features, as they help to a)
prove that your code works correctly, and b) guard against future breaking
changes to lower the maintenance cost. It's also helpful to check that any
changes you propose do not break existing unit tests. You can run tests (on CPU)
using the command,

```shell
bazel test --config=opt --copt=-O3 --copt=-march=native \
  //tensorflow_probability/...
```

or on GPU,

```shell
bazel test --config=opt --copt=-O3 --copt=-march=native --config=cuda \
  //tensorflow_probability/...
```

from the root of the `tensorflow_probability` repository.

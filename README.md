# python-stub

A project stub template for python projects with CI integration and pre-commit hooks.

## Initializing a New Repository

This step is unnecessary if creating from a template.

First, create a bare new repository and get the git URL. (e.g. `git@github.com:nnamon/testnew.git`)

Next, clone [python-stub](https://github.com/nnamon/python-stub) repository to your local file
system.

```shell
$ git clone git@github.com:nnamon/python-stub.git
Cloning into 'python-stub'...
remote: Enumerating objects: 20, done.
remote: Counting objects: 100% (20/20), done.
remote: Compressing objects: 100% (15/15), done.
remote: Total 20 (delta 0), reused 17 (delta 0), pack-reused 0
Receiving objects: 100% (20/20), done.
$ cd python-stub
```

Then, add your remote repository and push to it.

```shell

$ git remote rm origin
$ git remote add origin git@github.com:nnamon/testnew.git
$ git push origin master
Counting objects: 20, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (15/15), done.
Writing objects: 100% (20/20), 3.75 KiB | 3.75 MiB/s, done.
Total 20 (delta 0), reused 20 (delta 0)
remote:
remote: Create a pull request for 'master' on GitHub by visiting:
remote:      https://github.com/nnamon/testnew/pull/new/master
remote:
To github.com:nnamon/testnew.git
 * [new branch]      master -> master
```

Finally, remove the `python-stub` repository and clone your new one.

```shell
$ rm -rf python-stub
$ git clone git@github.com:nnamon/testnew.git
```

## Usage

To setup the pre-commit hooks, run `make develop` after cloning the repository.

Next, rename the `python_stub` directory to your module name. Make sure that it conforms to module
naming requirements (i.e. no dashes).

Then, replace all the references to `python-stub` in the following files:

1. `setup.py`
2. `tox.ini`
3. `tests/test_sanity.py`

## Writing and Running Tests

To run the tests, run the command `make test`.

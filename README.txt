# Rustpkg source

This is the last version of `rustpkg` (and its documentation) before
it was removed from the mozilla/rust repo.

At the time of writing, it's already bitrotted; and I (huonw) will not
be updating it. Anyone interested should contact me, I'm very happy to
add people to this organisation (and, preferably, transfer ownership
too).

-----

Right now, commands that work are "build" and "clean".

`rustpkg build` and `rustpkg clean` should work

for example:
$ cd ~/rust/src/librustpkg/testsuite/pass
$ rustpkg build hello-world
... some output ...
$ rustpkg clean hello-world

-------------
the following test packages in librustpkg/testsuite/pass:
      * hello-world
      * install-paths
      * simple-lib
      * deeply/nested/path
      * fancy-lib

   It fails on the following test packages:
      * external-crate (no support for `extern mod` inference yet)

and should fail with proper error messages
on all of the test packages in librustpkg/testsuite/fail
      * no-inferred-crates

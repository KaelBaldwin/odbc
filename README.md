odbc driver written in go. Implements database driver interface as used by standard database/sql package. It calls into odbc dll on Windows, and uses cgo (unixODBC) everywhere else.

----

See https://github.com/alexbrainman/odbc/issues/88

In order to use this driver with the iseries iaccess driver, I needed to use the changes alexbrainman implemented in his for_issue_88 branch, but rather than use the unmaintained branch, I wanted to be able to merge in any changes that are made after that branch was created.

So I forked the repo from that commit in the latest from master (there were a few conflicts, which I guessed at resolving, it seems to have worked.) and then just changed any imports from using alexbrainman's repo to using this one. 


# symlinkown
Patch for the Linux Kernel to implement "SymlinksIfOwnerMatches" features

description
-----------

This is a patch that implements a symlink protection feature in the Linux kernel.
For a configurable group all file accesses with symlinks will only be approved if
the owner of the symlink target matches the owner of the symlink.

This prevents attacks with web servers on multiuser systems. This attack was
used in the hack of Freedom Hosting II.

Background:
* https://blog.hboeck.de/archives/873-The-tricky-security-issue-with-FollowSymLinks-and-Apache.html
* https://securityaffairs.co/wordpress/55990/deep-web/freedom-hosting-ii-hack.html

versions
--------

The current patch has been created for kernel 4.14.12. At the time of this writing it can
be applied to both the latest stable (4.17.4) and longterm (4.14.53) kernel.

If you get rejects when applying this patch to the latest kernel please open an issue and
I'll try to update it.

source and copyright
--------------------

This patch is extracted from the grsecurity kernel patch. It is licensed (like the
Linux kernel itself) under the GPL version 2.

Copyright 2014-2017 by Open Source Security, Inc.,
Brad Spengler <spender@grsecurity.net>
and PaX Team <pageexec@freemail.hu>

The only thing I did is extract the patch out of the larger grsecurity patchset.

Hanno Böck, https://hboeck.de/

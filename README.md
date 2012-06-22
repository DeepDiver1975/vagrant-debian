About
-----

This script will: 

 1. download the Debian Squeeze, 32bit iso netinst
 2. ... do some magic to turn it into a vagrant box file
 3. output package.box 

Usage
-----

 > ./build.sh

 This should do everything you need. If you don't have 
 mkisofs, install macports, then: sudo port install cdrtools

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

William's notes
---------------

Forked off https://github.com/joneskoo/vagrant-debian-squeeze-32

Made it:

- 64-bit
- Bumped to 6.0.5
- Depend on bsdtar. GNU tar can not extract ISO.
- Run with Debian's VirtualBox toolset
- General clean-up
- Added Makefile

Joonas' notes
-------------

Forked off https://github.com/cal/vagrant-ubuntu-precise-64

Made it:

- build a 32 bit Debian stable instead of Ubuntu.
- zero the image before exporting a package (requires a lot of disk space)

Ben's notes
-----------

Forked Carl's repo, and it sort of worked out of the box. Tweaked 
office 12.04 release: 

 - Downloading 12.04 final release. (Today as of this writing)
 - Checking MD5 to make sure it is the right version
 - Added a few more checks for external dependencies, mkisofs
 - Removed wget, and used curl to reduce dependencies
 - Added more output to see what is going on
 - Still designed to work on Mac OS X :)
    ... though it should work for Linux systems too (maybe w/ a bit of porting)

Carl's original README
----------------------

Decided I wanted to learn how to make a vagrant base box.

Let's target Precise Pangolin since it should be releasing soon, I said.

Let's automate everything, I said.

Let's do it all on my macbook, I said.

Woo.

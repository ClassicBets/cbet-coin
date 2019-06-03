ClassicBets Core version *1.0.0* is now available from:  <https://github.com/ClassicBets/cbet-coin/releases>

This is a new minor version release, including various bug fixes and performance improvements, as well as updated translations.

Please report bugs using the issue tracker at github: <https://github.com/ClassicBets/cbet-coin/issues>

Non-Mandatory Update
==============

ClassicBets Core v1.0.0 is a non-mandatory update to address bugs and introduce minor enhancements that do not require a network change.

How to Upgrade
==============

If you are running an older version, shut it down. Wait until it has completely shut down (which might take a few minutes for older versions), then run the installer (on Windows) or just copy over /Applications/ClassicBets-Qt (on Mac) or classicbetsd/classicbets-qt (on Linux).


Compatibility
==============

ClassicBets Core is extensively tested on multiple operating systems using
the Linux kernel, macOS 10.8+, and Windows Vista and later.

Microsoft ended support for Windows XP on [April 8th, 2014](https://www.microsoft.com/en-us/WindowsForBusiness/end-of-xp-support),
No attempt is made to prevent installing or running the software on Windows XP, you
can still do so at your own risk but be aware that there are known instabilities and issues.
Please do not report issues about Windows XP to the issue tracker.

ClassicBets Core should also work on most other Unix-like systems but is not
frequently tested on them.

### :exclamation::exclamation::exclamation: MacOS 10.13 High Sierra :exclamation::exclamation::exclamation:

**Currently there are issues with the 1.0.0+ gitian release on MacOS version 10.13 (High Sierra), no reports of issues on older versions of MacOS.**

Notable Changes
==============

zCBET Updates
--------------

### Fix spending for v1 zCBET created before block 1050020

The transition to v2 zCBET and reset of the accumulators caused blocks 1050000 - 1050010 to be accumulated twice. This was causing a number v1 zCBET to not create valid witnesses, and thus were not spendable. This problem is fixed by double accumulating blocks 1050000-1050010 when creating the witness. Any user that had issues spending zCBET v1 will now be able to convert that into CBET and then zCBET v2 (if desired).

### Adjustment to staking properties to reduce orphaned blocks

zCBET stake set to update more frequently and lowering the stake hashdrift to 30 seconds to reduce the number of orphans being experienced by ClassicBets stakers.

Further work is being done to improve the efficiently of zPoS beyond this, and will be available in a subsequent release at a later date.



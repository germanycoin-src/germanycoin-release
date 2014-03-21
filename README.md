Germanycoin integration/staging tree
================================

http://www.germanycoin.net

Copyright (c) 2009-2013 Bitcoin Developers
Copyright (c) 2011-2013 Litecoin Developers
Copyright (c) 2014 Germanycoin Developers

What is Germanycoin?
----------------

Germanycoin is a lite version of Bitcoin using scrypt as a proof-of-work algorithm.
 - 1 minute block targets
 - Block reward decreasing 1 coin every 40 days 
 - 42 million total coins, 50% of which are premined to give away to Germans
 - 25 coins per block
 - Retarget every block (Kimoto's gravity well)

For more information, as well as an immediately useable, binary version of
the Germanycoin client sofware, see http://www.germanycoin.net.

License
-------

Germanycoin is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.

Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the Germanycoin
development team members simply pulls it.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/bitcoin/bitcoin/tags) are created
regularly to indicate new official, stable release versions of Germanycoin.

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test. Please be patient and help out, and
remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write unit tests for new code, and to
submit new unit tests for old code.

Unit tests for the core code are in `src/test/`. To compile and run them:

    cd src; make -f makefile.unix test

Unit tests for the GUI code are in `src/qt/test/`. To compile and run them:

    qmake BITCOIN_QT_TEST=1 -o Makefile.test bitcoin-qt.pro
    make -f Makefile.test
    ./germanycoin-qt_test

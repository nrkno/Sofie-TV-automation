# Installation

Note that although this gives you a full installation of all core components, you cannot do any actual playout yet. Please see the [FAQ](faq.md#is-there-any-missing-in-the-public-repositories).

1. Install [Meteor](https://www.meteor.com/).
2. Install [Node.js](https://nodejs.org/), version 8 \(LTS\).
3. Install **yarn** \(package manager, similar to **npm**\) by running `npm install --global yarn`
4. Clone the [tv-automation-server-core](https://github.com/nrkno/tv-automation-server-core) repository.
5. `cd` into the `tv-automation-server-core/meteor` directory.
6. Run `meteor npm install` in the `tv-automation-server-core`

    directory.

7. Run `meteor`
8. `cd ..` out of the `tv-automation-server-core` directory.
9. Clone the [tv-automation-playout-gateway](https://github.com/nrkno/tv-automation-playout-gateway) repository.
10. `cd` into the `tv-automation-playout-gateway` directory.
11. Run `yarn` in the `tv-automation-playout-gateway` directory.
12. Run `yarn buildstart` in the `tv-automation-playout-gateway` directory.
13. `cd ..` out of the`tv-automation-playout-gateway` directory.
14. Clone tv-automation-mos-gateway
15. cd into `tv-automation-mos-gateway`
16. run `yarn` in mos gateway directory
17. run `yarn buildstart` in mos gateway directory


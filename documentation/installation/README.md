# Installation

{% hint style="info" %}
Please note that this documentation is being actively developed during Q2 2019, and that the content and links are likely to undergo drastic changes from day to day. 
{% endhint %}

Note that although this gives you a full installation of all core components, you cannot do any actual playout yet. Please see the [FAQ](../faq.md#is-there-any-missing-in-the-public-repositories).

1. Install [Meteor](https://www.meteor.com/).
2. Install [Node.js](https://nodejs.org/), version 8 \(LTS\).
3. If on windows, install the build tools by running `npm install --global --production windows-build-tools`
4. Install **yarn** \(package manager, similar to **npm**\) by running `npm install --global yarn`
5. Clone the [tv-automation-server-core](https://github.com/nrkno/tv-automation-server-core) repository.
6. `cd` into the `tv-automation-server-core/meteor` directory.
7. Run `meteor npm install` in the `tv-automation-server-core`

    directory.

8. Run `meteor`
9. `cd ..` out of the `tv-automation-server-core` directory.
10. Clone the [tv-automation-playout-gateway](https://github.com/nrkno/tv-automation-playout-gateway) repository.
11. `cd` into the `tv-automation-playout-gateway` directory.
12. Run `yarn` in the `tv-automation-playout-gateway` directory.
13. Run `yarn buildstart` in the `tv-automation-playout-gateway` directory.
14. `cd ..` out of the`tv-automation-playout-gateway` directory.
15. Clone the [tv-automation-mos-gateway](https://github.com/nrkno/tv-automation-mos-gateway) repository.
16. `cd` into the `tv-automation-mos-gateway` directory.
17. Run `yarn` in the `tv-automation-mos-gateway` directory.
18. Run `yarn buildstart`


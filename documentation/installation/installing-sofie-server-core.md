# Quick install

## Installing for testing \(or production\)

### **Prerequisites**

**\(Linux\)** Install [Docker](https://docs.docker.com/install/linux/docker-ce/ubuntu/) and [docker-compose](https://www.digitalocean.com/community/tutorials/how-to-install-docker-compose-on-ubuntu-18-04).  
**\(Windows\)** Install [Docker for Windows](https://hub.docker.com/editions/community/docker-ce-desktop-windows) \(you will need to be running either _Windows 10 Pro_ or _Windows 10 Enterprise_ version\)

### Installation

This docker-compose file automates the basic setup of the [Sofie-Core application](../under-the-hood/libraries.md#main-application), the backend database and different Gateway options.

{% file src="../../.gitbook/assets/docker-compose \(2\).yaml" %}

After you've downloaded the file, open it in a text editor and navigate to the _ingest-gateway_ section, and select which type of _ingest-gateway_ you'd like installed by commenting out the others.

Create a `Sofie` folder and copy the docker-compose-file into it.

Then open a terminal, `cd your-sofie-folder` and `sudo docker-compose up` \(just `docker-compose up` on windows\).

Once the installation is done, Sofie should be running on [http://localhost:3000](http://localhost:3000)

Next, you will need to install a Rundown Gateway. Visit [Rundowns & Newsroom Systems](installing-a-gateway/rundown-or-newsroom-system-connection/) to see which _Rundown Gateway_ is best suited for ~~_your_~~ production environment. 

### Tips for running in production

There are some things not covered in this guide needed to run Sofie in a production environment:

* Logging: Collect, store and track error messages. [Kibana ](https://www.elastic.co/kibana)and [logstash](https://www.elastic.co/logstash) is one way to do it.
* NGINX: It is customary to put a load-balancer in front of Sofie-Core.
* Memory and CPU usage monitoring.

## Installing for Development

Installation instructions for installing Sofie-Core or the various gateways are available in the README-file in their respective github-repos. 

Common prerequisites are [Node.js](https://nodejs.org/) and [Yarn](https://yarnpkg.com/).  
Links to the repos are listed at [Applications & Libraries](../under-the-hood/libraries.md).

[Sofie Core GitHub Page for Developers](https://github.com/nrkno/tv-automation-server-core)


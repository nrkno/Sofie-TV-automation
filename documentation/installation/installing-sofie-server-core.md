# Installing Sofie Server Core

## Linux, using Docker

_Prerequisites: Install_ [_docker_](https://docs.docker.com/install/linux/docker-ce/ubuntu/) _and_ [_docker-compose_](https://www.digitalocean.com/community/tutorials/how-to-install-docker-compose-on-ubuntu-18-04)\_\_

First create a new directory for Sofie and copy _docker-compose.yaml_ \(link below\) into it.

```bash
mkdir Sofie
cd Sofie
```

{% file src="../../.gitbook/assets/docker-compose.yaml" %}

Then run `sudo docker-compose up`to install Sofie Core.

Now open up your browser and go to [http://127.0.0.1:3000](http://127.0.0.1:3000)   
You should be presented with the Sofie GUI. Head over to [Getting started](../getting-started.md) for more instructions

## Windows, using Docker

{% hint style="info" %}
Please note: Docker requires Windows 10 Pro/Enterprise
{% endhint %}

_Prerequisites: Install_ [_Docker_](https://hub.docker.com/editions/community/docker-ce-desktop-windows)_._

Create a new a folder for Sofie and copy _docker-compose.yaml_ \(link below\) into it.

{% file src="../../.gitbook/assets/docker-compose.yaml" %}

Open PowerShell and navigate to the folder you created earlier.  
Then run `docker-compose up` to install Server Core.

Now open up your browser and go to [http://127.0.0.1:3000](http://127.0.0.1:3000)   
You should be presented with the Sofie GUI. Head over to [Getting started](../getting-started.md) for more instructions

## Manual installation \(for developers\)

1. Install [Meteor](https://www.meteor.com/)
2. Install [Node.js](https://nodejs.org/), version 8 \(LTS\)
3. If on windows, install the build tools by running `npm install --global --production windows-build-tools`
4. Install **yarn** \(package manager, similar to **npm**\) by running `npm install --global yarn`
5. Clone the [tv-automation-server-core](https://github.com/nrkno/tv-automation-server-core) repository
6. `cd` into the `tv-automation-server-core/meteor` directory
7. Run `meteor npm install` in the `tv-automation-server-core`

   directory.

8. Run `meteor`
9. `cd ..` out of the `tv-automation-server-core` directory

The web interface is available at [http://127.0.0.1:3000](http://127.0.0.1:3000), if you need to access the database \(MongoDB\) directly \(we recommend [Robomongo](https://robomongo.org/)\), it'll be accessible at the meteor port +1, i.e. `3001`.  


After Server Core is installed, check out the Getting started guide on how set it up!

{% page-ref page="../getting-started.md" %}






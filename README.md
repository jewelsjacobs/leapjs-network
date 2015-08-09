# LeapJS Static Network Server

## Install

```
> git clone git@github.com:jewelsjacobs/leapjs-network.git -b static-server --single-branch
> npm install
```

## Server info

It runs as a [forever-service](https://github.com/zapty/forever-service) with [nodemon](https://github.com/remy/nodemon) called `raml`.

Here's the command to install the service:

```bash
npm install forever -g
npm install forever-service -g
npm install nodemon -g
cd /var/apps/leapjs-network
forever-service install leapjs-network --script server.js -f " -c nodemon" -o " --delay 10 --watch public --exitcrash" -e "PATH=/usr/local/bin:$PATH"
```

Commands to interact with service `leapjs-network`:

```
Start   - "sudo start leapjs-network"
Stop    - "sudo stop leapjs-network"
Status  - "sudo status leapjs-network"
Restart - "sudo restart leapjs-network"
```
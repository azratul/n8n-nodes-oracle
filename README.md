# n8n-nodes-oracle

<p align="center">
	<a href="https://n8n.io/"><img src="https://raw.githubusercontent.com/n8n-io/n8n/master/assets/n8n-logo.png" height="50" style="margin:10px"/></a>
	<a href="https://www.oracle.com/database/"><svg class="u30-oicn-mobile" xmlns="http://www.w3.org/2000/svg" width="100" height="50" viewBox="0 0 32 21"><path fill="#C74634" d="M9.9,20.1c-5.5,0-9.9-4.4-9.9-9.9c0-5.5,4.4-9.9,9.9-9.9h11.6c5.5,0,9.9,4.4,9.9,9.9c0,5.5-4.4,9.9-9.9,9.9H9.9 M21.2,16.6c3.6,0,6.4-2.9,6.4-6.4c0-3.6-2.9-6.4-6.4-6.4h-11c-3.6,0-6.4,2.9-6.4,6.4s2.9,6.4,6.4,6.4H21.2"></path></svg></a>
</p>

<p align="center">
  This package provides nodes for n8n to work with oracle<br />
  by <a href="https://github.com/jdu74">Jean Durieux</a>
</p>

This package provides nodes for [`n8n`](https://github.com/n8n-io/n8n) to work with [oracle](https://cad.oracle.com).

## Installation

### In a local NPM installation

```bash
npm i azratul/n8n-nodes-oracle
```

The nodes should be automatically discovered by `n8n`.

### In a global installation

```bash
npm i -g azratul/n8n-nodes-oracle
```

You should then set the `N8N_CUSTOM_EXTENSIONS` variable to the path of the modules, e.g. on Ubuntu:

```bash
export N8N_CUSTOM_EXTENSIONS="/usr/local/lib/node_modules/n8n-nodes-oracle"
```

### In a Docker image

You'll have to spin your own `Dockerfile` that builds from the official `n8n` image:

```Dockerfile
FROM n8nio/n8n

USER root

RUN npm_config_user=root npm install -g azratul/n8n-nodes-oracle

ENV N8N_CUSTOM_EXTENSIONS "/usr/local/lib/node_modules/n8n-nodes-oracle"

```

## Usage

### Credentials

The credentials are based on the standard oracle credentials. The easiest way is to [Using API Keys with oracle](https://oracle-public.github.io/docs/apikeys/) with the required permissions to work with oracle API.

### oracle Webhook Notifications

This node will listen to message on a topic's subscription and trigger whenever a new message is coming.

#### Parameters

* ClientId or DocumentId


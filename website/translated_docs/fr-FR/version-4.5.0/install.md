---
id: version-4.5.0-installation
title: Installation
original_id: installation
---

Verdaccio is a multiplatform web application. To install it, you need a few basic prerequisites.

#### Conditions préalables

1. Node higher Node `8.x` (LTS "Carbon") is the minimum supported version.
2. npm `>=5.x` or, `pnpm` or `yarn`

  > We highly recommend to use the latest Node Package Managers clients `> npm@6.x | yarn@1.x | pnpm@4.x`
3. The web interface supports the `Chrome, Firefox, Edge, and IE11` browsers.

> Verdaccio will support latest Node.js version according the [Node.js Release Working Group](https://github.com/nodejs/Release) recomendations.

<div id="codefund">''</div>

## En cours d'installation du CLI

`verdaccio` doit être installé globalement en utilisant l'une des méthodes suivantes:

En utilisant `npm`

```bash
npm install -g verdaccio
```
ou en utilisant `yarn`

```bash
yarn global add verdaccio
```

![installer verdaccio](assets/install_verdaccio.gif)


## Usage basique

Une fois installé, il vous suffit d’exécuter la commande CLI:

```bash
$> verdaccio
warn --- config file  - /home/.config/verdaccio/config.yaml
warn --- http address - http://localhost:4873/ - verdaccio/4.4.4
```

Pour plus d'information sur CLI, veuillez [lire la section cli](cli.md).

You can set the registry by using the following command.

```bash
npm set registry http://localhost:4873/
```

you can pass a `--registry` flag when needed.

```bash
npm install --registry http://localhost:4873
```

define in your `.npmrc` a `registry` field.

```bash
//.npmrc
registry=http://localhost:4873
```

Or a `publishConfig` in your `package.json`

```json
{
  "publishConfig": {
    "registry": "http://localhost:4873"
  }
}
```

## Create Your Own Private NPM Package Tutorial

If you still need a deep explanation, don't miss the at [thedevlife](https://mybiolink.co/thedevlife) tutorial how to publish your own private package using Verdaccio.  <iframe width="560" height="315" src="https://www.youtube.com/embed/Co0RwdpEsag" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen mark="crwd-mark"></iframe>

## Image de docker

```bash
docker run -it --rm --name verdaccio -p 4873:4873 verdaccio/verdaccio
```

`verdaccio` a une image de docker officielle que vous pouvez utiliser, et dans la majorité des cas, la configuration par défaut est assez bonne. Pour plus d’informations sur la façon d’installer l’image officielle, [lisez la section docker](docker.md).

## Cloudron

`verdaccio` est également disponible en application à installer en 1 clic sur [Cloudron](https://cloudron.io)

[![Installer](https://cloudron.io/img/button.svg)](https://cloudron.io/button.html?app=org.eggertsson.verdaccio)


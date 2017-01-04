# bibliomap

Bibliomap is a tool for real-time viewing in the browser localised usage events generated by [ezPAARSE](https://github.com/ezpaarse-project/ezpaarse).

How could it be useful ?
  * For real-time monitoring your ezproxy EC consultations 
  * For helping ezpaarse adoption in your institution.
  * And just for fun !

![anim](https://cloud.githubusercontent.com/assets/328244/19802257/11855392-9d03-11e6-9338-e35893ecddfc.gif)

[Demonstration on the CNRS subscribed electronic ressources usage statistics](http://bibliomap.inist.fr/)

## Technical architecture

Bibliomap uses these softwares:
  * [bibliomap-harvester](https://github.com/ezpaarse-project/bibliomap-harvester) for real-time listening lines of log comming from ezproxys
  * [bibliomap-enricher](https://github.com/ezpaarse-project/bibliomap-enricher) listening for bibliomap-harvester data, sending it to ezpaarse and sending the result to you this bibliomap
  * [bibliomap-viewer](https://github.com/ezpaarse-project/bibliomap-viewer) for the front end web interface showing ezPAARSE EC's in real time thanks to websocket protocol
  * [Log.io](http://logio.org/) protocol for all the communication between these scripts

<p align="center">
<img src="https://docs.google.com/drawings/d/1bkxEEBL1kLzH76dkIYFzspYHOVajDjQHCijU3mxJLnM/pub?w=694&h=519" />
</p>

## Prerequisites

  * Docker and docker-compose

## Installation and running a quick demo

```
git clone git@github.com:ezpaarse-project/bibliomap.git
cd bibliomap
npm start
```

Then browse to http://127.0.0.1:50197

### Expo mode
In expo mode, the description popup will automatically show and hide at determined intervals. To activate it, add `expo` or `e` in the query. By default, the popup will be shown for **1 minute**, then hidden for **10 minutes**. To define custom intervals, `expo` should take two numbers separated by a comma. The first one is the time shown, the second is the time hidden. Times are defined in **seconds**.

## Developers

## Installation for developing

```
git clone git@github.com:ezpaarse-project/bibliomap.git
cd bibliomap
git clone git@github.com:ezpaarse-project/bibliomap-harvester.git
git clone git@github.com:ezpaarse-project/bibliomap-enricher.git
git clone git@github.com:ezpaarse-project/bibliomap-viewer.git
npm run install
npm run start-debug
```

Then browse to http://127.0.0.1:50197


### Upgrade

To upgrade to the latest version of [bibliomap-harvester](https://github.com/ezpaarse-project/bibliomap-harvester), [bibliomap-enricher](https://github.com/ezpaarse-project/bibliomap-enricher), and [bibliomap-viewer](https://github.com/ezpaarse-project/bibliomap-viewer) in the docker-compose.yml, just git clone all of these into your bibliomap/ folder (see just above) and run this command:

```
npm version patch
```

### Running with the latest tags

To start the bibliomap demo with the latest tags (you must prealably do "make build" for each [bibliomap-harvester](https://github.com/ezpaarse-project/bibliomap-harvester), [bibliomap-enricher](https://github.com/ezpaarse-project/bibliomap-enricher), [bibliomap-viewer](https://github.com/ezpaarse-project/bibliomap-viewer), and [ezPAARSE](https://github.com/ezpaarse-project/ezpaarse) modules), just type :
```
npm run start-latest
```

Useful for developement and debugging.

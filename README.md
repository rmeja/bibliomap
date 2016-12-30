# bibliomap

Bibliomap is a tool for real-time viewing in the browser localised usage events generated by [ezPAARSE](https://github.com/ezpaarse-project/ezpaarse).

How could it be useful ?
  * For real-time monitoring your ezproxy EC consultations 
  * For the fun !

![anim](https://cloud.githubusercontent.com/assets/328244/19802257/11855392-9d03-11e6-9338-e35893ecddfc.gif)

[Demonstration on the CNRS subscribed electronic ressources usage statistics](http://bibliomap.inist.fr/)


Bibliomap uses these softwares:
  * [bibliomap-harvester](https://github.com/ezpaarse-project/bibliomap-harvester) for real-time listening lines of log comming from ezproxys
  * [bibliomap-enricher](https://github.com/ezpaarse-project/bibliomap-enricher) listening for bibliomap-harvester data, sending it to ezpaarse and sending the result to you this bibliomap
  * [bibliomap-viewer](https://github.com/ezpaarse-project/bibliomap-viewer) for the front end web interface showing ezPAARSE EC's in real time
  * [Log.io](http://logio.org/) protocol for all the communication between these scripts

<p align="center">
<img src="https://docs.google.com/drawings/d/1bkxEEBL1kLzH76dkIYFzspYHOVajDjQHCijU3mxJLnM/pub?w=694&h=519" />
</p>

## Prerequisites

  * Docker and docker-compose

## Installation and running a quick demo

```
git clone git@github.com:ezpaarse-project/bibliomap.git
npm start
```

Then browse to http://127.0.0.1:50197

## Upgrade

To upgrade to the latest version of [bibliomap-harvester](https://github.com/ezpaarse-project/bibliomap-harvester), [bibliomap-enricher](https://github.com/ezpaarse-project/bibliomap-enricher), and [bibliomap-viewer](https://github.com/ezpaarse-project/bibliomap-viewer) in the docker-compose.yml, just run this command:

```
npm version patch
```
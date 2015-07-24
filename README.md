PyLoad
=========
[![](https://badge.imagelayers.io/writl/pyload:latest.svg)](https://imagelayers.io/?images=writl/pyload:latest 'Get your own badge on imagelayers.io')

Introduction
----
pyLoad is a fast, lightweight and full featured download manager for many One-Click-Hoster, container formats like DLC, video sites or just plain http/ftp links. It aims for low hardware requirements and platform independence to be runnable on all kind of systems (desktop pc, netbook, NAS, router).

Despite its strict restriction it is packed full of features just like webinterface, captcha recognition, unrar and much more.

pyLoad is divided into core and clients, to make it easily remote accessible. Currently there are a webinterface, command line interface, and a GUI written in Qt.

Source [official pyload]

Install
----
Install is easy as all docker images

```sh
docker pull writl/pyload:0.4.9
```

Running
----

```sh
docker run -d -P writl/pyload:0.4.9
```

Configuration
----
You can link your Downloads to your host very easy like that:

```sh
docker run -d -v <host directoy>:/opt/pyload/Downloads -P writl/pyload:0.4.9
```
Notice to replace ```<host directory>``` with your directory path on the host. So if you want to store your Downloads in ```/tmp/Downloads``` then your command would look like this:

```sh
docker run -d -v /tmp/Downloads:/opt/pyload/Downloads -P writl/pyload:0.4.9
```
If you want to have your configuration persistent you have to link the configuration directory outside of the container. This can happen like this:

```sh
docker run -d -v <host directoy>:/opt/pyload/pyload-config -P writl/pyload:0.4.9
```
Finally
----
After the docker has created you can login via the webinterface with:

```sh
USER=pyload
PASSWORD=pyload
```


[official pyload]:http://pyload.org/


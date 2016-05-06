# beat-link

A Java library for synchronizing with beats from Pioneer DJ Link equipment.

[![License](https://img.shields.io/badge/License-Eclipse%20Public%20License%201.0-blue.svg)](#license)

## Installing

Beat-link is available through Maven Central, so to use it in your
Maven project, all you need is to include the appropriate dependency.

[![Maven Central](https://maven-badges.herokuapp.com/maven-central/org.deepsymmetry/beat-link/badge.svg)](https://maven-badges.herokuapp.com/maven-central/org.deepsymmetry/beat-link)

Click the **maven central** badge above to view the repository entry
for beat-link. The proper format for including the latest release as a
dependency in a variety of tools, including Leiningen if you are using
beat-link from Clojure, can be found in the **Dependency Information**
section.

If you want to manually install beat-link, you can download the library
from the [releases](https://github.com/brunchboy/beat-link/releases) page
and put it on your project&rsquo;s class path.

## Usage

See the [API Documentation](http://deepsymmetry.org/beatlink/apidocs/)
for full details, but here is a nutshell guide:

The [`DeviceListener`](http://deepsymmetry.org/beatlink/apidocs/org/deepsymmetry/beatlink/DeviceListener.html)
class allows you to find DJ Link devices on your network. To activate it:

```java
import org.deepsymmetry.beatlink.DeviceListener;

// ...

  DeviceListener.start();
```

After a second, it should have heard from all the devices, and you can
obtain the list of them by calling:

```java
  DeviceListener.currentDevices();
```

This returns a list of [`DeviceAnnouncement`](http://deepsymmetry.org/beatlink/apidocs/org/deepsymmetry/beatlink/DeviceAnnouncement.html)
objects describing the devices that were heard from.

:point_right: To be finished!

## Research

This project is being developed with the help of
[dysentery](https://github.com/brunchboy/dysentery). Check that out
for details of the packets and protocol, and for ways you can help
figure out more.

## License

<img align="right" alt="Deep Symmetry" src="assets/DS-logo-bw-200-padded-left.png">
Copyright © 2016 [Deep Symmetry, LLC](http://deepsymmetry.org)

Distributed under the
[Eclipse Public License 1.0](http://opensource.org/licenses/eclipse-1.0.php).
By using this software in any fashion, you are agreeing to be bound by
the terms of this license. You must not remove this notice, or any
other, from this software.
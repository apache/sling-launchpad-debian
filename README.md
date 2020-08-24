[<img src="https://sling.apache.org/res/logos/sling.png"/>](https://sling.apache.org)

 [![Build Status](https://ci-builds.apache.org/job/Sling/job/modules/job/sling-launchpad-debian/job/master/badge/icon)](https://ci-builds.apache.org/job/Sling/job/modules/job/sling-launchpad-debian/job/master/) [![Test Status](https://img.shields.io/jenkins/tests.svg?jobUrl=https://ci-builds.apache.org/job/Sling/job/modules/job/sling-launchpad-debian/job/master/)](https://ci-builds.apache.org/job/Sling/job/modules/job/sling-launchpad-debian/job/master/test/?width=800&height=600) [![Sonarcloud Status](https://sonarcloud.io/api/project_badges/measure?project=apache_sling-launchpad-debian&metric=alert_status)](https://sonarcloud.io/dashboard?id=apache_sling-launchpad-debian) [![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://www.apache.org/licenses/LICENSE-2.0)

# Apache Sling Launchpad Debian Package Builder

This module is part of the [Apache Sling](https://sling.apache.org) project.

This is a work in progress .deb packaging for Sling.
It provides basic init.d start/stop logrotate & sample sling config. The goal is to provide a generic yet configurable sling package to eliminate the need to build sling for in-house deployments.

To run this, and install using dpkg/apt commands, review /etc/default.sling
config and run
	"service sling start"

Components used are:
* [Sling launchpad](https://github.com/apache/sling/tree/trunk/launchpad/builder)

For the list of supported run modes see the official [launchpad documentation](https://sling.apache.org/documentation/the-sling-engine/the-sling-launchpad.html).

Important locations:

* SLING_EXEC=/opt/sling - Location for all binaries & scripts.
* SLING_DEFAULTS=/etc/default/sling - Defaults file for location & path setup and to override any of the launchpad settings.
* SLING_DATA=/var/lib/sling - Local sling data dir.
* SLING_LOG_DIR=/var/log/sling - Sling log data.

TODO:
* Support clustered configurations.

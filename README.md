# Table of Contents

* [Hazelcast CLI](#hazelcast-cli)
* [Installing Hazelcast CLI](#installing-hazelcast-cli)
* [Requirements](#requirements)
  * [hazelcast-cli.properties](#hazelcast-cli-properties)
  * [SSH Configuration](#ssh-configuration)
* [Operations](#operations)

# Hazelcast CLI

Hazelcast CLI is a Hazelcast management tool, a command line interface to install, configure, and upgrade Hazelcast on the local machine or cloud on any operating system.

# Installing Hazelcast CLI

Run the following command to install Hazelcast CLI:

```brew install https://raw.githubusercontent.com/bilalyasar/homebrew/master/Library/Formula/hazelcast-cli.rb```

# Requirements

## hazelcast-cli.properties

You need to create a properties file in your `home` to define the host machines to run Hazelcast. Name the file as `hazelcast-cli.properties` and provide your host username, host IP and port in this file. Please see the below properties file content as an example:

```
europe1.user=ubuntu
europe1.ip=ec2-54-159-97-238.compute-1.amazonaws.com
europe1.port=22
```

## SSH configuration

Your public key has to be configured on the target machine.

# Operations

**Installing Hazelcast:**

`hazelcast --install --hostname europe1 --version 3.4.1`

**Starting a Hazelcast Member:**

`hazelcast --start --hostname europe1 --clustername wildcats --nodename tiger`

**Stopping a Hazelcast Member:**

`hazelcast --stop --hostname europe1 --clustername wildcats --nodename tiger`

**Starting Hazelcast Management Center:**

`hazelcast --startMC --hostname europe1`

**Rolling Upgrade Hazelcast Management Center:**

`hazelcast --upgrade --clustername wildcats --version 3.4.2`

# To Do

* More operating system support: apt-get, exe, Android.
* Starting Hazelcast bundled Tomcat.











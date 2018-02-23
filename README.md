#  Docker Enterprise Edition Demo and DevOps Showcase

This installation guide last updated at: **2018-02-23**

Ubuntu Version: **16.04**

Docker Enterprise Edition Version: **17.06.2-ee-6**

## Overview

![Viseo Digital Makers](images/viseo-digital-makers.png)
![Docker](images/docker-horizontal.png)

This demo and showcase consists of:

- Platform
  - **Ubuntu Linux**
  - **Docker Enterprise Edition**
    - Applications
      1. **Jenkins Continuous Integration Server**
      2. **Metrics and Events - TICK Stack**
        - InfluxDB
        - Telegraf
        - Chronograf
        - Kapacitor
      3. **Demo Web App**
        - ExpressJS app (Nodejs)
      4. **Blockchain Decentralized ID (DID) Authentication Demo**
        - KoaJS app (Nodejs)
      5. **Centralized logging**
        - Cloud service Scalyr.com
- Compliance as Code
  - **Inspec framework** for testing and auditing:
    1. Applications
    2. Infrastructure

## Prerequisites

1. [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
2. [Vagrant](https://www.vagrantup.com/)
3. From the Prerequisties [described here](https://docs.docker.com/engine/installation/linux/docker-ee/ubuntu/) begin with getting the Docker EE URL.
  - It will look like: *https://storebits.docker.com/ee/ubuntu/sub-xxxxx-xxxxx-xxxxx-xxxx-xxxxx-xxxx*

## Installation

- [Install Docker Enterprise Edition](install_docker.md)
- [Install Docker Trusted Registry](install_dtr.md)
- [Install Docker HTTP routing mesh](install_ucp_hrm.md)
- [Install Centralized Logging](install_centralized_logging.md)
- [Install Continuous Integration Server](install_continuous_integration_server.md)
- [Install Continuous Integration Jobs](install_continuous_integration_jobs.md)
- [Install Application Monitoring](install_monitoring.md)
- [Install Application Secrets](install_secrets.md)
- [Install Civic Web App](install_civic_web_app.md)
- [Install Demo Web App](install_demo_web_app.md)

## Compliance and Auditing

- [Install Inspec and execute tests](compliance/README.md)

## Appendix

1. Tick Stack Complete

![TICK Stack Complete](images/Tick-Stack-Complete.png)

2. Scalyr.com

![Scalyr.com](images/scalyr.png)
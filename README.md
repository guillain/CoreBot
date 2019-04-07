# CoreBot as chatbot framework
Chatbot framework based on **[botkit](https://botkit.ai/)**.

The idea is to provide a simple solution compatible with the most of
business messaging. This must be easy to deploy, set and maintain.
In that case the features and/or sketches developed are fully
compatible with all environments and made the development reusable in
the futures integrations.

Instead to code to create and deploy our chatbot with its own scenario,
build it by configuration!

## Advantage
- Generic setup is done to support all environment and settings
- Business messaging compatibilities:
    - Web (web server included)
    - Jabber
    - Cisco Webex Teams (Cisco Spark)
    - Microsoft Teams
    - Slack
    - Google Hangout
- The security is natively integrated with access list and privilege
management on controller and user level.
- All features can be used on controller level (preload) or when event
is triggered (loaded dynamically)
- Standard libraries to create quickly and properly new feature
- The configuration can be provided in a single file
[config.json](app/conf/default/config.json) or in splitted files. The configuration
can overload the default configuration of each feature.

## Features
All features are stored in the *controller* folders and they're loaded
with the help of a common script.

The non-exhaustive list is hereafter:
- NLP provided by [LUIS](https://botkit.ai/docs/readme-middlewares.html)
via the botkit feature
- Google translation
- BigData connector (to send info/tracking/APM data to a datalake)
- CSV file management
- autoreply (like echo)
- survey
- button
- ...

## Pre requisites
1. Python
  - 2.7
  - 3.5
2. Redis server
3. Internet access (Business Messaging and additional API)

## Fast Run
If need, add your **environment variables** in *.env file* or *OS env var* or in the *json configuration files*

### Locally
1. Clone the project **demo**:
`git clone https://github.com/guillain/CoreBot-demo.git`
2. Run it
`./run.sh`
### Docker
1. Clone the framework **CoreBot**:
`gt clone https://github.com/guillain/CoreBot-framework.git`
2. Run it:
`cd CoreBot-framework && ./image build && ./image run`

## Configuration
Thanks to read this [doc of configuration](https://github.com/guillain/CoreBot-doc/configuration.md).

## Installation
Thanks to read this [doc of installation](https://github.com/guillain/CoreBot-doc/installation.md).

To jump in the framework's logic, follow this [doc](https://github.com/guillain/CoreBot-doc/logic.md).

## How to add new feature?
Thanks to read the [HowTo add new](https://github.com/guillain/CoreBot-doc/add_new.md) doc to have get
the complete details of the standard and template to use.

If need you can complete your framework knowledge with the following
ones:

- [Framework Logic](https://github.com/guillain/CoreBot-doc/logic.md)

- [Controller](https://github.com/guillain/CoreBot-doc/controller.md)

- [Security](https://github.com/guillain/CoreBot-doc/security.md)


Don't hesitate to share yours creation ;-)

## Tips
Redis local record issue
- `redis-cli> config set stop-writes-on-bgsave-error no`

## Welcome on the CoreBot repository structure
0. [CoreBot](https://https://github.com/guillain/CoreBot)
    - Repository that regroups all CoreBot repositories

1. [CoreBot-framework](https://github.com/guillain/CoreBot-framework)
    - CoreBot framework based on the [Botkit](https://botkit.ai/) application

2. [CoreBot-Ansible](https://github.com/guillain/CoreBot-Ansible)
    - Ansible playbooks to deploy and maintain CoreBot-framework on dev, stage and
   production environment taken into account CI/CD pipeline

3. [CoreBot-doc](https://github.com/guillain/CoreBot-doc)
    - Documentation about CoreBot-framework

        1. GetStarted
            - [logic](https://github.com/guillain/CoreBot-doc/blob/master/logic.md)
            - [installation](https://github.com/guillain/CoreBot-doc/blob/master/installation.md)
            - [configuration](https://github.com/guillain/CoreBot-doc/blob/master/configuration.md)

        2. Component explanation
            - [controller](https://github.com/guillain/CoreBot-doc/blob/master/controller.md)
            - [launcher](https://github.com/guillain/CoreBot-doc/blob/master/launcher.md)

        3. Features
            - [add new](https://github.com/guillain/CoreBot-doc/blob/master/add_new.md)
            - [library](https://github.com/guillain/CoreBot-doc/blob/master/library.md)
            - [security](https://github.com/guillain/CoreBot-doc/blob/master/security.md)
            - [ToDo](https://github.com/guillain/CoreBot-doc/blob/master/ToDo.md)

        4. [CoreBot-demo](https://github.com/guillain/CoreBot-demo)
            - Example of CoreBot application packaging for on-prem or on-cloud integration


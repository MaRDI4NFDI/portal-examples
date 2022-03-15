
Prerequisites
===============
This requires docker-compose >=1.28.5 


Make sure your local portal-compose docker-compose-dev has the following addition:
```
networks:
    default:
    external: true
    name: portal-compose_default
```
Run  `docker network create portal-compose_default` to create the network.
Start the portal with docker-compose.

See the examples
================
The examples are rendered online on GitHub. ***You do not need to clone the project to see the examples.***

Edit the examples
==================

1. Clone the project. 
2. Create a bot user in the wikibase using the wikibase GUI (Special:BotPasswords), note down the name and password of the bot user.
3. Create a config file by copying `data/credentials.tpl` to `data/credentials.ini` and replace bot name and password as required.
4. Start the containers by calling docker-compose:

`docker-compose -f docker-compose.yml up -d`


The Jupyter Notebooks can be found at: `http://localhost:8889/lab`

OpenRefine can be found at: `http://localhost:3334`

What's included
===============
Jupyter [Scipy-Notebook](https://jupyter-docker-stacks.readthedocs.io/en/latest/using/selecting.html#jupyter-scipy-notebook) with Pandas etc.
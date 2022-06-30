## Mautic 
============================
Mautic is the world's largest open source marketing automation project. With over 200,000 organisations using Mautic and over 1,000 community volunteers, we empower businesses by making it easy to manage their marketing across a range of channels.


# Quick start

The easiest way to start mautic with Mariadb is using Docker Compose. Just clone this repo and run following command in the root directory. The default docker-compose.yml uses Mariadb and phpMyAdmin.

### Install

## Using DECK
Install mautic from the DECK marketplace and follow the instructions on the GUI

### From terminal with Docker
```
git clone https://github.com/deck-app/mautic.git
cd mautic
```
Edit .env file to change any setting before installing like mautic, mariadb, php etc
```
docker-compose up -d
```
### Modifying project settings

From the DECK app, go to stack list and click on project's `More > configure > Advanced configuration` Follow the instructions below and restart your stack from the GUI

##### Edit Apache configuration

httpd.conf is located at `./mautic/httpd.conf`

##### Edit Nginx configuration

httpd.conf is located at `./mautic/default.conf`

#### Editing php.ini

PHP ini file is located at `./mautic/php.ini`

##### Rebuilding from terminal

You have to rebuild the docker image after you make any changes to the project configuration, use the snippet below to rebuild and restart the stack
```
docker-compose stop && docker-compose up --build -d
```

# License

Mautic is distributed under the GPL v3 license. Full details of the license can be found in the [Mautic GitHub repository](https://github.com/mautic/mautic/blob/staging/LICENSE.txt).
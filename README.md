## Dockerized PHP 5.6

### Status
<img alt="Image Size" src="https://img.shields.io/docker/image-size/salalex/php5.6" style="max-width:100%;"> <img alt="Docker Pulls" src="https://img.shields.io/docker/pulls/salalex/php5.6" style="max-width:100%;"> <img alt="Build Status" src="https://img.shields.io/docker/cloud/build/salalex/php5.6?logo=docker" style="max-width:100%;"> <img alt="Licenses" src="https://img.shields.io/badge/License-GPLv3-blue.svg" style="max-width:100%;">

### Table of contents
* [Prerequisites](#Prerequisites)
* [Project Tree](#Project-Tree)
* [Backup Folder](#Backup-Folder)
* [Config Folder](#Config-Folder)
* [Rename](#Rename)
* [Deployment](#Deployment)
* [Credits](#Credits)

For PHP5.6-FPM with Nginx use ![Dockerized PHP5.6-FPM with Nginx](https://github.com/eduardevops/dockerized-php5.6-fpm)

### Prerequisites
*	[Docker](https://www.docker.com/)
*	[Docker Compose](https://docs.docker.com/compose/install/)

### Project Tree
```less
├── .env.db
├── Dockerfile
├── backup
│   ├── db_backup.sh
│   ├── db_restore.sh
│   ├── web_backup.sh
│   └── web_restore.sh
├── conf
|   ├── php.ini
│   └── website.conf
├── docker-compose.yml
└── web
    └── index.php
```

### Backup Folder
| File                        | Description                              |
| :-------------------------- |:---------------------------------------- |
| db_backup.sh                | Small script to backup MySQL database    |      
| db_restore                  | Small script to backup web Folder        |
| web_backup.sh               | Small script to restore MySQL database   |
| web_restore.sh              | Small script to restore web Folder       |

### Config Folder
| File                        | Description                              |
| :-------------------------- |:------------------------------------------------------------------------------------ |
| php.ini                     | For additional configurations of PHP, еdit this file before deploying the container. |  
| website.conf                | Apache2 basic vhost file.  

### Rename
It is highy advised to change all names.

### Deployment
Clone repo to your server.
```less
sudo git clone https://github.com/<this-repo>.git
```

Put your website files (e.g. html, php, ..) into the ```web``` subfolder.

Navigate to the project folder and start containers.

```less
cd /path/to/project/folder
docker-compose up -d
```

----

### Credits
The contents of this repository are based on following original sources:
- [github.com/eduardevops/dockerized-php5.6](https://github.com/eduardevops/dockerized-php5.6)

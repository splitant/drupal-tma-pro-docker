# Drupal TMA pro docker

## About The Project

The goal is to set up fastly a local Drupal project with docker environment for third party application maintenance projects.

### Built With

* [Docker4Drupal](https://github.com/wodby/docker4drupal)

## Drupal version 7

For Drupal 7.X versions.

### Installation

   ```sh
   git checkout drupal-7
   make create-setup <project> <repo-git>
   cd ../<project>-docker
   make copy-env-file
   # Fill env file
   make up
   make drupal-install
   ```

### New project

   ```sh
   git checkout drupal-7
   make create-init <project>
   cd ../<project>-docker
   make copy-env-file
   # Fill env file
   make init
   ```

## Drupal version 8^(+)

For Drupal 8.X, 9.X versions.

### Installation

   ```sh
   git checkout master
   make create-setup <project> <repo-git>
   cd ../<project>-docker
   make copy-env-file
   # Fill env file
   # optionally fill GITLAB_TOKEN in .env and `make gitlab-auth`
   make setup
   ```

### New project

   ```sh
   git checkout master
   make create-init <project>
   cd ../<project>-docker
   make copy-env-file
   # Fill env file
   make init
   ```

## Nota

* XDEBUG Drush in container : `DRUSH_ALLOW_XDEBUG=1 drush <drush-command-name>`

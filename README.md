# dockenv

This is set of bash scripts to help manage developers environment based on Docker's containers.
Assumption is that you have a set of common developers tools already installed on you host machine
and you just want some additional ones for secific project. 

## General idea

For every environment you have to create configuration with list of images and commands to run in containers
run from this images. When a command is first time used, contaner is created and from now this command is run as
`docker exec` in the created container. After work on project is done, you can stop all containers with one command.

## Requirements
 * GNU/Linux 
 * Bash
 * Docker
 * direnv 
 * yq >= 3.0.0

## Setup

## Usage

## Tests

Tested manually on:
 * Ubuntu 16.04 
 * Bash 4.3.48 
 * direnv 2.23.1 
 * yq 3.4.1
 * Docker 19.03.13 

## Licence

This project is licensed under terms of **MIT** licence.


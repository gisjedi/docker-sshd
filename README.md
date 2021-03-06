# docker-sshd
Configuration injectable Docker images of sshd

## Usage

These images can be used out of the box for a simple ssh server that defaults to user ubuntu:ubuntu without sudo privileges. No password login is allowed and a public key must be supplied for the authorized_keys file via AUTHORIZED_KEYS environment variable. The following environment variables can be used to customize the behavior of the image:

* AUTHORIZED_KEYS: _Must_ be set with the string to inject for the authorized_keys file.
* NOPASSWD: Set to `true` to enable sudo for all users in sudo group (default is false).
* PASSWORD: The password to be set for user (default is the same as username).
* SUDO: Set to `true` to enable sudo for specified user (default is false).
* USERNAME: The username to create enabled for access via ssh client (default is `ubuntu` or `centos`)

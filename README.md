[![Build Status](https://travis-ci.org/jgeusebroek/ansible-role-java.svg?branch=master)](https://travis-ci.org/jgeusebroek/ansible-role-java)
[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-jgeusebroek.java-blue.svg)](https://galaxy.ansible.com/jgeusebroek/java)

# Ansible role: Java

An Ansible Role that installs Java on RedHat/CentOS or Debian/Ubuntu.

## Requirements

None

## Dependencies

None

## Example Playbook

    ---
    - hosts: all
      become: true

      roles:
         - { role: jgeusebroek.java, tags: ["java"] }

## Example Variables

    java_packages:
      - java-1.8.0-openjdk

When omitted defaults to:

	openjdk-8-jdk (Debian/Ubuntu)
	java-1.7.0-openjdk (Redhat/CentOS)

Should you need another Java version, make sure this version is available for the distribution package manager and define the `java_packages` variable.

For example using the Debian Backports repository install Java 8 with the `openjdk-8-jdk` package.

## License

MIT / BSD

## Author Information

This role was created in 2017 by [Jeroen Geusebroek](http://jeroengeusebroek.nl/). Forked from Jeff Geerling's Java role.

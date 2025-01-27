# SonarQube on OpenShift 3.x/4.x
This repo contains all of the resources required to build an OpenShift-specific
Docker image of SonarQube.

It is inspired by the upstream SonarQube Docker image:
https://github.com/SonarSource/docker-sonarqube

Forked from OpenShiftDemos/sonarqube-openshift-docker

# Docker Hub

Images are taken from official SonarQube Docker Hub at: https://hub.docker.com/_/sonarqube

# Deploy on OpenShift
You can do use the provided templates with an embedded or postgresql database to deploy SonarQube on 
OpenShift:

SonarQube with Embedded H2 Database:

    oc new-app -f sonarqube-template.yaml --param=SONARQUBE_VERSION=8.8.0-community

SonarQube with PostgreSQL Database:

    oc new-app -f sonarqube-postgresql-template.yaml --param=SONARQUBE_VERSION=8.8.0-community
    
It will works also on OpenShift 4.x

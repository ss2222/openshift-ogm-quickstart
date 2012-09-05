# OGM Kitchensink 

## What is it?

ogm-kitchensink is a [OGM](http://www.hibernate.org/subprojects/ogm.html) demo app for [AS 7](http://www.jboss.org/jbossas) based on
[kitchensink](https://github.com/jbossas/quickstart/tree/master/kitchensink)

## Install OpenShift command line tools

    gem install rhc

## Create OpenShift namespace and app (named "ogm" for example)

    rhc domain create -l <login_email> -n <namespace>
    rhc app create -a ogm -t jbossas-7
    rhc app cartridge add -a ogm -c mongodb-2.0

## Grab this quickstart codes and make it working for you!

    cd ogm
    git remote add upstream -m master git://github.com/openshift/openshift-ogm-quickstart.git
    git pull -s recursive -X theirs upstream master
    git push

## That's it, you can now checkout your app at:

    http://ogm-<namespace>.rhcloud.com

ODP
===

Open Data Portal based on CKAN


What is this?
-------------

This repository will contain a customized and themed version of CKAN.

[CKAN](http://ckan.org/) is Open Source data portal software written in Python by the [Open Knowlegde Foundation](http://en.wikipedia.org/wiki/Open_Knowledge_Foundation).



Installation
------------

 - Install PostgreSQL, Solr/Jetty (and for testing deployment: apache, nginx)

```
$ sudo apt-get update
$ sudo apt-get install build-essential
$ sudo apt-get install nginx apache2 libapache2-mod-wsgi libpq5
$ sudo apt-get install postgresql solr-jetty
$ sudo apt-get install postgresql-server-dev-9.1
```

 - Install git, pip and python-dev

```
$ sudo aptitude install python-pip python-dev git
```
 - Use pip to install virtualenv

```
$ sudo pip install virtualenv
```
 
 - Create a new virtualenv:

```
$ virtualenv --no-site-packages ckan_development
```

 - Inside the virtualenv, issue:

```
$ cd ckan_development
$ pip install -e 'git+https://github.com/okfn/ckan.git#egg=ckan'
```

 - That will install CKAN into the src/ directory of your virtualenv.
 - Issue the following from the root of the virtualenv, to install the required Python packages:

```
$ pip install -r src/ckan/requirements.txt
```
 - That should perform a local install of SQLAlchemy, Beaker, Babel, Jinja, Gensha, Paste and a bunch of other libs needed by CKAN. It'll take a while, especially since it will build some libs from source.



# DEPRECATED
This repository is deprecated and is not in use anymore.
For any question, please reach out to our support team: https://app.datadoghq.com/help


This repository contains a collection of modules needed by [Datadog](http://www.datadoghq.com)'s
[Agent](https://github.com/DataDog/dd-agent)

Details
=======

python-meld3
------------

Ubuntu 11.04 has a broken python-meld3 package that won't let supervisor run properly.
This package is tested on 11.04 and 10.04.

python-tornado
--------------

A dependency of `datadog-agent`.

Packaging
=========

python-tornado
--------------

You can find the source [here](https://github.com/DataDog/tornado).

On a CentOS box with python 2.6, run:
    
    git checkout v2.3.0-dd
    python setup.py bdist_rpm --obsoletes python26-tornado --packager="Datadog <package@datadoghq.com>" \
    --requires='python(abi) = 2.6'
    
where N is the build number.

On debian you need `python-stdeb`

    sudo apt-get install python-stdeb
    python setup.py --command-packages=stdeb.command bdist_deb

and the deb is in `deb_dist`.

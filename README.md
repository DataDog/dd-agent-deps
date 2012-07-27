This repository contains a collection of modules needed by [Datadog](http://www.datadoghq.com)'s
[Agent](https://github.com/DataDog/dd-agent)

Details
=======

python-meld3
------------

Ubuntu 11.04 has a broken python-meld3 package that won't let supervisor run properly.
This package is tested on 11.04 and 10.04.

Packaging
=========

python-tornado
--------------

You can find the source [here](https://github.com/DataDog/tornado).

On a CentOS box, get python(2.6) and run:
    
    python26 setup.py bdist_rpm --python python26 --obsoletes python26-tornado --release N
    
where N is the build number.


This repository contains a collection of modules needed by [Datadog](http://www.datadoghq.com)'s
[Agent](https://github.com/DataDog/dd-agent)

Packaging
=========

python-tornado
--------------

You can find the source [here](https://github.com/DataDog/tornado).

On a CentOS box, get python(2.6) and run:
    
    python26 setup.py bdist_rpm --python python26 --obsoletes python26-tornado --release N
    
where N is the build number.

tns
==========

tns is a name server based on twork

Environment
------------
* [virtualenv](http://www.virtualenv.org/en/latest/)

Requirements
------------
The following libraries are required

* [tornado](http://github.com/facebook/tornado)
* [pyutil](https://github.com/bufferx/pyutil)

Usage & Debug
------------
* source $VIRTUALENV/bin/activate
* cd $TORNADO_PATH && python setup.py install
* cd $PYUTIL_PATH && python setup.py install
* python tns/bin/tnsd.py -bind_ip=localhost -port=8000
* or tnsd -bind_ip=localhost -port=8000

Deploy
------------
* source $VIRTUALENV/bin/activate
* cd $TORNADO_PATH && python setup.py install
* cd $PYUTIL_PATH && python setup.py install
* python setup.py build_py -O2 bdist_egg --exclude-source-files
* easy_install dist/tns-VERSION-PYTHON.egg

Supervisor
------------
* [supervisord](http://supervisord.org/)
* [conf-template](https://github.com/bufferx/supervisor_conf_tpl)
* command: python -OO $VIRTUALENV/bin/tnsd -config=$TNS_CONFIG_PATH

Case
------------
* http://localhost:8000/v1.0/tns/stat

Issues
------

Please report any issues via [github issues](https://github.com/bufferx/tns/issues)

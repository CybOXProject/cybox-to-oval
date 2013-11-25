CybOX XML to OVAL XML Converter
===============================

Convert CybOX XML to OVAL XML

**Version** 0.2 BETA

    Copyright (c) 2013 - The MITRE Corporation
    All rights reserved. See LICENSE.txt for more details.

    BY USING THIS PROGRAM, YOU SIGNIFY YOUR ACCEPTANCE OF THE TERMS AND CONDITIONS
    OF USE.  IF YOU DO NOT AGREE TO THESE TERMS, DO NOT USE THIS PROGRAM.

Overview
--------
The CybOX-to-OVAL script generates OVAL 5.7 definitions, tests, and objects
from a CybOX document. Currently this is limited to CybOX's File and WinRegistryKey 
objects.

Compatible with:
* [CybOX 2.0.1](http://cybox.mitre.org/language/version2.0.1/)
* [OVAL 5.7](https://oval.mitre.org/archive/version5.7/index.html)

Installation
------------

Download and extract the included files into your directory of choice. 

CybOX-to-OVAL requires Python 2.X. It was developed using Python 2.7, and may work 
under Python 2.6. It is not compatible with Python 3.

### Dependencies 

* [python-cybox](https://pypi.python.org/pypi/cybox) - A Python library for CybOX

You can install the dependencies using pip:

    $ pip install cybox

**NOTE**: Installing LXML (which python-cybox depends on) on Ubuntu requrires the
python-dev, libxml2-dev, and libxslt1-dev packages to be installed. 
Follow the link for instructions on installing python-cybox and LXML on Windows.


Usage
-----

    python cybox_to_oval.py <flags> -i <cybox xml file> -o <oval xml file>
    
    Available Flags:
        -v: Verbose output mode. Lists any skipped observable items and also prints traceback for errors.
        
### Example files

OpenIOC-to-CybOX comes with example input and output files. You can use these to see an example
of the program's output, or to verify that you have installed the program correctly:    
        
    $ python cybox_to_oval.py -i examples/cybox.in.xml -o oval.xml
    $ diff oval.xml examples/oval.out.xml
    
The cybox.in.xml file contains one FileObject and one WinRegistryKey object.

Contributing
------------

Bug reports and feature requests are welcome and encouraged. Pull requests are especially appreciated. 
Feel free to use the issue tracker on GitHub or send an email directly to <cybox@mitre.org>.

More information
----------------

* CybOX - http://cybox.mitre.org/
* OVAL - http://oval.mitre.org/

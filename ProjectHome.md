## Overview ##
**formlayout** is a tiny Python module for creating form dialogs/widgets to edit various type of parameters with having to write any GUI code (it requires Python 2.5+ and PyQt4 4.3+ or PySide 1.1+).

The main advantage of **formlayout** over similar libraries is that it's very simple to use/install and that it's so light (it just needs PyQt4 or PySide to run). However, if you are looking for more advanced automatic GUI generation, try the [guidata](http://code.google.com/p/guidata/) library: this is an incredible combination of simplicity and power (and its compatible with PyQt4 and mostly with PySide too).

## Installation ##
**formlayout** supports both Python 2.6-2.7 and Python 3. It requires PyQt4 4.3+ or PySide 1.1+:
  * All supported platforms (GNU/Linux, MacOS and Microsoft Windows XP/Vista): install Python and PyQt4
  * Microsoft Windows XP/Vista: note that [Python(x,y)](http://www.pythonxy.com) and [WinPython](http://code.google.com/p/winpython/) (scientific-oriented Python distributions) include formlayout
Installation instructions:
  * [Python(x,y)](http://www.pythonxy.com) and [WinPython](http://code.google.com/p/winpython/): nothing to do, it's already included
  * Without _setuptools_: download the .tar.gz file, extract files and type `python setup.py install`
  * With _setuptools_: simply type `easy_install formlayout`


## Simple example ##
The main feature of **formlayout** is to provide the `fedit` function which transforms a list of parameters into a GUI-based form (you may also create a list of parameter lists - see `formlayout.py` for more advanced examples):
```
from formlayout import fedit

datalist = [('Name', 'Paul'),
            ('Age', 30),
            ('Sex', [0, 'Male', 'Female']),
            ('Size', 12.1),
            ('Eyes', 'green'),
            ('Married', True),
            ]

print "result:", fedit(datalist, title="Describe yourself",
                       comment="This is just an <b>example</b>.")
```
Here is the generated GUI dialog box:

![http://formlayout.googlecode.com/files/example.png](http://formlayout.googlecode.com/files/example.png)

And here is the result return by `fedit`:
```
[u'Paul', 30, 'Male', 12.1, u'#008000', True]
```
That's all!


## Advanced example: Pydee ##
**formlayout** is used in [Pydee](http://code.google.com/p/pydee/) (project renamed to [Spyder](http://code.google.com/p/spyderlib/) in 2009) to implement the matplotlib settings dialog box:

![http://formlayout.googlecode.com/files/fo1.png](http://formlayout.googlecode.com/files/fo1.png)
![http://formlayout.googlecode.com/files/fo2.png](http://formlayout.googlecode.com/files/fo2.png)

Integration in Pydee (http://code.google.com/p/pydee/):

![http://formlayout.googlecode.com/files/fo3.png](http://formlayout.googlecode.com/files/fo3.png)
Ascopy
=====

**Ascopy** is an MIT licensed Python implementation of Yuan et al.'s
`Copula method for correlation analysis 
<https://arxiv.org/abs/2203.06700>`_ and these pages will
show you how to use it.

This documentation won't teach you too much about Copula but there are a lot
of resources available for that (try `this one
<https://en.wikipedia.org/wiki/Copula>`_).
Our `paper <https://arxiv.org/abs/1810.12713>`_ explaining 
the Ascopy algorithm and implementation in detail. Ascopy is being actively developed on `GitHub <https://github.com/yuanzunli/Ascopy>`_.

.. image:: https://img.shields.io/badge/GitHub-wenjie-astro%2FAscopy-blue.svg?style=flat
    :target: https://github.com/wenjie-astro/Ascopy
.. image:: https://img.shields.io/badge/arXiv-1810.12713-red
    :target: https://arxiv.org/abs/1810.12713
.. image:: https://img.shields.io/badge/arXiv-1810.12713-brightgreen
    :target: https://arxiv.org/abs/1810.12713
.. image:: https://img.shields.io/badge/license-MIT-blue.svg?style=flat
    :target: https://github.com/yuanzunli/kdeLF/blob/master/LICENSE
.. image:: https://pepy.tech/badge/Ascopy
    :target: https://pepy.tech/project/Ascopy


Basic Usage
-----------

If you want to perform a Copula modeling or nction based on a survey data, you would do
something like:

.. code-block:: python

    import numpy as np
    import Ascopy as ac

    with open('data.txt', 'r') as f: 
        x, y= np.loadtxt(f, usecols=(0,1), unpack=True)  

    test = ac.Copula(x=x, y=y, copula_num=21, PDFx='norm', PDFy='norm')
    test.run_mcmc() 
    res = test.plot_regress(sigma=3)

A more complete example is available in the :ref:`quickstart` tutorial.


How to Use This Guide
---------------------

To start, you're probably going to need to follow the :ref:`install` guide to
get Ascopy installed on your computer.
After you finish that, you can probably learn most of what you need from the
tutorials listed below (you might want to start with
:ref:`quickstart` and go from there).
If you need more details about specific functionality, the User Guide below
should have what you need.

We welcome bug reports, patches, feature requests, and other comments via `the GitHub
issue tracker <https://github.com/wenjie-astro/Ascopy/issues>`_, but you should check out the
`contribution guidelines <https://github.com/wenjie-astro/Ascopy/blob/main/CONTRIBUTING.md>`_
first.



.. toctree::
   :maxdepth: 2
   :caption: User Guide

   user/install
   user/Ascopy
   user/faq

.. toctree::
   :maxdepth: 1
   :caption: Tutorials

   tutorials/quickstart
   tutorials/plot
   tutorials/parallel
   tutorials/KS-test
   tutorials/MCMC


License & Attribution
---------------------

Copyright 2022 Zunli Yuan and contributors.

kdeLF is free software made available under the MIT License. For details
see the ``LICENSE``.


Citation
--------

Please cite the following papers if you found this code useful in your
research:

    
- Yuan, Z., Zhang, X., Wang, J., Cheng, X., & Wang, W. 2022, ApJS, 260, 10 (`arXiv <https://arxiv.org/abs/2203.06700>`_, `ADS <https://ui.adsabs.harvard.edu/abs/2022ApJS..260...10Y>`_, `BibTeX <https://ui.adsabs.harvard.edu/abs/2022ApJS..260...10Y/exportcitation>`_).

- Yuan, Z., Jarvis, M. J., & Wang, J. 2020, ApJS, 248, 1 (`arXiv <https://arxiv.org/abs/2003.13373>`_, `ADS <https://ui.adsabs.harvard.edu/abs/2020ApJS..248....1Y>`_, `BibTeX <https://ui.adsabs.harvard.edu/abs/2020ApJS..248....1Y/exportcitation>`_).



Contributors
------------

- Wenjie Wang

Changelog
---------

.. include:: ../HISTORY.rst

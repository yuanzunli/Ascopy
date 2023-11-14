.. _install:

Installation
============

Using pip
---------

The recommended way to install the stable version of Ascopy is using
`pip <http://www.pip-installer.org/>`_

.. code-block:: bash

    pip install -U Ascopy

We have uploaded several `.whl` files to the `PyPI <https://pypi.org/project/Ascopy/>`_ web to support as many platforms as possible. If your platforms happens to be an exception, then the pip installation may fail. In this situation, you need to install the `Intel fortran Compiler <https://www.intel.com/content/www/us/en/developer/articles/news/free-intel-software-developer-tools.html>`_ first, and then try the pip installation again. Note that the version of NumPy library should ≥ 1.21.0. If you use the latest Intel fortran Compiler, then a higher version (≥ 1.22) of NumPy is required. If you have problems installing, please open an issue at `GitHub <https://github.com/yuanzunli/kdeLF/issues>`_.


From source
-----------

You can also install *Ascopy* after a download from `GitHub <https://github.com/wenjie-astro/Ascopy/>`_. Note that this requires a `Intel fortran Compiler <https://www.intel.com/content/www/us/en/developer/articles/news/free-intel-software-developer-tools.html>`_ to be installed in advance.

.. code-block:: bash

    git clone https://github.com/wenjie-astro/Ascopy.git
    cd kdeLF
    pip install .


Test the installation
---------------------

To make sure that the installation went alright, you can execute the built-in test program in kdeLF by running the following command:

.. code-block:: bash

    python3 -m Ascopy.test_ascopy

.. image:: https://github.com/pytest-dev/pytest/raw/main/doc/en/img/pytest_logo_curves.svg
   :target: https://docs.pytest.org/en/stable/
   :align: center
   :height: 200
   :alt: pytest


------

.. image:: https://img.shields.io/pypi/v/pytest.svg
    :target: https://pypi.org/project/pytest/

.. image:: https://img.shields.io/conda/vn/conda-forge/pytest.svg
    :target: https://anaconda.org/conda-forge/pytest

.. image:: https://img.shields.io/pypi/pyversions/pytest.svg
    :target: https://pypi.org/project/pytest/

.. image:: https://codecov.io/gh/pytest-dev/pytest/branch/main/graph/badge.svg
    :target: https://codecov.io/gh/pytest-dev/pytest
    :alt: Code coverage Status

.. image:: https://github.com/pytest-dev/pytest/workflows/test/badge.svg
    :target: https://github.com/pytest-dev/pytest/actions?query=workflow%3Atest

.. image:: https://results.pre-commit.ci/badge/github/pytest-dev/pytest/main.svg
   :target: https://results.pre-commit.ci/latest/github/pytest-dev/pytest/main
   :alt: pre-commit.ci status

.. image:: https://img.shields.io/badge/code%20style-black-000000.svg
    :target: https://github.com/psf/black

.. image:: https://www.codetriage.com/pytest-dev/pytest/badges/users.svg
    :target: https://www.codetriage.com/pytest-dev/pytest

.. image:: https://readthedocs.org/projects/pytest/badge/?version=latest
    :target: https://pytest.readthedocs.io/en/latest/?badge=latest
    :alt: Documentation Status

.. image:: https://img.shields.io/badge/Discord-pytest--dev-blue
    :target: https://discord.com/invite/pytest-dev
    :alt: Discord

.. image:: https://img.shields.io/badge/Libera%20chat-%23pytest-orange
    :target: https://web.libera.chat/#pytest
    :alt: Libera chat


The ``pytest`` framework makes it easy to write small tests, yet
scales to support complex functional testing for applications and libraries.

Running pytest on Windows
-------------------------

An example of a simple test:

.. code-block:: python

    # content of test_sample.py
    def func(x):
        return x - 7


    def test_answer():
        assert func(7) == 1


To execute it via terminal::

   PS C:\Users\XXX\XXX\XXX> pytest
   ======================================================================================================== test session starts ========================================================================================================
   platform win32 -- Python 3.11.6, pytest-7.4.2, pluggy-1.3.0
   rootdir: C:\Users\XXX\XXX\XXX
   plugins: anyio-4.0.0
   collected 1 item

   test_sample.py F                                                                                                                                                                                                               [100%]

   ============================================================================================================= FAILURES ==============================================================================================================
   ____________________________________________________________________________________________________________ test_answer ____________________________________________________________________________________________________________

    def test_answer():
   >       assert func(7) == 1
   E       assert 0 == 1
   E        +  where 0 = func(7)

   test_sample.py:6: AssertionError
   ====================================================================================================== short test summary info ====================================================================================================== 
   FAILED test_sample.py::test_answer - assert 0 == 1
   ========================================================================================================= 1 failed in 0.08s ========================================================================================================= 
This first example is a failed test.



Due to ``pytest``'s detailed assertion introspection, only plain ``assert`` statements are used. See `getting-started <https://docs.pytest.org/en/stable/getting-started.html#our-first-test-run>`_ for more examples.


Features
--------

- Detailed info on failing `assert statements <https://docs.pytest.org/en/stable/how-to/assert.html>`_ (no need to remember ``self.assert*`` names)

- `Auto-discovery
  <https://docs.pytest.org/en/stable/explanation/goodpractices.html#python-test-discovery>`_
  of test modules and functions

- `Modular fixtures <https://docs.pytest.org/en/stable/explanation/fixtures.html>`_ for
  managing small or parametrized long-lived test resources

- Can run `unittest <https://docs.pytest.org/en/stable/how-to/unittest.html>`_ (or trial),
  `nose <https://docs.pytest.org/en/stable/how-to/nose.html>`_ test suites out of the box

- Python 3.8+ or PyPy3

- Rich plugin architecture, with over 850+ `external plugins <https://docs.pytest.org/en/latest/reference/plugin_list.html>`_ and thriving community


Documentation
-------------

For full documentation, including installation, tutorials and PDF documents, please see https://docs.pytest.org/en/stable/.


Bugs/Requests
-------------

Please use the `GitHub issue tracker <https://github.com/pytest-dev/pytest/issues>`_ to submit bugs or request features.


Changelog
---------

Consult the `Changelog <https://docs.pytest.org/en/stable/changelog.html>`__ page for fixes and enhancements of each version.


Support pytest
--------------

`Open Collective`_ is an online funding platform for open and transparent communities.
It provides tools to raise money and share your finances in full transparency.

It is the platform of choice for individuals and companies that want to make one-time or
monthly donations directly to the project.

See more details in the `pytest collective`_.

.. _Open Collective: https://opencollective.com
.. _pytest collective: https://opencollective.com/pytest


pytest for enterprise
---------------------

Available as part of the Tidelift Subscription.

The maintainers of pytest and thousands of other packages are working with Tidelift to deliver commercial support and
maintenance for the open source dependencies you use to build your applications.
Save time, reduce risk, and improve code health, while paying the maintainers of the exact dependencies you use.

`Learn more. <https://tidelift.com/subscription/pkg/pypi-pytest?utm_source=pypi-pytest&utm_medium=referral&utm_campaign=enterprise&utm_term=repo>`_

Security
^^^^^^^^

pytest has never been associated with a security vulnerability, but in any case, to report a
security vulnerability please use the `Tidelift security contact <https://tidelift.com/security>`_.
Tidelift will coordinate the fix and disclosure.


License
-------

Copyright Holger Krekel and others, 2004.

Distributed under the terms of the `MIT`_ license, pytest is free and open source software.

.. _`MIT`: https://github.com/pytest-dev/pytest/blob/main/LICENSE

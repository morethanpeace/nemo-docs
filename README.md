# NEMO/ELMO Documentation

## Local Build Instructions

Requirements

* Python 2.7 or higher
* Python packages:
    * `sphinx` (1.7 or higher)
    * `sphinx-intl`
    * `transifex-client`

Building:

~~~ python
make html
~~~

## Pulling and Buliding Translations

Once changes are made to the PO file in Transifex:

Pull changes from Transifex to local repo (replace "fr" with the language code you are translating)

~~~ python
tx pull -l fr
~~~

Building:

~~~ python
make -e SPHINXOPTS="-D language='fr'" html
~~~

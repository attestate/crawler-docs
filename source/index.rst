@attestate/crawler
==================

The ``@attestate/crawler`` is a Node.js framework for scalably querying
Ethereum's JSON-RPC endpoints and to slice out portions of the Ethereum
network's data for local usage.

To modularize the crawler's data sources, developers can implement custom
strategies or re-use existing ones to compose crawl paths. Conceptually, the
crawler implements the Extract, Transform and Load separation, to minimize
downtime, dependencies on external interfaces and to increase reproducability.

The entire project is licensed licensed under the GPL3, to make it truly owned
by the community instead of a single entity. Branded as the "Neume Network",
the Attestate Crawler codebase has successfully been used to download the
metadata of the music NFT ecosystem.

Developers can integrate with Attestate's crawler in two ways for now:

#. From the command line of a UNIX-compatible system
#. From within JavaScript as an NPM dependency.

Table of Contents
-----------------

.. toctree::
  :caption: Basics

  getting-started

.. toctree::
  :caption: Strategies

  strategies/call-block-logs

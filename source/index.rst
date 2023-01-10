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

Why use `@attestate/crawler`?
-----------------------------

Copying a smart contract's state locally is difficult and requires a lot of
engineering.

Ethereum full node cloud providers like Alchemy are rate-limiting requests
which can lead to failures. Synchronizing a process's state with Ethereum's continuous block production is
challenging.

Turn-key solutions like The Graph Protocol exist but their goal is to replicate
contract storage and so external data sources cannot be integrated.
Additionally, it is often not enough to query contract state.

For example, to build a music NFT player, a developer isn't interested in
knowing all NFTs. Rather, they want to have a list of all unique songs (a
derivative of all NFTs) registered on Ethereum.

This is where Attestate's crawler comes in: It enables developers to build
derivative views from many data sources. It reduces the complexity of dealing
with data sources, makes extracting data super fast and implements resumability
into the crawling process.

Features
--------

* Complexity of dealing with data sources is simplified (rate-limiting support, retrying after error, reliably persisting crawl results)
* Fastest way to slice out on-chain data: 1 TB/h with a co-located Erigon node.
* Resumable crawls with isolated stages for transformation to minimize costly network requests.
* No token launch, no miners, no fees: Just a collaboratively developed GPL-3 free software project.
* Indexing off-chain data sources other than Ethereum is possible: IPFS, Arweave, HTTPS, GraphQL).
* Database-agnostic: Can be integrated with any type of database.

.. warning::
  We're currently actively working on these documents. They're still far from acurate or trustworthy.

Table of Contents
-----------------

.. toctree::
  :caption: Basics

  getting-started
  configuration

.. toctree::
  :caption: Strategies

  strategies/call-block-logs

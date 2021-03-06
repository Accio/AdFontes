---
layout: post
title: Learning Logstash - Part I
category: programming
tags: ELK Logstash ElasticSearch
---

Logstash a component of the *ELK* stack. *ELK* is the acronym of
*Elasticsearch*, *Logstash*, and *Kibana*. I learned how to use it with
examples.

* TOC
{:toc}

## The ELK stack

Yes, the acronym *ELK* was chosen to fit the common name of the animal *Cervus
canadensis*, the oldest in the deer family.

{% include image.html
url="https://upload.wikimedia.org/wikipedia/commons/thumb/5/55/Rocky_Mountain_Bull_Elk.jpg/300px-Rocky_Mountain_Bull_Elk.jpg"
description="An Elk. Photo in the public domain, taken by Wikimedia user MONGO."
%}

In short:

* *ElasticSearch* provides full-text indexing and search. It is a multi-server
    implementation of the Lucene engine, which is a Java-based indexing and
    full-text search engine.
* *Logstash* is a data-processing pipeline running on the server side that
  ingests[^1] data from multiple sources, transforms it, and sends it to a
  &ldquo;stash&rdquo; like ElasticSearch [^2].
* *Kibana* allows user visualize data in ElasticSearch.

## Logstash can deal with much more than logs

Logstash can convert virtually any type of data, for instance tab-delimited
files, into JSON objects that can be stored in ElasticSearch, which can then be
indexed and searched. Therefore, despite the word 'log' in its name, Logstash
can be applied to any type of structured data that we wish to index and search.
This can, for instance, also include gene annotation and phenotype data (or
known as metadata) in omics studies.

## Installation

It is possible to install Logstash from source files, which can be downloaded at
[elastic.co](https://www.elastic.co/downloads/logstash). Alternatively, one can
install it from package managers, for instance
[apt](https://www.elastic.co/guide/en/logstash/7.7/installing-logstash.html#_apt)
on Debian systems, or run it from a Docker container. The download
page gives clear instructions.

Now we have installed Logstash, we can run it to convert virtually any data into
JSON files. We will explore this in the next part of the tutorial.

## Acknowledgement and further resources

I started to learn Logstash thanks to [baddila](https://github.com/badilla).

* [Logstash on Wikitech](https://wikitech.wikimedia.org/wiki/Logstash). It
    documents how ELK and Logstash is used by Wikipedia.

[^1]: *ingest* means to absorb, take food or drink by swallowing or absorbing it.
[^2]: *stash* means a store or supply of something that is kept hidden or secret.

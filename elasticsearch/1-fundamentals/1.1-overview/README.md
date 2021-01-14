# Elastic Stack Overview

## Once Upon a Time...

In 1999 Doug Cutting started an open-Source project called Apache Lucene. Lucene is a Java library used for building search within applications. But Lucene cannot be used just by itself. You need to write a Java application that uses Lucene, and it is not designed to be scalable.

This is were Elasticsearch comes in, Elasticsearch is a distributed web service that utilizes JSON based REST APIs to refer to Lucene features.

## The birth of Elasticsearch

Elasticsearch was developed by Shay Banon, started in 2004 as Compass. This was scraped and Elasticsearch was born. It was created with 2 main goalds

* Make it distributed: cluster monitoring, management, etc. basically make it easily scalable.
* Make it easy to use with other languages and not just Java. So it includes RESTful API with JSON.

After its creation it was widely adopted and a company was born.

### Goal 1: Distributed Search

Documents stored in Elasticsearch are distributed across different containers known as shards. This distributions allows Elasticsearch to be very scalable and handle petabytes of data.

### Goal 2: Easily used by other languages

A client app can be written in whatever technology and language you want and to use Elasticsearch all you have to do is make a http request to the Elasticsearch server and you will get a response.

***

## Use cases for the Elastic Stack

* Logging
* Metrics
* Business Analytics
* Security Analytics

>[More use cases can be found here](https://www.elastic.co/customers/)

***

## Elastic Stack

Elastic stack begins in the ingest phase, in this phase you get data in and format it in a way so you get what you want to know.

### **Beats**

Beats are single purpose data shippers that can read your data and send this of to Elasticsearch and/or Logstash.
* **File beats**: give you a lightweight way to forward and centralise logs and files
* **Metric beats**: sends system and service statistics 
* **Packet beats**: is a lightweight network packet analyser

### **Logstash**

This is a server side data processing pipeline. It can ingest from a multitude of sources simultaneously while being able to parse, transform, enrich and prepare your data for ingestion.

### **Elasticsearch**

This is the heart of the stack, this stores, searches and analyses the data passed into it. Elasticsearch stores the data in shards, performs replication and keeps data safe. A node is a single instance of Elasticsearch and a cluster is a collection of nodes.

### **Kibana**

This is used to visualise and manage your data. This is the UI for the Elastic Stack. This presents your data in a meaningful way, this also manages your stack, searches, views, and interacts with your data.

***

# Summary

* Elasticsearch is designed to be scalable and easy-to-use by any programming language
* The Elastic Stack is a collection of products with Elasticsearch at the heart
    * Beats are single-purpose data shippers
    * Logstash is a server-side data processing pipeline
* Kibana is an analytics and visualisation platform
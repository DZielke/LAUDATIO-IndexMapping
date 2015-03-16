LAUDATIO-IndexMapping
===================

Copyright: © 2015, Working Group Electronic Publishing Computer- and Media Service, Humboldt-Universität zu Berlin
  License: Apache Licence 2.0
   Status: Draft
  Version: 1.0
  Authors: Dennis Zielke, Computer- and Media Service, Humboldt-Universität zu Berlin,
           Tino Schernickau Computer- and Media Service, Humboldt-Universität zu Berlin

This project contains the IndexMapping for the SearchIndex in [LAUDATIO-Repository](https://github.com/DZielke/laudatio). The LAUDATIO-Repository is an open source repository for historical corpora. For each corpus in the repository the metadata are TEI-XML. But the SearchIndex in ElasticSearch uses JSON as data format.
We use Java Bridge, a tomcat webapp, to convert the xml files to json, see also: [LAUDATIO-Repository - Technical Documentation](http://www.laudatio-repository.org/repository/technical-documentation/software/elasticsearch.html).

We use the following mapping to map all fields to the string type but the field that are used for range filters and use not analyzed multifields for the facets:

Dutch laws in GitHub
====================

What is this?
-------------

This is a repository that tracks changes of Dutch laws since sometime in 2010. Conceptually, this repository exists somewhere between the [MetaLex Document Server](http://doc.metalex.eu/) and the plain-text of your paper law book.

Why?
----

This project was inspired by similar projects in other locales (e.g., [Utah](https://github.com/divegeek/utahcode); [Germany](http://www.wired.com/2012/08/bundestag/)). It is something of a statement about transparency through usability. In the words of [Utah code's](https://github.com/divegeek/utahcode) GitHub maintainer:

>...  Its purpose is to publish the state legal code in a way that
makes it easy for interested individuals to access both its content
and its changes over time.

>Another purpose for this repository is to explore some ideas around
how to better facilitate the legislative process.  Legislation comes
in the form of bills which are essentially patches to the existing
legal code.  Many different versions of a patch may float around to be
debated, discussed, amended, etc., before a final version is applied
to the "trunk".  The process is extremely similar to how developers
manage software changes, particularly in the open source world.

The second paragraph is a provocation to the legal field, which is a notoriously analogue practice that could benefit a lot from innovations in information technology. For instance, network analysis of references between laws can [produce information that traditionally only exists in the minds of legal scholars](http://dl.acm.org/citation.cfm?id=1165505). If legal metadata were properly interlinked, it would take just a simple SPARQL query to find out, for instance, how different countries implement a certain EU directive. It would be easy to write a service that keeps track of new laws within a certain domain. Finding relevant case law would be a snap. These are things that are currently very hard or impossible to achieve. 

The legal standard [MetaLex](http://www.metalex.eu/) goes a long way as a framework to get laws in the [semantic web](http://en.wikipedia.org/wiki/Semantic_web), but is still very much under-utilized. The European project [OpenLaws.eu](http://www.openlaws.eu/) is a positive development in this respect.

A simple example of what MetaLex allows us to do, here is an example of a SPARQL query that finds all Dutch laws that have been modified in 2013: 

```
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX bwb: <http://doc.metalex.eu/bwb/ontology/>
PREFIX metalex: <http://www.metalex.eu/schema/1.0#>
PREFIX prov: <http://www.w3.org/ns/prov#>
PREFIX dc: <http://purl.org/dc/elements/1.1/>
PREFIX pr: <http://purl.org/ontology/prv/core#>
PREFIX pro: <http://purl.org/hpi/patchr#>

# Find the first 100 expressions that have been generated in 2013
SELECT DISTINCT * {  
  ?sub a metalex:BibliographicExpression.
  ?sub prov:wasGeneratedAtTime ?time.  

  FILTER(?time >= "2013-01-01"^^xsd:date && ?time <= "2013-12-31"^^xsd:date)
} LIMIT 100
```
<center><sup>[(Try it out)](http://doc.metalex.eu/query?contentTypeConstruct=text%2Fturtle&contentTypeSelect=application%2Fsparql-results%2Bxml&endpoint=http%3A%2F%2Fdoc.metalex.eu%3A8000%2Fsparql&outputFormat=table&query=PREFIX+rdf%3A+%3Chttp%3A%2F%2Fwww.w3.org%2F1999%2F02%2F22-rdf-syntax-ns%23%3E%0APREFIX+rdfs%3A+%3Chttp%3A%2F%2Fwww.w3.org%2F2000%2F01%2Frdf-schema%23%3E%0APREFIX+bwb%3A+%3Chttp%3A%2F%2Fdoc.metalex.eu%2Fbwb%2Fontology%2F%3E%0APREFIX+metalex%3A+%3Chttp%3A%2F%2Fwww.metalex.eu%2Fschema%2F1.0%23%3E%0APREFIX+prov%3A+%3Chttp%3A%2F%2Fwww.w3.org%2Fns%2Fprov%23%3E%0APREFIX+dc%3A+%3Chttp%3A%2F%2Fpurl.org%2Fdc%2Felements%2F1.1%2F%3E%0APREFIX+pr%3A+%3Chttp%3A%2F%2Fpurl.org%2Fontology%2Fprv%2Fcore%23%3E%0APREFIX+pro%3A+%3Chttp%3A%2F%2Fpurl.org%2Fhpi%2Fpatchr%23%3E%0A%0A%23+Find+the+first+100+expressions+that+have+been+generated+in+2013%0ASELECT+DISTINCT+*+%7B++%0A++%3Fsub+a+metalex%3ABibliographicExpression.%0A++%3Fsub+prov%3AwasGeneratedAtTime+%3Ftime.++%0A%0A++FILTER(%3Ftime+%3E%3D+%222013-01-01%22%5E%5Exsd%3Adate+%26%26+%3Ftime+%3C%3D+%222013-12-31%22%5E%5Exsd%3Adate)%0A%7D+LIMIT+100%0A&requestMethod=POST&tabTitle=Query)</sup></center> 

If you need more convincing still, watch the following TED talk by Clay Shirky:

[**How the Internet will (one day) transform government** ](https://www.youtube.com/watch?v=CEN4XNth61o)

How do I use this?
------------------

Every law in this repository is tucked away in a folder structure that has been based on the kind of law, its shortest name, and its unique identifier. I have done this because I don't want to dump 30,000+ files in a single folder with opaque filenames, but rather give them a semantically charged path. I have made sure that the names are Windows-safe (e.g., less than 260 characters without illegal characters). Find the path to a certain ID using the daily-generated [`bwbIdList.json`](bwbIdList.json).

Every commit that has a message formatted as `YYYY-MM-DD` is guaranteed to only contain the document changes corresponding to that date. Note that these changes are assumed to be a proxy for legislative changes, but also occur when additional metadata is added to a document (for instance, references are made explicit). Beware.

Every commit that has a message that reads `index` is guaranteed to contain only the update of the [bwbIdList.json](bwbIdList.json) file of that day.

**Note:** When trying to determine at what date a modification has happened, it is best to look at the *commit message*. Ignore the *commit date* in any case. Initial population of this repository happened somewhere in June 2014 and a lot of laws have  existed before that. I have tried to express this reality in the *author date* of a commit, but seeing as git was meant for code and not for law, modifications from before epoch (January 1st 1970) cannot be properly represented using author date. Law modifications from before this time will have an author date of 1970-01-01, but the commit message shows the actual date formatted as YYYY-MM-DD.

An example commit for a law from August 7, 1816:

| Commit date | Author date | Commit message |
| ----------- | ----------- | -------------- |
| 2014-06-17  | 1970-01-01  | 1816-08-07     |

Also note that commits are not guaranteed to be in chronological order. I have tried my best to make a sensible commit flow, but I am dependant on the dates provided from bwbIdList, which does not always provide consistent information and so the dates may not be in order.

Something looks wrong?
------------------------------

I have taken a lot of care to produce valid and pretty Markdown, but it's hard to find all edge cases when even official XML [doesn't validate to its own very complex schema](http://wetten.overheid.nl/xml.php?regelingID=BWBR0001842).

The bulk of the work has been getting whitespaces and tables right. If you notice an error, [open an issue](https://github.com/statengeneraal/wettenbestand-markdown/issues) or tinker around with [the code](https://github.com/statengeneraal/wetten-tools) yourself.

Also remember that laws typically have more complex markup need than Markdown allows for, so check first if Markdown even supports the desired markup. 

How does it work?
-----------------

I have set up a daily script that will keep track of the law as it changes. Find the source code [here](https://github.com/statengeneraal/wetten-tools). 

There are three sources I have used for populating this repository: 

1. The [official API from the Dutch government](https://data.overheid.nl/data/dataset/basis-wetten-bestand), which produces information about laws as they are today.
2. The [MetaLex document server](http://doc.metalex.eu/), which has been tracking Dutch law and converting it to MetaLex since 2010
3. A [CouchDB database](https://couchdb.apache.org/) I have set up to mirror information produced by the government database, and keep track of historical information since May 26 2014. I have made this database because the MetaLex documents have some whitespace issues which are relevant when converting to Markdown.  

I have taken the XML files in these databases and converted them to the simple markup language [Markdown](http://daringfireball.net/projects/markdown/). A considerable amount of code determines the order of modifying / deleting documents. If a document is not valid anymore, it is deleted from the repository.

Who are you?
------------

This repository is connected to [Open State](http://openstate.eu/), a Dutch organization that promotes open data and the [Leibniz Center for Law](http://www.leibnizcenter.org/), a research group in the University of Amsterdam which operates at the intersection of artificial intelligence and law.

Inquiries should go to maartenhoedjes@gmail.com.

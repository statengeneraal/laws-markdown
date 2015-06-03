Dutch laws in GitHub
====================

What is this?
-------------

This is a repository that tracks Dutch laws since sometime in 2010. Conceptually, this repository exists somewhere between the [MetaLex Document Server](http://doc.metalex.eu/) and the plain-text of your paper law book. The documents have been converted to Markdown to be human-legible and to provide easy-to-read diffs.

**NOTE:** This is not an official source of law. Use at your own peril.

![Example diff for a law about old people and money](http://s15.postimg.org/4d9rpp9nf/law_diff.png)

*Figure 1.* An example diff for a change in law about old people and money

Why?
----

This project was inspired by similar projects in other locales (e.g., [Utah](https://github.com/divegeek/utahcode); [Germany](http://www.wired.com/2012/08/bundestag/)). It is something of a statement about transparency. In the words of [Utah code's](https://github.com/divegeek/utahcode) GitHub maintainer:

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

The second paragraph is a provocation to the legal field, which is a notoriously analogue practice and could benefit a lot from innovations in information technology. As an example, network analysis of references between laws can [produce information that traditionally only exists in the minds of legal scholars](http://dl.acm.org/citation.cfm?id=1165505). If legal metadata were properly interlinked, it would take just a simple SPARQL query to find out, for instance, how different countries implement a certain EU directive. It would be easy to write a service that keeps track of new laws within a certain domain. Finding relevant (case) law would be a snap. These are things that are currently very hard or impossible to achieve automatically. 

Legal standards such as [Akoma Ntoso](http://www.akomantoso.org/) and [MetaLex](http://www.metalex.eu/) go a long way as a framework to get laws in the [semantic web](http://en.wikipedia.org/wiki/Semantic_web), but governments still rely too much on opaque homegrown solutions. European projects such as [OpenLaws.eu](http://www.openlaws.eu/) and [EUCases](http://www.eucases.eu/start/) are positive developments in this respect.

If you need more convincing, watch the following TED talk by Clay Shirky:

<center>
[**How the Internet will (one day) transform government**](http://www.youtube.com/watch?feature=player_embedded&v=CEN4XNth61o)<br /><a href="http://www.youtube.com/watch?feature=player_embedded&v=CEN4XNth61o
" target="_blank"><img src="https://img.youtube.com/vi/CEN4XNth61o/0.jpg" 
alt="Clay Shirky: How the Internet will (one day) transform government" width="240" height="180" border="10" /></a>
</center>

*Figure 2.* A video about why this project is worthwhile

How do I use this?
------------------

Every law in this repository is tucked away in a folder structure that has been based on the kind of law, its shortest name, and its unique identifier. I have done this because I don't want to dump 30,000+ files in a single folder with opaque filenames, but rather give them a semantically charged path. I have made sure that the names are Windows-safe (e.g., less than 260 characters without illegal characters). Find the path to a certain BWB ID using the daily-generated [`index.json`](index.json), which contains metadata on the laws in the repository.

Every commit that has a message formatted as `YYYY-MM-DD` is guaranteed to only contain the document changes corresponding to that date. Note that these dates are based on the 'date last modified' field provided by the  government CRM. They are assumed to be a proxy for legislative changes, but do not necessarily correspond to official legislative modifications (for instance, fixing a typo), or to the date on which a change is actually *in effect*. Beware.

Every commit that has a message that reads `index YYYY-MM-DD` is guaranteed to contain only the update of the [index.json](index.json) file of that day.

**Note:** When trying to determine at what date a modification has happened, it is best to look at the *commit message*. Ignore the *commit date* in any case. Initial population of this repository happened somewhere in June 2014 and a lot of laws have  existed before that. I have tried to express this reality in the *author date* of a commit, but seeing as git was meant for code and not for law, modifications from before epoch (January 1st 1970) cannot be properly represented using author date. Law modifications from before this time will have an author date of 1970-01-01, but the commit message shows the actual date formatted as YYYY-MM-DD.

An example commit for a law from August 7, 1816:

| Commit date | Author date | Commit message |
| ----------- | ----------- | -------------- |
| 2014-06-17  | 1970-01-01  | 1816-08-07     |

Also note that commits are not guaranteed to be in chronological order. I have tried my best to make a sensible commit flow, but I am dependant on the dates provided from bwbIdList. A previously overlooked old law may be added, for instance.

Something looks wrong?
------------------------------

I have taken a lot of care to produce valid and pretty Markdown, but it's hard to find all edge cases when even official XML [doesn't validate to its own very complex schema](http://wetten.overheid.nl/xml.php?regelingID=BWBR0001842).

The bulk of the work has been getting whitespaces and tables right. If you notice an error, [open an issue](https://github.com/statengeneraal/wettenbestand-markdown/issues) or tinker around with [the code](https://github.com/statengeneraal/tools-github-bwb) yourself.

Also remember that laws typically have more complex markup needs than Markdown allows for, so check first if Markdown even supports the desired markup. 

How does it work?
-----------------

I have set up a daily script that will keep track of the law as it changes. Find the source code [here](https://github.com/statengeneraal/tools-scripts/tree/master/scripts). 

There are three sources I have used for populating this repository: 

1. The [official API from the Dutch government](https://data.overheid.nl/data/dataset/basis-wetten-bestand), which produces information about laws as they are today.
2. The [MetaLex document server](http://doc.metalex.eu/), which has been tracking Dutch law and converting it to MetaLex since 2010
3. A [CouchDB database](https://couchdb.apache.org/) I have set up to mirror information produced by the government database, and keep track of historical information since May 26 2014. I have made this database because the MetaLex document server has some bugs. Source code for the service is [here](https://github.com/statengeneraal/tools-scripts).  

I have taken the XML files in these databases and converted them to the simple markup language [Markdown](http://daringfireball.net/projects/markdown/). A considerable amount of code determines the order of modifying / deleting documents. If a document is not valid anymore, it is deleted from the repository.


Contact
------------
Inquiries go to m.f.a.trompper@uva.nl.

This repository is maintained by the [Leibniz Center for Law](http://www.leibnizcenter.org/), a research group of the University of Amsterdam which operates at the intersection of artificial intelligence and law. It is also connected to [Open State](http://openstate.eu/), an organization that promotes open data. 

This project was part of an internship at Leibniz Center for Law. Read more about my work at Leibniz here [here](http://leibniz-internship-report.herokuapp.com/).

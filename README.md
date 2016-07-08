# Implementing Canonical Text Services in the Croatiae Auctores Latini Digital Collection

[Neven Jovanović](http://orcid.org/0000-0002-9119-399X), University of Zagreb

Alexander Simrell, College of the Holy Cross

## Description

A set of 216 CroALa TEI XML documents which can be imported into a [CTS/CITE Vagrant virtual machine](https://github.com/Leipzig-Furman-Plutarch/virtualMachine2016).

## License

Creative Commons [Attribution 4.0 International](LICENSE.md).

## How to use

* Copy the XML directory, the [inventory.xml](inventory.xml) and [citationconfig.xml](citationconfig.xml) files into the cts-corpus-template of the CTS/CITE Vagrant virtual machine repository (cloned on your local machine).
* Start the virtual machine with `vagrant up`.
* SSH to the virtual machine with `vagrant ssh`.
* Go to the /vagrant/scripts directory.
* Run scripts `8_Build_Template_Data.sh`, `9_Load_Template_Data_into_DB.sh`, `6_Run_SparqlCTS.sh`.
* Navigate to `http://localhost:9000/sparqlcts` (in the basic setup) and explore.

Sample URNs which you can check out:

`urn:cts:croala:kruzic-p.epist-1525-10-05b:head-p`

`urn:cts:croala:kruzic-p.epist-1525-10-05b:`

## About the project

The [Canonical Text Services (CTS) protocol](http://cite-architecture.github.io/), developed by Christopher Blackwell and Neel Smith, offers the scholarly community a way to use URNs for referring to two categories of "a text" and its parts: to their specific realizations ("manifestations" in FRBR), and to its ideal representation ("work"). CTS has the potential to transform scholarly practices, by easing the migration of our interpretations and knowledge from print to digital, by forcing us to reconsider what exactly we are doing when we refer or cite, and, eventually, by integrating into our referring and citing machine-driven comparisons across multiple versions of texts.

### CTS implementations

The CTS protocol is currently implemented in two projects: the [Homer Multitext](http://www.homermultitext.org/) and the [Perseus Digital Library](http://www.perseus.tufts.edu/hopper/). Both focus on texts which have been considered classical - texts of Greek and Roman antiquity - and have well-established citation schemes, in some cases going back thousands of years. We put the CTS protocol to test by applying it to a non-canonical collection - to Latin texts in the collection [Croatiae auctores Latini (CroALa)](http://croala.ffzg.unizg.hr/intro/).

### Croatiae auctores Latini

In Croatia there was a rich tradition of writing in Latin during the Medieval and Early Modern period (texts in CroALa date from 976 to 1984). The corpus happens to include a number of complete or partial translations of Homeric poems into Latin, such as the partial one by Janus Pannonius (1447), and the complete one by Rajmund Kunić (1776). We applied the CTS protocol and its supporting technologies to connect  these translations to the "ideal" CTS representation of the Iliad. Through this canonical reference a connection was established to the Greek language sources served on the internet by the Homer Multitext project.

### Workflow

The process involved three stages: 
* making the CroALa texts “canonically" referable through XML catalog records
* validating and verifying the prepared editions
* establishing the connection between editions prepared by different projects


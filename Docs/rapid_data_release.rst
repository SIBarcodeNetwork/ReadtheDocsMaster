.. _rapid_data_release-link:

Rapid Data Release Policy
=========================

Since its inception in FY2011, the SI Barcode Network has expected PIs to release barcode data records on GenBank as soon as possible after sequences have undergone data quality validation.  This expectation has been stated in various ways in Announcements of Opportunities and the Terms of Participation to which PIs agree prior to receipt of support.  Examples are:

	* *Public data release will be expected within 12 months of sequencing under normal circumstances;* 
	* *Finished records on BOLD will be released to GenBank as soon as they comply with the Barcode Data Standard and have gone through quality control to the PI’s satisfaction; and*
	* *Recipients of SI Barcode Network support in previous years are required to provide a one-page appendix that describes the creation, verification and public release of barcode data as the primary deliverables.*

This program policy on rapid data release is based on a number of considerations:

	* Rapid data release will increase the visibility and discoverability of SI-generated data and voucher specimens in SI units.  This will serve SI’s access mission and increase the Institution’s research impact;
	* PIs have several options for publishing small ‘data release’ papers at the time they make their data public (see Wellcome Trust Fort Lauderdale meeting, below).  These papers allow PIs to state their intent to publish follow-up papers based on their datasets, in essence asking others not to use their data for the stated intent;
	* PIs who release their results sooner will be viewed as more productive which will increase the success of their funding proposals;
	* There is a pervasive trend toward data sharing and openness, especially when the data result from federal research support.  This trend has been accelerated by a 2013 Executive Order([#]_) and a 2013 OSTP Policy Memorandum([#]_); and
	* Genomic projects like the Human Genome grappled with the tension between the benefits to the community of rapid data release and the perceived costs to the data providers.  The Wellcome Trust proposed a solution([#]_) that the community has followed with success;

Here are some of the concerns that are commonly associated with rapid release of DNA barcode sequence records on GenBank:

I haven’t had time to confirm the species identification on all the voucher specimens.  I need to visit a few more museums to check some types before I’m comfortable releasing GenBank records with these species names.
	The Barcode Data Standard requires either a formal or provisional species name.  PIs can release data with names like *Genus X aff. species y* or *X cf y* or *X sp. USNM12345* (as a provisional place-holder name).  A PI can update these records with formal names when the identifications have been confirmed.

I’m concerned that someone can use my data to publish a paper before I have time to do it.  I’d rather wait to release the data until the paper is published.
	This concern would definitely be justified for a dataset with multiple markers or a whole mitochondrial genome that are used for most phylogenies (especially deep phylogenies) and phylogeographic analyses, but it’s far less true for just barcode sequences.  There are two ways that a PI can reduce the probability of being ‘scooped’ by another researcher using their data.  First, the researcher can publish a note or short article announcing the rapid data release and describing the follow-up research paper(s) that he or she plans to publish based on the data.  The note or paper could say that researchers are welcome to use the dataset for other purposes (as described in the Fort Lauderdale principles, referenced above).  Each barcode record in the dataset would reference this publication so anyone finding a record in the dataset through a BLAST search would see the request not to publish on certain topics.  Second, the dataset could be released without a formal species name. The GenBank records can be updated with formal species names when the PI publishes his or her research paper based on the dataset.

What’s the value of releasing barcode records without the final species name?  Won’t that look like second-rate research? 
	There’s value in having barcode records in the public domain even in this interim form.  First, other PIs will find them in the results of their BLAST search and will discover that it’s part of a larger USNM dataset.  They may contact the PI to ask for additional information or permission to see and use the additional data, or they may be able to provide information that’s useful to the PI.  If the PI chooses to publish a brief project description([#]_), it can describe the PI’s plans to finish the dataset and release it when an in-progress paper is published.  This publication would be part of every barcode record in the dataset so anyone finding a record in a BLAST search would see the reference.

I see the value of rapid data release and I’d like to comply, but it’s extra work to put provisional names on records and then have to update them later.  I don’t know how long it will take to get the identifications done properly.  I don’t want it to look like I’m releasing sloppy, unreliable results. Is there an easier way to release the preliminary IDs but let people know that there may be errors?  
	Absolutely.  CBOL has recognized that users have no way of knowing how reliable the taxonomic identifications are in BOLD records and barcode records in GenBank.  For this reason, CBOL has developed additional metadata fields that convey information about how the identification was done, who identified the voucher specimen and when, and what level of confidence they have in their identification.  These metadata elements would appear as structured comments in the barcode records.  They are not yet part of the Barcode Data Standard but CBOL is putting them on all records generated by its project on endangered species.  More information about these metadata fields can be obtained from schindeld@si.edu.

.. rubric:: Footnotes

.. [#] See Executive Order -- `Making Open and Machine Readable the New Default for Government Information <https://www.whitehouse.gov/the-press-office/2013/05/09/executive-order-making-open-and-machine-readable-new-default-government->`_ and associated `Open Data Highlights document <https://www.whitehouse.gov/sites/default/files/microsites/ostp/2013opendata.pdf>`_
.. [#] OSTP Policy Memorandum, February 22, 2013, on `Increasing Access to the Results of Federally Funded Scientific Research <https://www.whitehouse.gov/sites/default/files/microsites/ostp/ostp_public_access_memo_2013.pdf>`_
.. [#] Report of Wellcome Trust Fort Lauderdale meeting, January 2003, on `Sharing Data from Large-scale Biological Research Projects: A System of Tripartite Responsibility <https://www.genome.gov/pages/research/wellcomereport0303.pdf>`_
.. [#] The Wellcome Trust Principles on data release suggest that publication of ‘project descriptions’ is a way to ask the community to respect the PI’s plans to publish specific studies based on datasets that are being made public by him or her.  See example for `birds <http://zookeys.pensoft.net/articles.php?id=1953>`_ and `insects <http://www.bioone.org/doi/pdf/10.4289/0013-8797.116.1.137>`_.

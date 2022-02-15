+--------------------+----------------------+------------------------------------+
| Part of sequence   | Type of Annotation   | Annotation Properties              |
|                    |                      | (Name: Value)                      |
+====================+======================+====================================+
| psbA	             | Gene                 | gene: psbA                         |
+--------------------+----------------------+------------------------------------+
| psbA               | CDS                  | gene: psbA                         |
+                    +                      +                                    +
|                    |                      | product: photosystem II protein D1 |
+                    +                      +                                    +
|                    |                      | codon_start: 3                     |
+                    +                      +                                    +
|                    |                      | transl_table: 11                   |
+--------------------+----------------------+------------------------------------+
| psba-trnH spacer   | Misc Feature         | note: psbA-trnH intergenic spacer  |
+--------------------+----------------------+------------------------------------+
| trnH               | Gene                 | gene: trnH                         |
+--------------------+----------------------+------------------------------------+
| trnH               | tRNA                 | gene: trnH                         |
+                    +                      +                                    +
|                    |                      | product: tRNA-His                  |
+--------------------+----------------------+------------------------------------+

+--------------------+----------------------+-----------------------------------------+
| Part of sequence   | Type of Annotation   | Annotation Properties                   |
|                    |                      | (Name: Value)                           |
+====================+======================+=========================================+
| entire sequence    | Gene                 | gene: ABBREVIATION OF GENE (ex: matK)   |
+                    +                      +                                         +
|                    |                      | note: FULL NAME OF GENE (ex: maturase K)|
+                    +                      +                                         +
|                    |                      | pseudo  (no value for this property)    |
+--------------------+----------------------+-----------------------------------------+

+--------------------+----------------------+-----------------------------------------+
| Part of sequence   | Type of Annotation   | Annotation Properties                   |
|                    |                      | (Name: Value)                           |
+====================+======================+=========================================+
| entire sequence    | Gene                 | gene: ABBRIVIATION OF GENE (ex: matK)   |
+                    +                      +                                         +
|                    |                      | note: FULL NAME OF GENE (ex: maturase K)|
+                    +                      +                                         +
|                    |                      | pseudogene: unknown                     |
+--------------------+----------------------+-----------------------------------------+


+-----------------------------------+------------------------+
| Field in Geneious Prime           | Genbank modifier field |
+===================================+========================+
| voucherCatalogueNumber*           | Sequence_ID**          |
+-----------------------------------+------------------------+
| scientificName                    | Organism               |
+-----------------------------------+------------------------+
| collectorList                     | Collected_by           |
+-----------------------------------+------------------------+
| identifiedBy                      | Identified_by          |
+-----------------------------------+------------------------+
| genbankCountry                    | Country                |
+-----------------------------------+------------------------+
| genbankDate                       | Collection_date        |
+-----------------------------------+------------------------+
| genbankLatLng                     | Lat_Lon                |
+-----------------------------------+------------------------+
| Sequencing Primer:                |                        |
| Forward Sequencing Primer Name    | Fwd_primer_name        |
+-----------------------------------+------------------------+
| Sequencing Primer:                |                        |
| Forward Sequencing Primer Sequence| Fwd_primer_seq         |
+-----------------------------------+------------------------+
| Sequencing Primer:                |                        |
| Reverse Sequencing Primer Name    | Rev_primer_name        |
+-----------------------------------+------------------------+
| Sequencing Primer:                |                        |
| Reverse Sequencing Primer Sequence| Rev_primer_seq         |
+-----------------------------------+------------------------+

\* voucherCatalogueNumber or value used to name sequences in FASTA file

** Specimen_ID will translate to Specimen_voucher or isolate, depending on what was chosen in the previous tab of the portal

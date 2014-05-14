Global dissemination of a multidrug resistant Escherichia coli clone
====================================================================

This repository provides sequence data for our phylogenomic study of E. coli
ST131 in an easily accessible format. If you use this data in your 
publications please cite::

    PETTY NK*, BEN ZAKOUR NL*, STANTON-COOK M, SKIPPINGTON E, TOTSIKA M, FORDE BM,
    PHAN MD, MORIEL D, PETERS KM, DAVIES MR, ROGERS BA, DOUGAN G, RODRIGUEZ-BAÑO J,
    PASCUAL A, PITOUT JDD, UPTON M, PATERSON DL, WALSH TR, SCHEMBRI MA^, BEATSON
    SA^. Global dissemination of a multidrug resistant Escherichia coli clone. 
    Proc Natl Acad Sci USA (in press). 
    
    ^CORRESPONDING AUTHORS *AUTHORS CONTRIBUTED EQUALLY


The Illumina sequencing reads are available under the ENA accessions 
`PRJEB2968`_ (95 paired reads) and `PRJEB5004`_ (4 paired reads).


Mapping the ENA accession to Strain identifier
----------------------------------------------

The following table facilitates this:

======= =========
Strain  Accession
======= =========
HVM2757 ERR161327
HVM1181 ERR161319
P112EC  ERR161312
HVM2049 ERR161324
S2EC    ERR161235
S26EC   ERR161245
S37EC   ERR161302
S31EC   ERR161300
S5EC    ERR161236
S94EC   ERR161257
S120EC  ERR161283
S34EC   ERR161247
S79EC   ERR161305
S128EC  ERR161291
S104EC  ERR161267
S105EC  ERR161268
S21EC   ERR161242
S22EC   ERR161243
HVM1147 ERR161318
S24EC   ERR161244
S6EC    ERR161299
S114EC  ERR161277
S32EC   ERR161301
S19EC   ERR161241
HVM277  ERR161315
HVM52   ERR161308
HVM2044 ERR161323
HVM2289 ERR161325
S77EC   ERR161304
S115EC  ERR161278
S103EC  ERR161266
S65EC   ERR161303
IR18E   ERR458470
S119EC  ERR161282
S118EC  ERR161281
HVM1299 ERR161320
HVM3017 ERR161328
S122EC  ERR161285
MS2481  ERR161252
S98EC   ERR161261
S97EC   ERR161260
S99EC   ERR161262
S125EC  ERR161288
S111EC  ERR161274
S109EC  ERR161272
S121EC  ERR161284
S131EC  ERR161294
S15EC   ERR161240
S123EC  ERR161286
S126EC  ERR161289
S132EC  ERR161295
S130EC  ERR161293
S96EC   ERR161259
S113EC  ERR161276
S101EC  ERR161264
S47EC   ERR161250
S30EC   ERR161246
S43EC   ERR161249
B36EC   ERR161254
S127EC  ERR161290
S53EC   ERR161251
S134EC  ERR161297
S39EC   ERR161248
S10EC   ERR161237
S12EC   ERR161239
HVM834  ERR161317
HVM1997 ERR161322
HVM1619 ERR161321
S133EC  ERR161296
S124EC  ERR161287
S129EC  ERR161292
IR68    ERR458473
IR65    ERR458472
IR49    ERR458471
S93EC   ERR161256
S1EC    ERR161234
S11EC   ERR161238
P189EC  ERR161314
S92EC   ERR161255
S117EC  ERR161280
S116EC  ERR161279
P146EC  ERR161313
S95EC   ERR161258
P56EC   ERR161310
HVR2496 ERR161326
HVM5    ERR161306
HVM3189 ERR161329
P50EC   ERR161307
HVR83   ERR161311
S100EC  ERR161263
S110EC  ERR161273
S102EC  ERR161265
S112EC  ERR161275
MS2493  ERR161253
HVM826  ERR161316
P53EC   ERR161309
S135EC  ERR161298
S107EC  ERR161270
S108EC  ERR161271
======= =========


Getting the data
----------------

**Warning:** The data is ~1GB.

**Option 1) Download the current release as an archive:**

With wget::

    $ wget https://github.com/BeatsonLab-MicrobialGenomics/ST131_99/archive/1.0.tar.gz -O ST131_99-1.0.tar.gz


**Option 2) Clone the current master branch in this repository:**

Please ensure you have `git`_ installed. git can be really useful for 
scientists. See `here`_ for some discussion.

With git::

    $ git clone --recursive https://github.com/BeatsonLab-MicrobialGenomics/ST131_99.git
    # The --recursive option is used to pull down all the smaller repositories


**Programmatic Access**:

If you're only interested in a subset of strains you should be able to write 
a curl or/wget call.

The files have the following patterns:
    * draft assemblies- https://github.com/BeatsonLab-MicrobialGenomics/ST131_99/blob/master/assemblies/$STRAINID_*_Contigs.fasta
    * ordered assemblies against complete EC958- https://github.com/BeatsonLab-MicrobialGenomics/ST131_99/blob/master/ordered/$STRAINID_*_Contigs-against-EC958.fas

VFDB
----

We updated VFDB in May 2014 to include the fimH, parC and gyrA alleles used in the 
study. Please see: https://github.com/BeatsonLab-MicrobialGenomics/VFDB/tree/master/fimH_parC_gyrA 

These are the sequences along with the draft genomes that were used as inputs 
to `SeqFindR`_ to generate the presence/absence plots (Figure 3, Figure S4, and
Figure S6). See the `VFDB repository`_ for more information.  



Manifest
--------

Contains:
    * VFDB/ - Virulence factor & Islands sequences. SeqFindR formatted. 
    * assemblies/ - the assembled contigs from `Velvet`_.
    * ordered/ - the assembled sequences ordered against EC958. The complete 
      EC958 genome can be `downloaded from here`_.

The assembly statistics are `provided`_. The draft assemblies were ordered 
with The `Mauve Contig Mover (MCM)`_.


About
-----

The 99 ST131 genomes were analysed using the `Banzai Microbial Genomics 
Pipeline`_. We also used the `EasyFig`_, `SeqFindR`_ and `BRIG`_ tools
developed within the Beatson Lab.

.. _`VFDB repository`: https://github.com/BeatsonLab-MicrobialGenomics/VFDB
.. _PRJEB2968: http://www.ebi.ac.uk/ena/data/view/PRJEB2968
.. _PRJEB5004: http://www.ebi.ac.uk/ena/data/view/PRJEB5004
.. _provided: https://github.com/BeatsonLab-MicrobialGenomics/ST131_99/blob/master/assembly_stats.rst
.. _git: http://git-scm.com/
.. _here: http://blogs.biomedcentral.com/bmcblog/2013/02/28/version-control-for-scientific-research/
.. _Velvet: https://github.com/dzerbino/velvet
.. _`downloaded from here`: http://beatsonlab.com/pages/data.html
.. _`Banzai Microbial Genomics Pipeline`: https://github.com/mscook/Banzai-MicrobialGenomics-Pipeline
.. _EasyFig: http://easyfig.sourceforge.net
.. _SeqFindR: https://github.com/BeatsonLab-MicrobialGenomics/SeqFindR
.. _BRIG: http://sourceforge.net/projects/brig/
.. _`Mauve Contig Mover (MCM)`: http://asap.ahabs.wisc.edu/mauve-aligner/mauve-user-guide/reording-contigs-in-draft-genomes.html

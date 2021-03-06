.. _biometadata:

.. image:: /_static/biometadata_schema.png
   :scale: 50 %
   :align: right

.. _biometadata_biosample:

****************************
BioMetadata: *BioSample* Object
****************************

BioSample in the GA4GH Schema
------------------------------

The majority of use cases of GA4GH
schema compatible resources will serve to facilitate the retrieval of *molecular
features* (DNA sequence variations, gene expression, protein variants) measured
by performing *experimental* (whole genome sequencing, expression arrays, mass
spectroscopy) in conjunction with *bioinformatics* procedures, applied to a
preparation of target molecules (e.g. DNA, RNA) which has been extracted from a
*biological sample* (e.g. tissue biopsy, single cell from FACS,
environmental sample).

In the GA4GH schema, a *BioSample* represents the main "biological
item" against which molecular variants are referenced.

BioSample attributes
====================

===================== ==========================================================
Attribute             Notes
===================== ==========================================================
*id*                  * the BioSample's id
                      * unique in the context of the server
                      * used for referencing this BioSample
*name*                * a human readable object label/identifier
                      * not to be used for referencing
*description*         * additional, unstructured information about this BioSample
*disease*             * OntologyTerm annotating the disease of the sample
*individualId*        * the *id* of the *Individual* this BioSample was derived from
*created*             * the time the record was created, in ISO8601
*updated*             * the time the record was updated, in ISO8601
*info*                * additional, structured information
===================== ==========================================================

.. _biometadata_Individual:

*****************************
BioMetadata: *Individual* Object
*****************************

Individual in the GA4GH Schema
------------------------------

An *Individual* is a GA4GH data object representing a biological instance
(most commonly a human being or other individual organism) on whose *BioSamples*
experimental analyses are performed.

Individual attributes
=====================

===================== ==========================================================
Attribute             Notes
===================== ==========================================================
*id*                  * the Individual's id
                      * unique in the context of the server
                      * used for referencing this Individual
*name*                * a human readable object label/identifier
                      * not to be used for referencing
*description*         * additional, unstructured information about this Individual
*species*             * OntologyTerm representing the species (NCBITaxon:9606)
*sex*                 * OntologyTerm for the genetic sex of this individual.
*created*             * the time the record was created, in ISO8601
*updated*             * the time the record was updated, in ISO8601
*info*                * additional, structured information
===================== ==========================================================

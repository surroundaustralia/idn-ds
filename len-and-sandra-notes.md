# Len and Sandra's rough notes - for input to Nick/Surround

Rough thoughts here. To be discussed with Nick and Sam and added to appropriate area in this data standard.

Focus here is technical.

## Some thoughts on sustainability and core tasks

See these very rough notes https://rdxx.org/idn/sustainability.txt 
Would be good to go through this quickly with Nick to extract various requirements (and/or should we add this doc as a source?).

## Exemplars and Case studies

### List prepared by Len for Vanessa 2021-10-25, with Sandra's comments.

Sandra's notes incorporated in this very rough summary Len prepared for Vanessa of the datasets which have been identified so far, including databases maintained by others to which we would want to link. 

Note that this task sometimes involves full-spectrum archiving, ie linking to indexes of the location of paper records, of digitised images, of legacy digital archives, etc.   
### Data about people
#### The Koori Health Research Database (KHRD) and the Sandra Smith Archive at Museum Victoria. 
KHRD: a case study of what to do to rectify past less than state of the art practice. Sandra has identified the steps required to make this fully maintainable and sustainable. Access to the Sandra Smith archive is still to be negotiated with the Museum. 
#### Diane Barwick Archive at State Library of Victoria: 
needs to be integrated with KHRD. Negotiation required with State Library. 
#### The Victorian Perinatal database. 
I only know the general situation. Jane Freemantle is across it. Negotiation needed with VicHealth. 
#### WA linked data. 
This was nominated by Sandra Eades. Investigation, documentation and negotiation needed.  
#### ATSIDA, the Aboriginal and Torres Strait Islander Data Archive at the Australian Data Archive and ANU Archives. 
This was specifically mentioned in the NCRIS Roadmap as an existing strength to be built on. It needs staff at the Data Archive to fully curate and digitise these collections and make them web-accessible. It includes:
- Historical Colonial, State and Commonwealth censuses
- The inter-war Aboriginal censuses.
Len and Gordon's police districts dataset. Catalogued in ATSIDA@ADA: https://www.atsida.edu.au/archive/datasets/au.edu.anu.ada.ddi.20002-nsw
- The Northern Territory Aboriginal Population Record (APR)
- Historical population data
#### ATSIDA at UTS Sydney
An exisiting node of ADA... what is it's status? NSW Library/Jumbunna plans for this? Partners? ADA role?
It looks like a Drupal installation? Is it up to date or not? Len's response: they use Murkurtu, which uses an old version of Drupal. Kirsten Thorpe believes Mukurtu is being updated.  
- Aboriginal Deaths and Injuries in Custody. 
ATSIDA@UTS has taken over this data, but needs help to turn it into an ongoing public database
#### The Fred Hollows Archive (National Trachoma and Eye Health Program) 
This comprises records of about 70,000 Indigenous and 30,000 non-Indigenous people surveyed in the 1970s and 1980s. Some paper records are held at AIATSIS. Microfilms of others are at UNSW Archives. There have been preliminary discussions with AIATSIS, the National Library and former members of the Hollows team about a program to digitise the records. IDN staff/resources would be needed. 
#### Tasmanian Aboriginal genealogies: 
these are extensive paper records which Ian Anderson has proposed incorporating in a database. Negotiation is still needed. 
#### People Australia. 
Existing database at the National Library.
#### Australian Dictionary of Biography. 
Existing database at ANU.
#### National, State/Territory and University Archives. 
Need to review and link to Catalogues
#### War Memorial. 
Ditto
#### National, State/Territory and University Museums. 
Ditto
#### Population, health and social data 
including censuses and surveys.
#### Public finance and the Indigenous economy. 
Economic data was identified as a missing component in the Closing the Gap refresh. Databases include
- GDP and Genuine Progress Indicator (Torrens University). 
An earlier application with Marcia for AIATSIS funding was never considered.
- Expenditure on Indigenous advancement. 
Yothu Yindi Foundation has done extensive work on where the money goes in the NT. Needs to be a national database.
### Data about place. 
#### An Indigenous geography and gazetteer, including a Loc-I framework for tribal, language and community data. 
Requires developmental work in collaboration with Universities, ABS, AIHW, Geoscience Australia, AURIN etc etc. 
#### the ATNS Negotiated Settlements Database.
Marcia's native title database and/or public native title data:
 - what is the relationship of Marcia's work to publicly available native title data??? 
 - see Sandra's work converting the NTD shape files to XML database (also aiatsis placenames matched to composite gazette ~78% ); 
 - next step geosparql 1.1 plus vocabularise native title determination (long term Daghstul vocab governance issues); 
 - can use this to quickly generate demos or ETL as guided by Surround and user requirements
Needs to be made fully maintainable, sustainable and web-accessible? 
#### Native Title databases at NNTT. 
Marcia will need to negotiate this.
#### AIATSIS Placenames Thesaurus. 
Need Craig to agree to its use
#### AIATSIS Subject Thesaurus. 
Ditto
#### Compound Gazetteer of Australia at Geoscience Australia
#### Tindale/Horton map. 
Strong demand but controversial.
#### Dual placenames. 
Need to work with GA and Commonwealth-State placenames committee.
#### Austlang database. 
Need to have access to boundaries.

### Other orphan datasets and databases

 - various datasets Sam says people at ANU are wanting to give him; need details.
 
## Requirements for user and organisation catalogue using case studies as examples

IDN membership catalog contents:
 - use ROR for organisations?
 - use ORCID for individuals? (Ldaca/ARDC compute platform Authz/Authn should be able to easily support this)

Leverage data stored in ORCID - perhaps a "profile" to check ORCID data and direct users to fill in gaps.

Need additional encoding of the following (with aim of vocabularising these and publishing in RVA):
 - user/org "point of view", 
 - interests,
 - subjects (top level of aiatsis subjects - can easily skosify if aiatsis give permission),
 - preferred methods, skills, tools, approaches
 - available technologies used to generate data e.g. excel, fmpro, csv, drupal -- surely an existing vocab of software tools?
 - geospatial focus and mandate 
 - temporal focus
 
Purpose of this "point of view" encoding is to provide the required data infrastructure to support networking, communities of practice, alerts of new deposits of interest.

## Requirements for data catalogue using case studies as examples

Additional functional requirements compared to current ATSIDA content description (ATSIDA appears to be inactive? Nothing since 2018?).

Using Len's census work as an example:
 - expose the machine readability of backend (ie. ddi/dcat-2/dcat-3), enable export of various serialisations (csv, json-ld, xml, rdf).
 - allocate PIDS for everything where it makes sense to be able to address and locate that thing;
   - governance;
   - persistence;
   - domain (.gov.au probably not appropriate for trust; available: airdcat.net.au - aust indigenous research data catalog)
 - IDN "ontology" of "things" of interest to DATA MANAGEMENT LIFECYCLE (this should be actionable in producing the catalog's UI for humans) e.g.
   - data owners, data custodians, data collections, datasets, subjects, places 
   - leverage AUSTLANG (see Sandra's work converting this to XML and matching to unofficial Tindale shape file)
 - explicitly add licensing;
 - provide sufficient information about the collection to enable a user to determine if its relevant and useful to them (a challenging task as this is quite a complex collection when provenance is considered)
 - provide direct access to the data or machine actionable process by which data can be requested (ldaca RO-Crate) ;
 - add linkage between the States (it's really one study with multiple geospatial extents (States, Police Districts) and multiple temporal extents, and multiple classification systems (differences by State and temporal evolution). Possible candidate for "depth" study;

Explcitly capture and enable human friendly and useful presentations:
 - geospatial scale, extent and frequency
 - temporal scale, extent and frequency 
 - subject matter : Indigenous field of interest (nb: See Sandra's work on AIATSIS subject thesaurus conversion)
 - methodological descriptions (including software, scripts, workflows, aggregators, local browsing tools etc) - PROV-O should be adequate
   
## Thoughts on sources

### Comments on the AI/Indigenous paper added by Sam:

 - opens way to having MR (machine readable) "permissions" to assist elders determining access;
 - Table 2 expresses access protection requirements succinctly;
 - many resonances with 2nd order cybernetics (i.e. including observer as part of observing systems) an important insight;
 - suggest emphasis in our project is not yet about representing Indigenous ontologies (a long term project, should be bottom up) but about using and adapting "at hand" tools with a deliberately narrow focus on a CARE/FAIR enabled research data management lifecycle aiming to:
   - raise Indigenous data capabilities by offering a practical, working data repository and catalog; 
   - offer working examples (case studies) of what is possible for critique and feedback by partners and network members; and
   - enable others to replicate and re-apply case studies in different contexts.

# Executive Summary
The main objective of SP4 is the creation of a Knowledge Graph (KG) that up-to-now provides: 

a. access in one place to Life Cycle Inventory (LCI) data that is commonly distributed across different information sources, causing environmental experts to spend large amounts of time looking for the adequate data to create GHG assessment reports; 

b. translation of GHG assessment reports from one assessment standard into another. 

This is necessary so that reports can be comparable. Currently, comparing reports that follow different standards requires environmental experts recreating a GHG assessment report almost from scratch so that it follows the same assessment standard as the other. The KG hence, will automate several processes that currently require a lot of time, effort and expertise from environmental experts. Towards this KG, in 2023 we have been working on: 


1.	Creating machine readable and machine understandable representations of publicly available LCI databases such as UVEK and PlasticsEurope.
2.	Linking data from the databases to established sources of knowledge to provide more functionalities in dashboard prototypes (SP5, SP6 and SP7), such as ranking data searches according to the geographical accuracy.
3.	Creating machine readable and machine understandable representations of assessment standards (e.g., the GHG protocol and the ISO 14064-1 standard); which up until now are only described on natural language in documents and need to be interpreted by environmental experts.
4.	Utilising open-source toolboxes for computing scope 3 GHG emission factors from various LCI databases that do not directly provide it.


Regarding the creation of the machine-readable representation of databases that are described differently, we have considered three common data formats, namely EcoSpold1, EcoSpold2 and ILCD; which even though, they describe the same type of data, they utilize different nomenclatures and structures. Thus, to allow for easy querying, we have created a layer that uniforms them, which we call the WISER Bridge Ontology.

Furthermore, given that environmental experts need to decide if a specific dataset is valid for the assessment context of the system they analyse, they need to know the dataset’s region of validity. This can be complex and time consuming since different databases express geography in different ways (e.g., CH and Switzerland). To improve the possibility of finding geographically relevant datasets, we created another layer capable of homogenizing geographical data from different databases; and we integrated a well-established ontology called Geonames. Thanks to the linked nature of a KG, we can easily plugin this geographical source of knowledge and, with little effort, get access to finer and coarser grain information regarding location.

The translation of GHG assessment that the WISER KG enables allow reports that has been created in accordance with a specific assessment standard (e.g., GHG protocol) to be expressed in a different standard (e.g., ISO 14064-1) ; which in turn simplifies the comparison of emissions reports from various stakeholders (that made assessments with different standards) within a supply chain or will even enable fair comparison between competitors. To enable this feature, we have collaborated closely with domain experts of SP1 to create a machine-readable and machine-understandable representation of different assessment standards, and to define how they map and relate to each other.

Furthermore, we have worked on automatic tools that can take advantage of open-source toolboxes such as OpenLCA and Brightway to compute scope 3 GHG emission factors (also known as Life Cycle Impact Assessment (LCIA) results) that environmental data sources do not directly provide, so that such emissions factors can be found in the WISER KG.

# EcoSpold02


The ecoSpold2 format replaces the ecoSpold1 format for ecoinvent version 3 released in May 2013. New developments in the field of LCA software demanded a revision of the data format. An ad-hoc expert working group was formed by ecoinvent to guide the revision process and an open hearing has been conducted among users of the ecoSpold format. The result of this hearing and the way the input has been treated can be seen in this public report. The final ecospold2 format is designed to represent all three stages of life cycle assessment: UPR, LCI and LCIA on an xml basis.

Among others, the ecospold2 format adds features such as:

- Properties of exchanges like dry mass, wet mass, carbon content etc.
- Mathematical relations in a new formula language and variable names for exchanges, properties and parameters
- Use of UUIDs for referencing certain fields
- New fields for production volumes

For a comparison between ecospold1 and ecospold2 visit: Changes ecospold1 to ecospold2

Today, ecospold2 is used by most of the software providers that use the ecoinvent database. The open-source python framework Brightway2 supports the import of ecospold2 as well.

Find more information [here](https://ecoinvent.org/the-ecoinvent-database/data-formats/ecospold2/)
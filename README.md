# Google--Ads--Database.
Google is a multinational technology company offering online advertising services through the Google Ads platform. As a data analyst, you have been tasked with developing a comprehensive Relational Database Management System (RDBMS) to support Google Ads operations. The goal is to manage advertisers,campaigns,ads, keywords, and performance metrics.

##Objectives
* Identifying the main entities in the database system.
* Clearly defining the attributes, relationships and constraint that support the business needs.
* Designing an entity relationship diagram that supports the business needs based on the database entities, relatinships and participation constraints.


  
## Main Entities in the table
Entities are tables or real world objects that are meant to store information in the database. They are fundamental component of an Entity Relationship Diagram(ERD).

# Advertiser
This is the table that stores the advertisers' information. The attributes and data types are as follows:<br>
AdvertiserID **INT** PK<br>
AdvertiserName **VARCHAR**<br>
ContactPerson **VARCHAR**<br>
ContactEmail **VARCHAR**<br>

## Campaign
This is the table that stores information from the campaigns. The attributes and data types are as follows:<br>
CampaignID **INT** PK <br>
AdvertiserID **INT** FK <br>
CampaignName **VARCHAR**<br>
StartDate **DATE**<br>

## Advertisement
This is the table that stores information from the advertisement. The attributes and data types are as follows:<br>
AdID **INT** PK <br>
CampaignID **INT** FK <br>
AdTitle **VARCHAR**<br>
TargetURL **VARCHAR**<br>
Impression **SMALLINT**<br>

## Keyword
This is the table that stores information from keyword. The attributes and data types are as follows:<br>
KeywordID **INT** PK <br>
AdID **INT** FK <br>
KeywordText **TEXT**<br>
BidAmount **SMALLINT**<br>
QualityScore **SMALLINT**<br>

## Performance
This is the table that stores information from performance.  The attributes and data types are as follows:<br>
PerformanceID **INT** PK <br>
AdID **INT** FK <br>
Date **DATE**<br>
Clicks **SMALLINT**<br>
Conversions **SMALLINT**<br>

## The Cardinality and Relationship Requirements for the Database
Advertiser- campaign: One advertiser can manage multiple campaigns, but each company belongs to one advertiser. (one-to-many) <br>
Campaign -Ad: One campaign can contain multiple ads, but each adis linked to one campaign. (one-to-many) <br>
Ad - Keyword: An ad can target multiple keywords, but each keyword is associated with one ad. (one-to-many) <br>
Ad - Performance: One ad can generate multiple performance records over time, but each performance record belongs to a specific ad. (one-to-many) <br>

## The Entity Relationship Diagram
The entity relationship diagram shows the collection of object within a database and the relationships between them. It included the entities, schemas, participation, constraints and the relationships between the entities. I modelled this using theERD tools by defining the table and specifying the relationships between the tables using pre-existing columns as foreign keys.

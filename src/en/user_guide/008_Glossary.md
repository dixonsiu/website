# Glossary


##### [A](#anc_a) | [B](#anc_b) | [C](#anc_c) | D | [E](#anc_e) | [F](#anc_f) | G | H | [I](#anc_i) | J | K | L | [M](#anc_m) | [N](#anc_n) | [O](#anc_o) | [P](#anc_p) | Q | [R](#anc_r) | [S](#anc_s) | [T](#anc_t) | [U](#anc_u) | V | [W](#anc_w) | X | Y | Z


## <a name="anc_a"> A</a>
### ACL
<font size=1>[General]</font> An abbreviation of "Access Control List".  
It defines which users are authorized to access and which control instructions are permitted to be used depending on the privileges granted to objects.  
(Example: Read: Read permissions, Write: Edit permissions, Read/Write: Read/Edit permissions)


### Account
<font size=1>[Pesronium]</font> One of the cell control objects. It represents user authentication means in that cell, and can register multiple cells per cell. The basic type (selected by default) is composed of information such as account name and password. It is also possible to correspond to other authentication means such as OpenID Connect by installing a plugin. It may be used to register multiple authentication means in an individual's cell or may be used to authenticate an organization member in an organization's cell.


### Association
<font size=1>[OData]</font> Shows the relationship between two or more EntityTypes (RDB tables). It is defined by a pair of AssociationEnds and $links in between.  
Associations are categorized into "one-to-one", "one-to-many", and "many-to-many". For details, refer to User OData Model.


### AssociationEnd
<font size=1>[OData]</font>The EntityType that is the endpoint that constitutes the Association. The Association consists of a pair of AssociationEnds and $ links between them.


### Authentication
<font size=1>[General]</font> Authentication. For the account authentication of Personium, the method that performs authentication based on the created account name and password to acquire tokens has been adopted.  


## <a name="anc_b"> B</a>
### bar file
<font size=1>[Personium]</font> An abbreviation of "box archive file". This archive file is a compilation of box structure details.  
The hierarchical structure in the folder represents the hierarchical structure of WebDAV collections, and the files stored in WebDAV are retained by storing files at these hierarchical levels.  
For details, refer to [bar File](../apiref/current/301_Bar_File.md).


### Box
<font size=1>[Personium]</font> The area that stores data used for the application. It is also a WebDAV collection. It has a unique name and schema URL. One box is initially retained in a cell (the main box) even before boxes are created, but it cannot be deleted.


### Box installation
<font size=1>[Personium]</font> To create a box using the bar file. For details, refer to the [Box Installation](../apiref/current/302_Box_Installation.md) API.


### Box level ACL
<font size=1>[Personium]</font> The ACL for resources under the box. For details, refer to [Access Control Model](../apiref/current/006_Access_Control.md).


## <a name="anc_c"> C</a>
### Cell
<font size=1>[Personium]</font> Data store for each data subject. PDS (Personal Data Store) is used for personal use. In Personium, it is possible to use the concept of data principals not only for people but also for data and organizations of organizations and objects.  
(Eg My Cell, Your Cell, Cell of a Company, Cell of a Department, Cell of My Car)


### Cell control object
<font size=1>[Personium]</font> The definition structure that defines each function of a cell, including Role, Account, Box, ExtCell, and ExtRole. Refer to Cell Control Object.


### Cell level ACL
<font size=1>[Personium]</font> ACL to Cell excluding Box level access authority. Define the operation of the Cell control object and the access control to the subordinate Box.


### Cell Profile
<font size=1>[Personium]</font> The item that shows the cell name, image, and other cell information within the Personium portal.


### Collection
<font size=1>[WebDAV]</font> Corresponds to the folder / directory in the ordinary file system. Personium can handle special collections called "OData Service Collection" and "Engine Service Collection" in addition to regular collections.


### ComplexType
<font size=1>[OData]</font> The property that has an attribute accompanied by lower attributes. The item name is ComplexTypeProperty.  
(For example, if "Address" is a ComplexType, possible attributes could be Street 1, Street 2, Country, Zip code, Prefecture, City/town/village, etc.)


### ComplexTypeProperty
<font size=1>[OData]</font> The name of lower attributes of a ComplexType. For example, if ComplexType is "Address", possible attributes could be Street 1, Street 2, Country, Zip code, Prefecture, City/town/village, etc.


### CORS
<font size=1>[General]</font> An abbreviation of "Cross-Origin Resource Sharing". JavaScript shall permit XMLHttpRequest for other domains in the Web page. Refer to [CORS Support](../apiref/current/002_CORS_Support.md).  
(For details, refer to [External Site](http://www.w3.org/TR/cors/))


### Cross Domain Access Control
<font size=1>[General]</font> Access control for servers that have different domains. In Personium, the [Cross Domain Access Policy File](../apiref/current/001_Cross_Domain_Policy_File.md) based on XMLHttpRequest Level2 is used for control.


## <a name="anc_e"> E</a>
### Engine Service Collection
<font size=1>[Personium]</font> A special collection for the user to register new logic on the server side. For details, refer to [Engine Service Collection](../apiref/current/379_Engine_Service_Collection_APIs.md).


### Entity
<font size=1>[OData]</font> The recording structure of data, which corresponds to one row of an RDB table. For example, it represents a row of information such as Name, Address, and Sex.


### EntityType
<font size=1>[OData]</font> The definition structure for representing data structure as an Entity Data Model (EDM). EntityTypes represent broader concepts (such as customers and order details)


### ETag
<font size=1>[HTTP]</font> Refers to the Entity Tag. It is possible to send requests depending on the client status using unique identifiers used for Web cache verification.  
This makes use of the cache more effective and secures bandwidth when it is not necessary to return all responses in a situation where contents are not updated.


### Event
<font size=1>[Personium]</font> An instance that occurs inside or outside Personium. For details, refer to [Event Overview](../apiref/current/277_Event_Summary.md).


### EventLog
<font size=1>[Personium]</font> External and internal event occurrence logs. These can be acquired using the [Log Acquisition API](../apiref/current/285_Retrieve_Log_File.md).


### $expand query
<font size=1>[OData]</font> One of the supported OData queries. This query is for acquiring specified relation information simultaneously by addition to a data acquisition request. ([Details](../apiref/current/405_Expand_Query.md))


### External Cell
<font size=1>[Personium]</font> An external cell. It is one of the cell control objects. It is a cell outside a cell. Cells of all units can be handled as external cells. For details, refer to Cell Control Object.


### External Role
<font size=1>[Personium]</font> An external role. It is one of the cell control objects (ExtRole). It represents a user entity to which a specific role has been granted in an external cell that has a specific relationship. For example, it is possible to register "External Role" such as "administrator (Role) of affiliated organization (Cell) " or "consulting doctor (Role) of goods purchase customer (Cell) ", etc., and by linking this with the role, operations such as data disclosure etc. to indirectly related others It is possible to use like to forgive.

## <a name="anc_f"> F</a>
### $filter query
<font size=1>[OData]</font> One of the supported OData queries. This query is for refining data by specifying search conditions. ([Details](../apiref/current/403_Filter_Query.md))


### $format query
<font size=1>[OData]</font> One of the supported OData queries. This query is for specifying the media type in the HTTP response. ([Details](../apiref/current/404_Format_Query.md))


### FQDN
<font size=1>[General]</font> An abbreviation of "Fully Qualified Domain Name".  
This represents the complete domain name that defines a specific computer or host on the Internet (for example, host-name.domain-name.com)


### Full-Text Search Query
<font size=1>[OData]</font> The query for performing a search that compares every word in the entire data included in the EntityType by adding q="Search word" to a request. ([Details](../apiref/current/408_Full_Text_Search_Query.md))

## <a name="anc_i"> I</a>
### Implicit Flow
<font size=1>[OAuth2.0]</font> One of the permitting flows defined in [OAuth2.0](http://tools.ietf.org/pdf/rfc6749.pdf). Clients directly receive access tokens as substitutes for permission codes (resource owner permission results).  
For details, refer to [External Site](http://openid-foundation-japan.github.io/draft-ietf-oauth-v2-draft22.ja.html#grant-implicit).


### $inlinecount query
<font size=1>[OData]</font> One of the supported OData queries. This query is for displaying the count of entities in the collection. ([Details](../apiref/current/407_Inlinecount_Query.md))


## <a name="anc_m"> M</a>
### Main Box
<font size=1>[Personium]</font> The box named "\_\_" (two underscores) created by default during cell creation. Its behavior is similar to that of normal boxes but this box is undeletable.  
It is used not only for application data storage but also for the storage of information (json format) specific to that cell.


### Message
<font size=1>[Personium]</font> The function that sends and receives messages between cells in Personium. It can transmit and receive arbitrary messages of users and issue relationships ($links) between cells. For details, refer to Message Model.


### Multiplicity
<font size=1>[OData]</font> Multiplicity. The related EntityType count when AssociationEnd is created.  
The notation of AssociationEnd multiplicity is one of "1", "0..1" (0 or 1), and "\*" (many) with respect to the relationship between two EntityTypes.


## <a name="anc_n"> N</a>
### NavigationProperty
<font size=1>[OData]</font> The property that represents the navigation from one end to the other end of an association in the Entity Data Model or OData data structure.


## <a name="anc_o"> O</a>
### OData
<font size=1>[OData]</font> An abbreviation of "Open Data Protocol". It is one of the collections (a data set stored in a box). This is the standard data access protocol conforming to HTML and enables CRUD access to data resources.  
For details on OData, click [here](http://www.odata.org/).


### OData Service Collection
<font size=1>[Personium]</font> It is a special WebDAV extension collection for handling arbitrary relational data with OData protocol, and it can be created in arbitrary hierarchy in Box. Under this collection itself is the root of the service of OData and $ metadata itself storing the schema information is also the root of the OData space for setting the schema. Relational data can be handled based on arbitrary schema defined here.


### $orderby query
<font size=1>[OData]</font> One of the supported OData queries. The values are displayed sorted in the order specified by the user. The default is ascending order. ([Details](../apiref/current/400_Orderby_Query.md))


## <a name="anc_p"> P</a>
### Property
<font size=1>[OData]</font> The column head value of each EntityType. For example, if the EntityType is "Customer", possible properties could be "ID", "Name", and "Address".


### Privilege
<font size=1>[Personium]</font> Privileges granted to the roles defined in the cell to access data in the box associated with specific roles.  
Privileges are defined in ACL configuration in Personium. For details, refer to [Access Control Model](../apiref/current/006_Access_Control.md).


## <a name="anc_r"> R</a>
### RBAC
<font size=1>[General]</font> An abbreviation of "role-based access control". It involves defining roles for various accounts and configuring access control based on roles.


### ReceivedMessage
<font size=1>[Personium]</font> A definition body that receives Relation issue requests and messages from specific cells.


### Refresh token
<font size=1>[OAuth2]</font> The token used for reissuing access tokens. The refresh token is valid for 24 hours.


### Refresh token authentication
<font size=1>[Personium]</font> The process that reissues access tokens..


### Relation
<font size=1>[Personium]</font> A cell control object indicating the relationship between itself (own cell) and another person (external cell). By linking the cell control object Relation and Role, it is possible to collectively assign roles to accessers from other cells in a specific relationship. Be aware that it is a model that independently defines unilateral relationships of relationships to others seen by themselves. In principle, Relation registration of own cell and link to external cell can be done without consent of the other party. For example, when expressing a mutual relationship of "parent and child", a Relation object "My child" is registered in the parent cell and associated with a child cell whose parent cell is registered as an external cell In addition to this, it is desirable to register Relation objects having the opposite meaning of "my parents" in the child cells to the parent cell that the child cell registers as an external cell, and link them.


### Relation class URL
<font size=1>[Personium]</font> The URL of a related resource defined as an application. The relation class URL structure is as follows:  
${Schema URL}/\_\_relation/\_\_/${RelationName}


### Relation instance URL
<font size=1>[Personium]</font> The URL of a specific relation with respect to which a request is sent to one or more external cells.  
The relation instance URL structure is as follows:  
${Cell URL}/\__relation/${BoxName}/${RelationName}


### RequireSchemaAuthz
<font size=1>[Personium]</font> The attribute value of an ACL element that defines the request level for box schema privileges.


### resourcetype
<font size=1>[WebDAV]</font> Represents the collection type. ODataCollection/ServiceCollection/DavCollection/file etc.


### Role
<font size=1>[Personium]</font> One of the cell control objects. This represents the "role" defined for all cells. (Examples: administrator, teacher, student)  
As it is possible to specify which accounts (users) can access the cell, the settings that define the account ownership of the cell can be created with different access privileges.


### Role class URL
<font size=1>[Personium]</font> The URL of the role for storage inside the trans-cell token. The role class URL structure is as follows:  
${schema URL}/\_\_role/\_\_/${RoleName}


### Role instance URL
<font size=1>[Personium]</font> The URL that provides the current status of the role registered with a specific cell. It is the same as the role resource URL. The Schema is as follows:  
${Cell URL}/\__role/${BoxName}/${RoleName}


### ROPC
<font size=1>[OAuth2.0]</font> An abbreviation of "Resource Owner Password Credentials". It is one of the permitting processes defined in [OAuth2.0](http://tools.ietf.org/pdf/rfc6749.pdf). For details, refer to [External Site](http://openid-foundation-japan.github.io/draft-ietf-oauth-v2-draft22.ja.html#anchor7). A standard authentication method for obtaining Personium tokens using ID / PW.


## <a name="anc_s"> S</a>
### Schema URL
<font size=1>[Personium]</font> The URL that represents the schema stored in Personium. The definition is Cell URL or URI.


### $select query
<font size=1>[OData]</font> One of the supported OData queries. This query is for specifying and acquiring only a specific property during data acquisition. Multiple properties can also be specified. ([Details](../apiref/current/406_Select_Query.md))


### SentMessage
<font size=1>[Personium]</font> The definition structure that transmits messages for relation setting approval and normal messages for a target cell. For details, refer to Message Model.


### Service Collection
<font size=1>[Personium]</font> One of the collections (a data set stored in a box). This is a collection of services to execute user-defined server-side logic.


### Service registration
<font size=1>[WebDAV]</font> To register user-defined server-side logic in a collection.


### $skip query
<font size=1>[OData]</font> One of the supported OData queries. This query is for extracting data excluding the specified count from the display among acquired data. ([Details](../apiref/current/402_Skip_Query.md))


## <a name="anc_t"> T</a>
### Token
<font size=1>[General]</font> A random string used mainly for user authentication. Tokens are used for access to stored data and resources in Personium. A token is described in the cURL requested by a client.  
There are the following types in Personium, and the tokens are changed an hour after issuing.  
(1)Cell local token: Used for the access to resources in the authenticated cell  
(2)Trans-cell token: Used for the access to resources in a cell authenticated by another cell  



### Token authentication
<font size=1>[General]</font> One of authentication processes. The method for authentication using the access token described in the cURL requested by a client. For details, refer to [Certification Model](./003_Auth.md).


### $top query
<font size=1>[OData]</font> One of the supported OData queries. This specifies the maximum number of acquired data records and returns data for that count. Extracted data is counted from the beginning in the set. ([Details](../apiref/current/401_Top_Query.md))


## <a name="anc_u"> U</a>
### Unit
<font size=1>[Personium]</font> The data area composed of multiple cells on the Personium platform server. It has a fully qualified domain name (UnitFQDN) that is referred to as the absolute domain name.


### Unit control object
<font size=1>[Personium]</font> A group of objects for creating and managing cells as the unit user (administrator).


### Unit User
<font size=1>[Personium]</font> Unit administrator user. This user has CRUD (Create/Read/Update/Delete) privileges within the unit.


## <a name="anc_w"> W</a>
### WebDAV
<font size=1>[WebDAV]</font> An abbreviation of "Web-based Distributed Authoring and Versioning". This is the protocol for various users to co-write documents and files on the Web server; it is an extension of HTTP.  
On the Personium portal, WebDAV collections are files and folders, and CRUD functions are used.  
Refer to [WebDAV Resources](https://web.archive.org/web/20120626092812/http://webdav.org/).  
  
  
  

##### [A](#anc_a) | [B](#anc_b) | [C](#anc_c) | D | [E](#anc_e) | [F](#anc_f) | G | H | [I](#anc_i) | J | K | L | [M](#anc_m) | [N](#anc_n) | [O](#anc_o) | [P](#anc_p) | Q | [R](#anc_r) | [S](#anc_s) | [T](#anc_t) | [U](#anc_u) | V | [W](#anc_w) | X | Y | Z  
  
  
  


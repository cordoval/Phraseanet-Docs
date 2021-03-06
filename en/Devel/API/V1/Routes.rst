Routes
======


.. toctree::
    :hidden:

    Route/Databox/List
    Route/Databox/Collections
    Route/Databox/Status
    Route/Databox/Metadatas
    Route/Databox/TermsOfUse
    Route/Records/Search
    Route/Records/Metadatas
    Route/Records/Status
    Route/Records/Embed
    Route/Records/Related
    Route/Records/Record
    Route/Records/SetStatus
    Route/Records/SetMetadatas
    Route/Records/SetCollection
    Route/Baskets/Add
    Route/Baskets/Content
    Route/Baskets/Delete
    Route/Baskets/List
    Route/Baskets/SetDescription
    Route/Baskets/SetName
    Route/Feeds/List
    Route/Feeds/Content


Phraseanet API provides routes to access resources using canonical URL. 
These resources are listed below.

For the moment, all these routes require authentication. 
Phraseanet API uses POST and GET methods.

For each resource, some aspects and actions are avalaible. 
For example, you can get the permalinks of a record with the following route: 


+----------+--------------------------------------+------------------------------------------------+------------------------------------------------------+
|          | General                              | Aspect                                         | Act                                                  |
+==========+======================================+================================================+======================================================+
| databox  |* :doc:`list <Route/Databox/List>`    |* :doc:`collections <Route/Databox/Collections>`|                                                      |
|          |                                      |* :doc:`status <Route/Databox/Status>`          |                                                      |
|          |                                      |* :doc:`metadatas <Route/Databox/Metadatas>`    |                                                      |
|          |                                      |* :doc:`termsOfUse <Route/Databox/TermsOfUse>`  |                                                      |
+----------+--------------------------------------+------------------------------------------------+------------------------------------------------------+
| records  |* :doc:`search <Route/Records/Search>`|* :doc:`metadatas <Route/Records/Metadatas>`    |* :doc:`setstatus <Route/Records/SetStatus>`          |
|          |                                      |* :doc:`status <Route/Records/Status>`          |* :doc:`setcollection <Route/Records/SetCollection>`  |
|          |                                      |* :doc:`embed <Route/Records/Embed>`            |* :doc:`setmetadatas <Route/Records/SetMetadatas>`    |
|          |                                      |* :doc:`related <Route/Records/Related>`        |                                                      |
|          |                                      |* :doc:`record <Route/Records/Record>`          |                                                      |
+----------+--------------------------------------+------------------------------------------------+------------------------------------------------------+
| baskets  |* :doc:`list <Route/Baskets/List>`    |* :doc:`content <Route/Baskets/Content>`        |* :doc:`setname <Route/Baskets/SetName>`              |
|          |* :doc:`add <Route/Baskets/Add>`      |                                                |* :doc:`setdescription <Route/Baskets/SetDescription>`|
|          |                                      |                                                |* :doc:`delete <Route/Baskets/Delete>`                |
+----------+--------------------------------------+------------------------------------------------+------------------------------------------------------+
| feeds    |* :doc:`list <Route/Feeds/List>`      |* :doc:`content <Route/Feeds/Content>`          |                                                      |
+----------+--------------------------------------+------------------------------------------------+------------------------------------------------------+


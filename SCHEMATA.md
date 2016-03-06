# Schemata

We came to the conclusion, that our primary goal should be extensibility. Therefore, the communication between the database and the routing service will be divided into an *GIS* schema (longitude and latitude, terrain height etc), an *OSM* schema (street names, connected nodes), a *weather* schema (temperature, wind etc) and a *traffic* schema (traffic, average speed etc). This model is extensible and allows to integrate new data providers without breaking backwards compatibility.

The front end consumes a different schema: to minimize the data traffic in order to improve mobile performance, only the necessary routing data will be transmitted. For the prototyping tool, a second more verbose schema is needed to show/count all tested points during the algorithm as well as the order.

Queries to either service are all performed using REST.

## Overview

From | To | Schema name | Status
--- | --- | --- | ---
Data service | Routing service | GIS | *TODO*
Data service | Routing service | OSM | *TODO*
Data service | Routing service | Weather | *TODO*
Data service | Routing service | Traffic | *TODO*
Routing service | Front end | Routing | *TODO*
Routing service | Prototyping tool | Verbose routing | *TODO*

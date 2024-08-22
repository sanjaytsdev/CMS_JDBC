CREATE CONTACTGROUP TABLE
---------------------------
CREATE TABLE contactgrp (grpid INTEGER PRIMARY KEY, grpname TEXT NOT NULL, grpdesc TEXT );

CREATE CONTACT TABLE
---------------------------
CREATE TABLE contacts (contactid INTEGER PRIMARY KEY, contactgrpid INTEGER, contactname TEXT NOT NULL, contactphone TEXT NOT NULL, contactaddress TEXT, contactpin TEXT, FOREIGN KEY (contactgrpid) REFERENCES contactgrp(grpid) );

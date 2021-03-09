---
title: ASNA DataGate Studio Overview

Id: dgStudioOverview
TocParent: Welcome
TocOrder: 2

keywords: welcome to DataGate Studio
keywords: DataGate Studio, overview
keywords: DataGate Studio, about
keywords: DataGate Studio, DataGate Explorer
keywords: DataGate Explorer, DataGate Studio
keywords: getting started, DataGate Studio
keywords: overview, DataGate Studio

---

ASNA DataGate is a Database Management System, which, like all databases allows you to describe data formats, access paths, and store and retrieve data. 

DataGate Studio (the replacement for the existing database management product; ASNA DataGate Database Manager) is a utility that operates within ASNA DataGate, allowing you to manipulate objects in the DataGate database in a manner similar to Microsoft's Visual Studio Team System Database Edition, or SQL Management Studio. These objects include: libraries, file, and members. 

**DataGate Studio consists of three main display windows** 

1. The DataGate Explorer window is used to browse servers, databases, libraries, 
			files and members. For users of the ASNA DataGate Database Manager, DataGate 
			Explorer is most similar to the Active Dictionary Area. DataGate Explorer works 
			in conjunction with the Properties window, which shows management details of 
			the object currently selected.
2. With the Solution Explorer you create and use DataGate projects, with which you 
			can view and create file definitions in source code residing on your PC, and 
			create new database and print files.  DataGate projects are similar to the 
			DataGate Projects of the former Database Manager.
3. The DataGate Import/Export window provides graphical access to the new 
			client/server based facility for saving and deploying database schema and data.

Basic operations such as copy, delete, move, rename, save and restore can be done to DataGate Explorer objects from within the DataGate Studio in an interactive manner.

You can easily create Physical, Simple, Join, Multiformat, SQL Logical and print files using the editors, designers, and commands in a DataGate project. 

To do this, first create a database file definition, giving a description of the file type, its record format and access path. The record format will also be created, which stores the fields, keys, and Select/Omit Rule nodes. Then add fields, keys, and Select/Omit Rules to the appropriate node. 

When all record format information is entered, you then Create the File, which takes the database file definition from a DataGate project source file and creates the defined file and a member into a selected library in the database. Additional members, who hold a collection of records and access paths, can be added to the file. 

## DataGate Explorer - Database Management
<div>
For database management, a VSIP-based tree control, known as " **DataGate Explorer** ", is the focus of operations.

- The tree has two primary nodes for manipulating database 
  			connections and database names, respectively.
- Connections are current connections to the database used to 
  			directly interact with the database server.

For example, here you could rename a file or use drag-and-drop operations to move a library. The DataGate Explorer is the primary axis for administrative tasks, as shown below.

![DataGate Menu Options](../images/DataGate_Explorer.png) 
DataGate Projects

For development tasks, a "DataGate Projects" is used, which is similar to a Visual Studio language project. Instead of building programs however, a DataGate project is intended to be used to host database file definitions, and the commands to create files and extract their metadata.

With a DataGate project, an applications programmer (or administrator) can maintain DataGate file definitions as source files. 

DataGate projects are hosted by the VS Solution Explorer (in the far right pane). Source files containing file definitions are editable with both designer and code view windows. Application support will be provided by a suite of controls and libraries.

To date, we have completed initial development of controls used to edit connection details (and database names), browse libraries, edit/view data, and copy libraries. 

![DataGate Explorer](../images/Solution.png) 

#### DataGate Options
The majority of the DataGate options are the same as in DataGate Database Manager, and can be found from the **DataGate** menu from within Visual Studio, as shown below.
<img alt="DataGate Explorer" src="../images/DataGate_Menu_Options.png" />

---

<span> *[ © 2008-2018 ASNA. All rights reserved. ](mailto:Documentation@asna.com">Submit feedback to ASNA</a>* </span> 

*<a href="Copyright.html)* 

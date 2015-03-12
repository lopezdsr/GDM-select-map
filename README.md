# GDM-select-map
Dynamically select a message map (graphical data map) that is used by a Mapping node in an integration solution. 

This tutorial demonstrates how to select a message map (also known as a graphical data map) at run time based on information passed as part of the input XML message. 

This Graphical Data Mapping capability in IBM Integration Bus is implemented within an application. In this application, a message flow defines the steps required to implement the message transformation and the message split logic of the solution.

An application is a container for all the resources that are required to create the solution. An application can contain IBM Integration Bus resources, such as message flows, message models, libraries, and JAR files.

The application takes as input one file.

The message model that represents the input message is defined by an XML schema. This model is contained in a shared library. The library is then referenced by the application.

A FileInput node is used to model the input step in the message flow. When the input node detects that a file with one or more records is available, it parses the content of the file, and sends the internal message representation to the next step in the flow. In this tutorial, an internal message is created for each sales item record in the input file.

The first Mapping node in the solution is used to define the logic so that a message map can be assigned dynamically at runtime based on data from the input message.

A second Mapping node is used to model the graphical data transformation step in the message flow. The mapping node has a default associated message map.

The message map is the resource you use to define and implement the data transformation and message split requirements.

A FileOutput node is used to place any output messages in the file system.

The output message is a JSON message.

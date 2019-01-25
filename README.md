# WebSchemaVisualizer

WebSchemaVisualizer is a web application that visualizes the schema evolution of relational Dbs.

It utilizes the functionalities provided by the [ParmenidianTruth][1] tool to compute a set of statistics related to evolution and also to visualize the schema history as well as four evolution-related patterns.

It consists of 2 submodules, namely [ParmenidianTruth-API][2] and [WebParmenidianTruth][3] projects. The former is responsible for providing the main functionalities of the ParmenidianTruth tool to the latter one. The latter is responsible for implementing the following functionalities:

 * **Create** a new project via uploading a set of DD files that contain the history of schema evolution 
 * **Load** a project from the server
 * **Visualize** Diachronic Graph(nodes:set of DB's tables, edges:set of FK constraints)/schema versions
 * **Visualize** evolution-related patterns
 * **Compute** evolution-related statistics
 
### To clone the project, please follow these steps:
1. In a git bash, type `<git clone https://github.com/kdimolikas/WebSchemaVisualizer.git>`
2. From the project folder (WebSchemaVisualizer) in the bash, type `<git submodule init>`
3. Type `<git submodule update>`

### To import the project in Eclipse, you shall do the following:
1. Select File->Import
2. Select Git->Projects from Git
3. Select Existing local repository
4. Choose *Next* until the import process is finished

### To build the project in Eclipse, the steps are:
1. Right click on *WebSchemaVisualizer* project, then select *Maven -> Update Project*
2. Right click on *WebSchemaVisualizer* project, then select *Run As -> Maven clean*
3. Right click on *WebSchemaVisualizer* project, then select *Run As -> Maven install* (in case you have installed Maven as standalone tool, you can merge steps 2 and 3 by typing in a terminal (from the *WebSchemaVisualizer* folder) `<mvn clean install>`)

### To run the application, there are 2 alternatives:
* In case you have not installed Maven as standalone tool, the recommended steps are:  
1. Right click on the *WebParmenidianTruth* project, then select *Run As -> Run Configurations*
2. In the text field *Goals*, type `<jetty:run>` and then select *Run*
3. In any browser, type `<localhost:8080>`

* Otherwise, you can merge steps 1 and 2 via typing in a terminal (from the *WebParmenidianTruth* folder) `<mvn jetty:run-war>`




[1]:https://github.com/DAINTINESS-Group/ParmenidianTruth
[2]:https://github.com/kdimolikas/ParmenidianTruth-API
[3]:https://github.com/kdimolikas/WebParmenidianTruth
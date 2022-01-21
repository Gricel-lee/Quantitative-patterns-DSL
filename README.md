# Quantitative-patterns-DSL

## Installation from a new project

### Ecore diagram

Useful resources: https://eclipsesource.com/blogs/tutorials/emf-tutorial/
We will be using Eclipse Modelling Tools 2020. 

In Eclipse, install the plugins Xtext and Xtend (Help> Eclipse Marketplace).

Create a new Empty EMF project. 

![image](https://user-images.githubusercontent.com/63869574/150193041-1a012626-ef52-46a1-aaea-6681dae78894.png)

Next > Project name se.gu.uoy.dsl > Finish.

Right click in the model folder and create a new Ecore Model
![image](https://user-images.githubusercontent.com/63869574/150193584-60f2ffe1-4ea8-4278-a747-1d214ca296f6.png)

![image](https://user-images.githubusercontent.com/63869574/150193659-2d973eab-958a-4b9c-a8fd-f7170da24ba8.png)

Next > File Name: quantitativePatterns.ecore > Finish

![image](https://user-images.githubusercontent.com/63869574/150193843-82f893fa-a780-4c21-b8b9-065ad1d4c7d5.png)

Go to the location of the file in the file explorer and open it.

![image](https://user-images.githubusercontent.com/63869574/150194057-5c970450-e0c2-4b78-a2d2-26b270382ce2.png)

It should contain:
![image](https://user-images.githubusercontent.com/63869574/150194099-117f5448-8a77-4c2d-ba21-b8124c2f0e5c.png)

We are going to merge the files already developed at: https://github.com/SergioGarG/quantitative-patterns/blob/main/se.gu.patterns/model/patterns.ecore and our new Ecore Model. In my case, I copied and pasted, except for the attribute at the beggining **xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"**

In Eclipse, Refresh the project. 

Open the Ecore file and right click on the root > Validate, to check if the model is correct.
![image](https://user-images.githubusercontent.com/63869574/150230521-304a1d7d-4b4b-4bf3-83f9-3a556e54b685.png)


Right click on the Ecore Model > Initialize Ecore Diagram > File name: quantitativePatterns.aird > Next > Entities in a Class Diagram > Finish.

![image](https://user-images.githubusercontent.com/63869574/150195152-8ca289bc-e1d7-4d6b-ad80-7807b5306000.png)

![image](https://user-images.githubusercontent.com/63869574/150195185-2725a23b-74e4-436f-98be-cc6008ee11a1.png)

![image](https://user-images.githubusercontent.com/63869574/150195237-ff53c56d-314c-406a-b414-94ec9f097c46.png)

Double click on: 

![image](https://user-images.githubusercontent.com/63869574/150195330-f0ab12e2-ed23-4c61-b684-0aa22e12b32d.png)

You should be able to visualize the Ecore Diagram.

![image](https://user-images.githubusercontent.com/63869574/150195468-c6d809cb-cd57-4702-8fd0-bfb5637eabc4.png)

### Generator Model

Right click on the Ecore Model and create a new EMF Generator Model> Next > Next > Ecore model > Select the Ecore File and click Load > Next > Finish

![image](https://user-images.githubusercontent.com/63869574/150195820-81e60fca-708a-4a2b-8b0b-5b4629133fe0.png)

![image](https://user-images.githubusercontent.com/63869574/150195857-4cbe8f35-8bc1-43db-8d6c-419a590e8637.png)

![image](https://user-images.githubusercontent.com/63869574/150195894-262f1061-194e-4cb7-9ed5-70bb7c7f6658.png)

![image](https://user-images.githubusercontent.com/63869574/150195964-f2509110-bf8c-462c-95ab-3cc874d5467c.png)

![image](https://user-images.githubusercontent.com/63869574/150196036-2f3c2924-c970-40b2-bc9f-c004d0b9a737.png)

This should create some code in the "src" folder and the .genmodel. Right click at the root of the .genmodel and select Generate All.

![image](https://user-images.githubusercontent.com/63869574/150196227-92a332c5-7a3c-4c80-b831-f23da9d42481.png)

This should generate: 

![image](https://user-images.githubusercontent.com/63869574/150196304-8897aed0-87a8-4a98-ab49-5df1fddde94a.png)

NOTE: If the genmodel needs to be change: delete the "src" folder in the main Ecore project, the build.properties, plugin.properties and plugin.xml files; and delete the three lines in the MANIFEST.MF file (to see the code select the tab MANIFEST.MF from underneath the opened file).

![image](https://user-images.githubusercontent.com/63869574/150198010-c63cf6a9-2723-41e1-b595-07d18f4c3a60.png)

![image](https://user-images.githubusercontent.com/63869574/150198051-fc866f09-6863-4f70-a115-1420fa0551d4.png)

### Xtext

Help link: http://koehnlein.blogspot.com/2010/03/xtext-for-your-ecore-models.html

Right click on each of the folders (plugins) and Configure > Convert to Xtext Project

![image](https://user-images.githubusercontent.com/63869574/150229813-e097e857-add4-4ff3-803f-a4b608e77179.png)

Then File > New > Other > Xtext > Xtext Project From Existing Ecore Models > Add the .genmodel and select Scenario as Entry rule > Next > Finish 

![image](https://user-images.githubusercontent.com/63869574/150231308-dba68cd5-10a1-4676-9972-e28223fef640.png)

![image](https://user-images.githubusercontent.com/63869574/150231527-9e6f8e80-1edc-46ac-b2bf-b7682258b259.png)

It should generate 4 new plugins:

![image](https://user-images.githubusercontent.com/63869574/150231843-99885bf7-0dc7-45a5-8b29-ab3d1b5cfbdd.png)

Open the .xtext file on the src folder of the first plugin. 

![image](https://user-images.githubusercontent.com/63869574/150232125-bbdf1022-bd65-4c12-923d-6bbd3f43897f.png)

We will merge this file with https://github.com/SergioGarG/quantitative-patterns/blob/main/se.gu.xtext.patterns/src/se/gu/xtext/patterns/Pattens.xtext

In this case, Eclipse detects an error associated with Maintain, AbortIf and ResumeIf:

![image](https://user-images.githubusercontent.com/63869574/150232952-9b30f8ec-a645-4684-aa91-368dbcc844fe.png)

Changing "locationevent+=LocationEvent" to "locationevent=LocationEvent" should solve the problem (however, further changes are done later).

## New Ecore and Xtext files
The reviewed ecore and xtext files are available here.


## Run Xtext file

Right click on the first xtext plugin > Run as > Run Configuration > Run

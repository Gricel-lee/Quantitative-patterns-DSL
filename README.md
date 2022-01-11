# Quantitative-patterns-DSL

## Installation

- Download from https://github.com/Askarpour/quantitative-patterns
- Unzip
- In Eclipse, install the plugins Xtext and Xtend
- File > Import > Project from Folder or Archive, and import unzipped folders one by one that start with "se.gu.patterns"
- Go to:

![image](https://user-images.githubusercontent.com/63869574/148663951-50f56bd5-85c4-4420-bd0c-bd37acfcca3c.png)

- select one of the representations to visualize the ecore DSL pattern:

![image](https://user-images.githubusercontent.com/63869574/148664047-68611d79-291e-49f4-befa-0f2fae19a256.png)



## Errors
# Not solved yet:
![image](https://user-images.githubusercontent.com/63869574/148935347-2b77ff2d-b568-4a12-96f1-30083f373e43.png)

(Solution didn't work)
Go to Help > Install new software. In Work With select All available sites:

![image](https://user-images.githubusercontent.com/63869574/148935707-5041d4f0-e812-4f6f-82d2-17c8e51cfddb.png)

Then look for the unclassified ones that contains SWT. Click next and install:

![image](https://user-images.githubusercontent.com/63869574/148935561-690b1571-9703-4224-8fc5-f9d1a27a1572.png)

##

![image](https://user-images.githubusercontent.com/63869574/148951215-522521f5-30df-4df8-879b-be08ddcee034.png)


# Tries:
// Empty workspace
C:\Users\grist\Documents\eclipse2021-workspace
//Open Eclipse EMF


************************ 1)
From sergio repository:
https://github.com/SergioGarG/quantitative-patterns
- Import > General Projects from Folder or Archive > se.gu.patterns

Warnings:
Execution environment is lower than one of the plug-in's dependencies (org.eclipse.core.runtime) which has an execution environment of JavaSE-11.	MANIFEST.MF	/se.gu.patterns/META-INF	line 10	Plug-in Problem
The JRE container on the classpath is not a perfect match to the 'J2SE-1.5' execution environment	MANIFEST.MF	/se.gu.patterns/META-INF	line 10	Plug-in Problem
There is no 'jre.compilation.profile' build entry and the project has Java compliance preferences set	build.properties	/se.gu.patterns	line 1	Plug-in Problem
Unknown referenced nature: org.eclipse.ocl.pivot.ui.oclnature.	.project	/se.gu.patterns	Unknown	Unknown nature

*********************** 2)
Copy all files from Sergio repository into workspace: eclipse2021-workspace


-Open eclipse

Warning:
The ... workspace was written with an older version. Continue and update workspace which may make it incompatible with older versions?

-Click continue
![image](https://user-images.githubusercontent.com/63869574/149015231-115a212a-0183-4f36-8766-0badabf7ccf1.png)

Errors:
![image](https://user-images.githubusercontent.com/63869574/149015340-b2c260f6-9b6f-47d5-99e4-5f409485ad0a.png)

![image](https://user-images.githubusercontent.com/63869574/149015416-c5db9e25-b8f1-487e-bf93-88b159f7b81b.png)

NOTE: Found the DSL rules in: se.gu.xtext.patterns/src/se/gu/xtext/patterns/Patterns.xtext

![image](https://user-images.githubusercontent.com/63869574/149015549-c62f13a8-53e0-44ab-8b1a-7e850bfb090b.png)


- Delete all (also on directory ![image](https://user-images.githubusercontent.com/63869574/149017095-88b661e2-c6dd-4702-bc6b-afec43f195fa.png)
 ) except:

![image](https://user-images.githubusercontent.com/63869574/149016980-87390c44-71ee-4dcb-9a9f-094ba0178f75.png)


- 


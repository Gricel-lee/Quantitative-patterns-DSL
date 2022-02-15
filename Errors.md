# Possible Errors

##  org.eclipse.xtext.common.Terminals package not detected in MyDSL.xtext file
Check xtext manifest. It should contains something similar to:
```
Manifest-Version: 1.0
Automatic-Module-Name: org.xtext.example.mydsl
Bundle-ManifestVersion: 2
Bundle-Name: org.xtext.example.mydsl
Bundle-Vendor: My Company
Bundle-Version: 1.0.0.qualifier
Bundle-SymbolicName: org.xtext.example.mydsl; singleton:=true
Bundle-ActivationPolicy: lazy
Require-Bundle: uoy.mrs.dsl,
 org.eclipse.xtext,
 org.eclipse.xtext.xbase,
 org.eclipse.equinox.common;bundle-version="3.5.0",
 org.eclipse.emf.ecore,
 org.eclipse.xtext.xbase.lib;bundle-version="2.14.0",
 org.eclipse.xtext.util,
 org.eclipse.emf.common,
 org.antlr.runtime;bundle-version="[3.2.0,3.2.1)"
Bundle-RequiredExecutionEnvironment: JavaSE-11
Export-Package: org.xtext.example.mydsl.myDsl.util,
 org.xtext.example.mydsl.parser.antlr.internal,
 org.xtext.example.mydsl.scoping,
 org.xtext.example.mydsl.services,
 org.xtext.example.mydsl.generator,
 org.xtext.example.mydsl.validation,
 org.xtext.example.mydsl,
 org.xtext.example.mydsl.myDsl.impl,
 org.xtext.example.mydsl.formatting2,
 org.xtext.example.mydsl.myDsl,
 org.xtext.example.mydsl.serializer,
 org.xtext.example.mydsl.parser.antlr
Import-Package: org.apache.log4j
```

where ```Require-Bundle: uoy.mrs.dsl``` is the project containing the .ecore file; and ```org.xtext.example.mydsl``` is the xtext project.


## Downloading ANTLR parser generator failed: download.itemis.com. Please install the feature 'Xtext Antlr SDK' manually using the external updatesite: 'http://download.itemis.com/updates/'.

Go to Marketplace and uninstall/reinstall Xtext. 

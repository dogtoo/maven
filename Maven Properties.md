## Full detailed explanations can be found in Maven Model Builder Interpolation reference documentation.

### This page extracts a few classical values:
```
${project.basedir} 
```
. This references to the root folder of the module/project (the location where the current pom.xml file is located)

### POM properties referencing useful build locations, with default values defined in the Super POM:
1. This represents by default the target folder.
```
${project.build.directory}
```
2. This represents by default the target/classes folder.
```
${project.build.outputDirectory}
```
3. This represents by default the target/test-classes folder.
```
${project.build.testOutputDirectory}
```
4. This represents by default the src/main/java folder.
```
${project.build.sourceDirectory}
```
5. This represents by default the src/test/java folder.
```
${project.build.testSourceDirectory}
```

### You can use further properties like the following:

1. This is by default defined as ${project.artifactId}-${project.version}.
```
${project.build.finalName}
```

2. This can be used at locations where you have to write a literal version otherwise, in particular if you are in a multi-modules build for inter modules dependencies.
```
${project.version}
```

### user Settings

#### The settings.xml elements could be referenced by using things like this (see also at the Super POM):
```
${settings.localRepository}
```
which references the location of the local repository. This is by default ${home}/.m2/repository.

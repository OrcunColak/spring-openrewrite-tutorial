# Read me

The original idea is from  
https://hkcodeblogs.medium.com/upgrade-springboot-applications-to-latest-version-in-10-minutes-9bd141d02498

To upgrade from Spring 3.2 to Spring 3.3 run

```
mvn rewrite:run
```
or 
```
mvn -U org.openrewrite.maven:rewrite-maven-plugin:run -Drewrite.recipeArtifactCoordinates=org.openrewrite.recipe:rewrite-spring:RELEASE -Drewrite.activeRecipes=org.openrewrite.java.spring.boot3.UpgradeSpringBoot_3_3 -Drewrite.exportDatatables=true

Windows
mvn -U org.openrewrite.maven:rewrite-maven-plugin:run "-Drewrite.recipeArtifactCoordinates=org.openrewrite.recipe:rewrite-spring:RELEASE" "-Drewrite.activeRecipes=org.openrewrite.java.spring.boot3.UpgradeSpringBoot_3_3" "-Drewrite.exportDatatables=true"

```



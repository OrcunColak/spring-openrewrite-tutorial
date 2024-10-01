# Read me

The original idea is from  
https://hkcodeblogs.medium.com/upgrade-springboot-applications-to-latest-version-in-10-minutes-9bd141d02498

To upgrade from Spring 3.2 to Spring 3.3 run

To upgrade from configuration

```
mvn rewrite:run
```

To upgrade Java from CLI

```
[mvn -U org.openrewrite.maven:rewrite-maven-plugin:run "-Drewrite.recipeArtifactCoordinates=org.openrewrite.recipe:rewrite-migrate-java:RELEASE" "-Drewrite.activeRecipes=org.openrewrite.java.migrate.UpgradeToJava21" "-Drewrite.exportDatatables=true"]()
```

To upgrade Spring from CLI

```
mvn -U org.openrewrite.maven:rewrite-maven-plugin:run -Drewrite.recipeArtifactCoordinates=org.openrewrite.recipe:rewrite-spring:RELEASE -Drewrite.activeRecipes=org.openrewrite.java.spring.boot3.UpgradeSpringBoot_3_3 -Drewrite.exportDatatables=true

Windows
mvn -U org.openrewrite.maven:rewrite-maven-plugin:run "-Drewrite.recipeArtifactCoordinates=org.openrewrite.recipe:rewrite-spring:RELEASE" "-Drewrite.activeRecipes=org.openrewrite.java.spring.boot3.UpgradeSpringBoot_3_3" "-Drewrite.exportDatatables=true"

```



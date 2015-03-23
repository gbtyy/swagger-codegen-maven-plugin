swagger-codegen-maven-plugin
============================

A Maven plugin to support the [swagger](http://swagger.io) code generation project

Usage
============================

Add to your `build->plugins` section (default phase is `generate-sources` phase)
```xml
<plugin>
    <groupId>com.wordnik.swagger</groupId>
    <artifactId>swagger-codegen-maven-plugin</artifactId>
    <version>0.0.1-SNAPSHOT</version>
    <executions>
        <execution>
            <goals>
                <goal>generate</goal>
            </goals>
            <configuration>
                <inputSpec>src/main/resources/api.yaml</inputSpec>
                <language>java</language>
            </configuration>
        </execution>
    </executions>
</plugin>
```

Followed by:

```
mvn clean compile
```

### Configuration parameters

- `inputSpec` - swagger spec file path
- `language` - target generation language
- `output` - target output path (default is `${project.build.directory}/generated-sources/swagger`)
- `templateDirectory` - directory with mustache templates


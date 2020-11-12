# Seudev's Style Guide

The Seudev's Style Guide

## Java

### Eclipse Formatter

The `eclipse-java-seudev-style.xml` file is an Eclipse Formatter configured with the *Seudev's Style*.
It is compatible with some plugins and IDEs, see below how to use it:

#### Maven plugin

Use the [formatter-maven-plugin](https://github.com/revelc/formatter-maven-plugin) to format your Maven project automatically during a Maven build.
Paste the below code in the `pom.xml` file:

```xml
<build>
    <plugins>
        <plugin>
            <groupId>net.revelc.code.formatter</groupId>
            <artifactId>formatter-maven-plugin</artifactId>
            <version>2.13.0</version>
            <configuration>
                <configFile>https://raw.githubusercontent.com/seudev/seudev-style-guide/v1.0.0/java/eclipse-java-seudev-style.xml</configFile>
                <overrideConfigCompilerVersion>true</overrideConfigCompilerVersion>
                <lineEnding>LF</lineEnding>
            </configuration>
            <executions>
                <execution>
                <goals>
                    <goal>format</goal>
                </goals>
                </execution>
            </executions>
        </plugin>
    </plugins>
</build>
```

For more details, see the [documentation](https://code.revelc.net/formatter-maven-plugin).

**Note**: If you have network restrictions, then download the [eclipse-java-seudev-style.xml](https://raw.githubusercontent.com/seudev/seudev-style-guide/v1.0.0/java/eclipse-java-seudev-style.xml)
file and put the file path in the `configFile` tag (e.g `${project.basedir}/eclipse-java-seudev-style.xml`).

#### VSCode

Set the following properties, in the **settings.json** file:

```json
"java.format.settings.profile": "Seudev's Style",
"java.format.settings.url": "https://raw.githubusercontent.com/seudev/seudev-style-guide/v1.0.0/java/eclipse-java-seudev-style.xml"
```

**Note**: If you have network restrictions, then download the [eclipse-java-seudev-style.xml](https://raw.githubusercontent.com/seudev/seudev-style-guide/v1.0.0/java/eclipse-java-seudev-style.xml) file
and put the file path in the `java.format.settings.url` property (e.g. `file://path/to/eclipse-java-seudev-style.xml`).

#### Eclipse

1. Download the [eclipse-java-seudev-style.xml](https://raw.githubusercontent.com/seudev/seudev-style-guide/v1.0.0/java/eclipse-java-seudev-style.xml) file;
2. In eclipse, click `Window` > `Preferences` > `Java` > `Code Style` > `Formatter`, then click on the `Import...` button and select the `eclipse-java-seudev-style.xml` file.

## Licensing

**seudev/seudev-style-guide** is provided and distributed under the [Apache Software License 2.0](http://www.apache.org/licenses/LICENSE-2.0).

Refer to *LICENSE* for more information.

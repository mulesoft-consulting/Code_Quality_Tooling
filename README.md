# Code Quality Tooling

This repository covers possible maven plugins to include code quality and testing
tooling. Currently included are:

- CheckStyle: in the CheckStyle folder is a configuration file which contains
  the setting based on the Mulesoft documentation. The configuration file is
  set-up to cover the Maven plugin 3.0.0 (which is different from
  the earlier versions.) Note: the Maven plugin is based on CheckStyle 6.13,
  which is different and not compatible with the currently latest version 8.8.

## Maven Plugins:

### CheckStyle:

The following plugin definition needs to be added to the `<reporting>` block of
the `pom.xml` file:

```
<plugin>
  <groupId>org.apache.maven.plugins</groupId>
  <artifactId>maven-checkstyle-plugin</artifactId>
  <version>3.0.0</version>
  <configuration>
    <configLocation>checkstyle-config.xml</configLocation>
  </configuration>
</plugin>
```

The `checkstyle-config.xml` file can be found in the CheckStyle folder in
this repository.

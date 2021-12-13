## 01. Submodule modify : uaa (src/uaa)

> $ vi src/uaa/dependencies.gradle
```diff
 // Versions we're overriding from the Spring Boot Bom
-ext["mariadb.version"] = "2.3.0"
+ext["mariadb.version"] = "2.5.1"
 ext["flyway.version"] = "5.2.4"
+ext['log4j2.version'] = '2.15.0' // this pinning can be removed when we bump to a spring boot version that has 2.15.0+ (due to CVE https://github.com/advisories/GHSA-jfh8-c2jp-5v3q in log4j < 2.15.0)

 // Versions shared between multiple dependencies
```

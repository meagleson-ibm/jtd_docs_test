# POM template \(reference\)

```
<project xmlns="http://maven.apache.org/POM/4.0.0"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
<!-- IBM Confidential         -->
<!-- Copyright IBM Corp. 2024 -->
    <modelVersion>4.0.0</modelVersion>

    <groupId>com.ibm.gbs.intldsgn</groupId>
    <artifactId>intldsgn-data-application</artifactId>
    <version>0.1</version>
    <name>intldsgn-data-application</name>
    <description>Intelligent Design Database Service</description>

    <properties>
        <java.version>1.8</java.version>
    </properties>

    <dependencies>
        <dependency>
            <groupId>org.postgresql</groupId>
            <artifactId>postgresql</artifactId>
            <version>42.3.3</version>
        </dependency>
        <dependency>
            <groupId>org.liquibase</groupId>
            <artifactId>liquibase-core</artifactId>
            <version>4.8.0</version>
        </dependency>

    </dependencies>
    <profiles>
        <profile>
            **<id\>id-prod</id\>**
            <properties>
                <liquibase.rollbackTag>v.5.0.10</liquibase.rollbackTag>
            </properties>
            <build>
                <plugins>
                    <plugin>
                        <groupId>org.liquibase</groupId>
                        <artifactId>liquibase-maven-plugin</artifactId>
                        <version>4.8.0</version>
                        <configuration>
                            <driver>org.postgresql.Driver</driver>
                            <promptOnNonLocalDatabase>false</promptOnNonLocalDatabase>
                            <changeLogFile>src\main\resources\master-changelog.xml</changeLogFile>
	             **<contexts\>$\{liquibase.contexts\}</contexts\>**
                        </configuration>
                        <executions>

                            <execution>
                                **<id\>rapidus-id-prod</id\>**
                                <phase>process-resources</phase>
                                <configuration>
                                    **<url\>\[DATABASE URL\]</url\> <!-- Update DATABASE URL --\>
                                    <username\>\[USERNAME\]</username\> <!-- UPDATE DATABASE USERNAME --\>
                                    <password\>\[PASSWORD\]</password\> <!-- UPDATE DATABASE PASSWORD --\>**
                                </configuration>

                                <goals>
                                    <goal>update</goal>
                                </goals>
                            </execution>

                            <execution>
                                **<id\>rapidus-id-prod-rollback</id\>**
                                <phase>clean</phase>
                                <configuration>
                                    **<url\>\[DATABASE URL\]</url\> <!-- Update DATABASE URL --\>
                                    <username\>\[USERNAME\]</username\> <!-- UPDATE DATABASE USERNAME --\>
                                    <password\>\[PASSWORD\]</password\> <!-- UPDATE DATABASE PASSWORD --\>**
                                </configuration>

                                <goals>
                                    <goal>rollback</goal>
                                </goals>
                            </execution>
                        </executions>
                    </plugin>
                </plugins>
            </build>
        </profile>
    </profiles>
</project>

```

**Parent topic:**[Deploying Intelligent Design data repositories](../../id_docs/installation/deploy_data_repos.md)


 1. Caused by: java.lang.NullPointerException: Cannot invoke "org.springframework.boot.docker.compose.core.DockerCliInspectResponse.hostConfig()" because "inspectResponse" is null
* Fixed by change docker-compose.yml version to 3.8

2. In build.gradle change org.springframework.boot version from 3.1.1 to 3.1.6
*  https://github.com/spring-projects/spring-boot/issues/37982

3. Also upgrade spring boot version from 3.1.3 to 3.1.6 in pom.xml

4. I have postgres run on local uninstall it อาการคือไม่สร้าง user/pass/db petclinic

5. Failed to execute goal org.apache.maven.plugins:maven-checkstyle-plugin:3.2.2:check (nohttp-checkstyle-validation) on project spring-petclinic: You have 20 Checkstyle violations.
* mvnw package -Dcheckstyle.skip 

Remark
If still cannot build use skip test option
-Dmaven.test.skip=true
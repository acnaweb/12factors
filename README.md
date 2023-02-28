# 12 Factors

### Definition

[12 Factors]

### Java: Factors and Tools

| Factor | Tools |
| --- | --- |
| 1. Codebase | [Git]  |
| 2. Dependencies | [Maven] / [Gradle] |
| 3.1 Configurations | [Ansible] or [Chef] |
| 3.2 Configurations | [Spring Boot] - application.properties/application.yaml |
| 4. Backing Services | [Spring Boot] - IE @Repository |
| 5.1 Build | [Maven]: Build Stage ``` mvn clean compile test package ``` |
| 5.2 Release | [Ansible] + [Packer]: Release Stage ``` packer build application.json ``` |
| 5.3 Run | [Docker]: Run Stage ``` docker run --name <container_id> -it <image_id> ``` |
| 6. Processes | Stateless |
| 7. Port Binding  | Run with ``` java -jar application.jar ``` |
| 8. Concurrency | [Kubernetes] |
| 9. Disposability | [Idempotent Operation] |
| 10. Dev/Prod Parity | [Spring Boot] + [Docker] |
| 11. Logs |[SLF4J] + [Fluentd] + [Elasticsearch] + [Kibana] |
| 12. Admin Processes | 

### References

[12 Factors in Java]

[12 Factors]: <https://12factor.net/pt_br/>
[12 Factors in Java]: <https://www.baeldung.com/spring-boot-12-factor>
[Git]: <https://git-scm.com/>
[Ansible]: <https://www.ansible.com/>
[Chef]: <https://www.chef.io/>
[Maven]: <https://maven.apache.org/>
[Gradle]: <https://gradle.org/>
[Spring Boot]: <https://spring.io/>
[Packer]: <https://www.packer.io/>
[Docker]: <https://www.docker.com/>
[Kubernetes]: <https://www.baeldung.com/kubernetes>
[Idempotent Operation]: <https://www.baeldung.com/cs/idempotent-operations>
[SLF4J]: <https://www.baeldung.com/slf4j-with-log4j2-logback>
[Fluentd]: <https://www.fluentd.org/>
[Elasticsearch]: <https://www.elastic.co/>
[Kibana]: <https://www.elastic.co/products/kibana>
[Groovy integrated with Java ]: <https://www.baeldung.com/groovy-java-applications>


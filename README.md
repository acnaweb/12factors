# 12factors


### Java: Factors and Tools

| Factor | Tools |
| --- | --- |
| 1. Codebase | [Git]  |
| 2. Dependencies | [Maven] / [Gradle] |
| 3.1 Configurations | [Ansible] / [Chef] |
| 3.2 Configurations | [Spring] - application.properties/application.yaml |
| 4. Backing Services | [Spring] - IE @Repository |
| 5.1 Build | [Maven]: Build Stage ``` mvn clean compile test package ``` |
| 5.2 Release | [Ansible] and [Packer]: Release Stage ``` packer build application.json ``` |
| 5.3 Run | [Docker]: Run Stage ``` docker run --name <container_id> -it <image_id> ``` |



#### Links

- [12 Factors in Java](https://www.baeldung.com/spring-boot-12-factor)
- [12 Factors](https://12factor.net/pt_br/)

[Git]: <https://git-scm.com/>
[Ansible]: <https://www.ansible.com/>
[Chef]: <https://www.chef.io/>
[Maven]: <https://maven.apache.org/>
[Gradle]: <https://gradle.org/>
[Spring]: <https://spring.io/>
[Packer]: <https://www.packer.io/>
[Docker]: <https://www.docker.com/>




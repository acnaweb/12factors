# 12 Factors

[12 Factors] é uma metodologia para construir web Apps/Software Como Serviços (SaaS)


- Formatos declarativos para automatizar a configuração inicial
- Contrato claro com o sistema operacional que o suporta
- Portabilidade máxima entre ambientes que o executem
- Implantação em modernas plataformas em nuvem
- Minimizam a divergência entre desenvolvimento e produção
- Implantação contínua para máxima agilidade;
- Escalar sem significativas mudanças em ferramentas, arquiteturas, ou práticas de desenvolvimento

## Factor

### 1. Codebase

- [Git]

### 2. Dependencies

- [npm](https://www.npmjs.com/)
- [Maven](https://maven.apache.org/)
- [Gradle](https://gradle.org/)
- [Composer](https://getcomposer.org/)
- [Bundler](https://bundler.io/)
- [pip](https://pip.pypa.io/en/stable/installation/)


### 3. Configurations 

Use __Environment Variables__ to:

- BD (server, port, credentials)
- SMTP (server, port, credentials)

> `.env` - https://www.ibm.com/docs/pt-br/aix/7.3?topic=files-env-file

Tools:

- [Ansible]
- [Chef]

### 4. Backing Services

Programação baseada em __interfaces__ usando DI [Dependency Ingection](https://en.wikipedia.org/wiki/Dependency_injection)

- BD (server, port, credentials)
- SMTP (server, port, credentials)

> .env - https://www.ibm.com/docs/pt-br/aix/7.3?topic=files-env-file

### 5. Build, release, run

#### 5.1 Build

- Download de dependencias
- Geração de binário
- Packaging

#### 5.2 Release

- Merge das configurações com a saída de `5.1 build`

#### 5.3 Run

- Deploy em ambiente

### 6. Processes 

- Stateless
- Use JWT
- Assets shared
- Use Redis/Mencache para armazenar sessões

Permite uso de Load Balance

### 7. Port Binding

- Self-contained adicionando um webserver library ao app

### 8. Concurrency 

![](https://12factor.net/images/process-types.png)

### 9. Disposability

 [Crash-only design](https://lwn.net/Articles/191059/)

### 10. Dev/Prod Parity

- [Continuous Deployment](https://avc.com/2011/02/continuous-deployment/)

- Docker/Kubernetes para software

### 11. Logs

Output

- stdout
- stderr

Tools

- Prometheus
- Grafana 
- Alertmanager

### 12. Admin Processes

Use [Workers](https://developer.mozilla.org/pt-BR/docs/Web/API/Worker).

- DB migrations
- Run scripts to fix
- Run scripts to send email

Save history

## Languages

### Java: Factors and Tools

| Factor | Tools |
| --- | --- |
| 3.1 Configurations |  |
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
| 12. Admin Processes | |

## References

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

- https://developer.mozilla.org/pt-BR/docs/Web/API/Worker
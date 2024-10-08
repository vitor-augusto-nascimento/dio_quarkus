# aplicativo de votação

Este projeto usa o Quarkus, o Supersonic Subatomic Java Framework.

Se você quiser saber mais sobre o Quarkus, visite o site: https://quarkus.io/ .

## Executando o aplicativo no modo dev

Você pode executar seu aplicativo no modo de desenvolvimento que habilita a codificação dinâmica usando:
'''script de shell
./mvnw compilar quarkus:dev
```

> **_NOTE:_** O Quarkus agora vem com uma interface do usuário de desenvolvimento, que está disponível no modo de desenvolvimento apenas no http://localhost:8080/q/dev/.

## Empacotando e executando o aplicativo

O aplicativo pode ser empacotado usando:
'''script de shell
Pacote ./mvnw
```
Ele produz o arquivo 'quarkus-run.jar' no diretório 'target/quarkus-app/'.
Esteja ciente de que não é um jar_ _über, pois as dependências são copiadas para o diretório 'target/quarkus-app/lib/'.

O aplicativo agora pode ser executado usando 'java -jar target/quarkus-app/quarkus-run.jar'.

Se você quiser criar um _über-jar_, execute o seguinte comando:
'''script de shell
./mvnw pacote -Dquarkus.package.type=uber-jar
```

O aplicativo, empacotado como um _über-jar_, agora pode ser executado usando 'java -jar target/*-runner.jar'.

## Criando um executável nativo

Você pode criar um executável nativo usando: 
'''script de shell
./mvnw pacote -Pnative
```

Ou, se você não tiver o GraalVM instalado, poderá executar a compilação executável nativa em um contêiner usando: 
'''script de shell
./mvnw pacote -Pnative -Dquarkus.native.container-build=true
```

Você pode então executar seu executável nativo com: './target/voting-app-1.0.0-SNAPSHOT-runner'

Se você quiser saber mais sobre como criar executáveis nativos, consulte https://quarkus.io/guides/maven-tooling.

## Guias Relacionados

- Registro GELF ([guia](https://quarkus.io/guides/centralized-log-management)): Registre usando o Graylog Extended Log Format e centralize seus logs em ELK ou EFK
- SmallRye Health ([guia](https://quarkus.io/guides/microprofile-health)): Monitorar a integridade do serviço
- Propagação de contexto do SmallRye ([guide](https://quarkus.io/guides/context-propagation)): Propagar contextos entre threads gerenciados em aplicativos reativos
- RESTEasy Reactive ([guide](https://quarkus.io/guides/resteasy-reactive)): Uma implementação JAX-RS utilizando processamento de tempo de compilação e Vert.x. Esta extensão não é compatível com a extensão quarkus-resteasy ou qualquer uma das extensões que dependem dela.
- OpenTelemetry ([guide](https://quarkus.io/guides/opentelemetry)): Use o OpenTelemetry para rastrear serviços
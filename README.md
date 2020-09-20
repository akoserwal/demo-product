# demo-product project
Quarkus application used as demo product.
used in the scenario:

## How to design an Kubernetes/Openshift Operator

Scenario: https://www.katacoda.com/akoserwal/scenarios/how-to-design-an-operator


## Dependency
Dependency which let us deploy application on Kubernetes/Openshift

```
<dependency>
      <groupId>io.quarkus</groupId>
      <artifactId>quarkus-openshift</artifactId>
</dependency>
```


## Properties
```
quarkus.openshift.expose=true
quarkus.kubernetes-client.trust-certs=true
```

## Kubernetes/Openshift YAML
```
target/kubernetes/kubernetes.json
target/kubernetes/Openshift.json
```


## Docker Image

```
docker push akoserwal/demo-product:tagname
```


## Image

If you want to learn more about Quarkus, please visit its website: https://quarkus.io/ .

## Running the application in dev mode

You can run your application in dev mode that enables live coding using:
```
./mvnw quarkus:dev
```

## Packaging and running the application

The application can be packaged using `./mvnw package`.
It produces the `demo-product-1.0.0-SNAPSHOT-runner.jar` file in the `/target` directory.
Be aware that it’s not an _über-jar_ as the dependencies are copied into the `target/lib` directory.

The application is now runnable using `java -jar target/demo-product-1.0.0-SNAPSHOT-runner.jar`.

## Creating a native executable

You can create a native executable using: `./mvnw package -Pnative`.

Or, if you don't have GraalVM installed, you can run the native executable build in a container using: `./mvnw package -Pnative -Dquarkus.native.container-build=true`.

You can then execute your native executable with: `./target/demo-product-1.0.0-SNAPSHOT-runner`

If you want to learn more about building native executables, please consult https://quarkus.io/guides/building-native-image.
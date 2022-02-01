FROM maven:3.5-jdk-8-alpine AS builder
WORKDIR /worker
COPY . /worker
RUN mvn dependency:resolve && \
mvn package && \
mvn dependency:purge-local-repository

FROM openjdk:8-jre-alpine
WORKDIR /worker
COPY --from=builder /worker/target/worker-jar-with-dependencies.jar /worker/worker.jar

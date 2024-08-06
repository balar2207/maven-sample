sample (WAR-style)
===============

This is the simplest possible Java webapp for testing servlet container deployments.  It should work on any container and requires no other dependencies or configuration.

```
git clone https://github.com/balar2207/maven-sample.git

docker run -it --rm --name my-demo-maven-project -v /root/maven-helloworld/:/usr/src/mymaven -w /usr/src/mymaven maven:3.3-jdk-8 mvn clean package

```

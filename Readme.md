Small example project demonstrating the following issue:

Adding the dependency io.debezium:debezium-testing-testcontainers
breaks the logging in a Spring Boot application.

To try out, run the `DemoApplicationTests` and see the logging output.
Then, in the pom.xml, add this dependency:

```
		<dependency>
			<groupId>io.debezium</groupId>
			<artifactId>debezium-testing-testcontainers</artifactId>
			<version>2.1.2.Final</version>
			<scope>test</scope>
		</dependency>
```

and rerun the test. There will be no logging output.
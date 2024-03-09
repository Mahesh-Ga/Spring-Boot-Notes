## Spring Boot Notes

1. Spring Boot Supports specific java versions: 

	SPRING BOOT: `3.x.x` => JAVA 17 or 21
	SPRING BOOT: `2.x.x` => JAVA 8 or 11 or 15 
    ONLINE FOOD ORDERING AND DELIVERY SYSTEM: Spring Boot Version: `2.7.13`

2. A version with the suffix "SNAPSHOT" indicates that it is a development version or a version under active development.

3. To check the installation path of a specific Java version on your system, 
	Windows: `where java`
	Linux/macOS: `which java`

4. 	**Dependencies**
	1. Spring Web
	2. Spring Data JPA
	3. MySQL Driver


5. ### Steps to run Spring Boot Project:
	1. Right Click -> maven -> Force Update
	*If getting ClassNotFoundException Clean Project*
	2. To clean, Run as -> Maven Clean
				 Project -> Clean...	
	3. Run as -> Spring Boot Project

6. 	Default port 8080
	
7. **White Label Error Page** 
	A "Whitelabel Error Page" typically indicates that an **unhandled exception** occurred in a Spring Boot application. When you see this error, it means that **Spring Boot's default error handling mechanism** has kicked in and it's displaying a generic error page instead of the expected application page.	


	*Handle Exceptions:* Ensure that your application properly handles exceptions. You can use Spring's `@ExceptionHandler` annotation to define methods that handle specific exceptions and return custom error responses.

8. **Project Structure** 

	* src/main/java/com/test/demo -> Application.java(`main` method)(`@SpringBootApplication`) 
								  -> /controller/controllers.java
								  -> /service/services.java
								  -> /dao/daos.java
								  -> /entities/entities.java
			
	* src/main/resources 		  -> application.properties 
		* contains non-Java resources such as property files, XML configuration files, static resources 
		* *application.properties*: configure properties such as database connection details, server port, logging levels, etc
		
	* src/test/java/com/test/demo -> ApplicationTests.java(`@SpringBootTest`)
		* contains test Java source code

	* src/test/resources 		 
		* contains resources for testing, such as configuration files, test data
	
	* target(maven) OR build(gradle)
		* output directory for *compiled code, resources and generated artifacts* produced during the build process.
		* When you compile a Maven project, the resulting compiled Java classes, along with other resources such as property files, XML configurations, etc., are placed in the `target/classes` directory
		* Also, any generated files, such as compiled `JARs, WARs` or any other artifacts, are placed in the `target directory`.
	
	* Maven Dependencies
		* Virtual representation of the dependencies specified in pom.xml file.
		* Maven handles dependencies by downloading them from remote repositories (such as Maven Central) and caching them in your local Maven repository
			* For Unix/Linux/Mac: `~/.m2/repository`
			* For Windows: `C:\Users\{YourUsername}\.m2\repository`

	* `pom.xml` OR `build.gradle` (if using Gradle):
		* Project Object Model.(POM)
		* manages dependencies for your project. 


# Creating new web application

1. Create a new maven application
Simple:
```mvn archetype:generate -DgroupId=in.sureshsarda -DartifactId=simplewebapp -DinteractiveMode=false```

WebApp (We don't need this since we are using Spring but just for reference):
```mvn archetype:generate -DgroupId=in.sureshsarda -DartifactId=simplewebapp -DarchetypeArtifactId=maven-archetype-webapp -DinteractiveMode=false```

2. Add Spring Dependencies:
```
<parent>
	<groupId>org.springframework.boot</groupId>
	<artifactId>spring-boot-starter-parent</artifactId>
	<version>1.5.8.RELEASE</version>
</parent>
	
<dependency>
	<groupId>org.springframework.boot</groupId>
	<artifactId>spring-boot-starter-web</artifactId>
</dependency>
```

3. Create a controller:
```
@RestController
public class DummyController {

	@RequestMapping("/")
	public String index() {
		return "Greetings from Spring Boot!";
	}
}
```

4. Update the main method:
```
@SpringBootApplication
public class App 
{
    public static void main( String[] args )
    {
        SpringApplication.run(App.class);
    }
}

```

5. Run it and you are done!!

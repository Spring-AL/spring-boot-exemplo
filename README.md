# Exemplo de Spring Boot Application
Criando um projeto maven e configurando o spring boot

Maven Spring Boot
 
    	<parent>
      	 	 <groupId>org.springframework.boot</groupId>
     		 <artifactId>spring-boot-starter-parent</artifactId>
     		 <version>1.2.5.RELEASE</version>
    	</parent>	
    
    	<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-web</artifactId>
		</dependency>
	
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-test</artifactId>
			<scope>test</scope>
		</dependency>
  	
Classe Main Spring Boot

    @Controller
    @SpringBootApplication
    public class HomeController {
	
     	private static final Logger logger = LoggerFactory.getLogger(HomeController.class);
	
    	@RequestMapping(value = "/", method = RequestMethod.GET)
    	@ResponseBody
	    public String home() {
	    	return "hello World";
	    }
	
	    public static void main(String[] args) {
	   	   SpringApplication.run(HomeController.class, args);
	    }
	 }  



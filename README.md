# MycoolApp
Java Backend Monolithic Application Development practice

Problem
You need for your app to be configurable....no hard-coding of values
You need to read app cofiguration from a properties file

Solution : Application Properties file
By default, Spring Boot reads information from a standard properties file
Located at: src/main/resources/application.properties

You can define Any custom properties in this file
Your Spring Boot app can access properties using @value

Development Process
1. Define custom properties in application.properties
2. Inject properties into Spring Boot application using @Value

Step 1: Defining custom appliation properties
coach.name=Mickey Mouse
team.name=The Mouse Club

Note: You can define any custom name as per requirement

Step 2: Inject Properties into Spring Boot application

@RestController
public class FunRestController {

    // inect properties for: coach.name and team.name
    @Value("${coach.name}")
    private String coachName;

    @Value("${team.name}")
    private String teamName;

    Here other coding or config required spring boot automatically reads application.properties file and access those values using @Value
    annotation
}
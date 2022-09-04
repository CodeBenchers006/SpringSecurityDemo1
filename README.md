# SpringSecurityDemo1
This POC is to learn how to configure Authentication Manager Builder


Step1 - Create a normal Spring Boot Application

Step2 - Add a dependency - "spring-boot-starter-security" which enables Spring Security on your SB Application

Step3 - Create a class (eg. SecurityConfig) and extend it with WebSecurityConfigurerAdapter class

Step4 - Add @EnableWebSecurity annotation - It allows Spring to find (it's a @Configuration and, therefore, @Component ) and automatically apply the class to the global WebSecurity

Step5 - Override the configure method configure(AuthenticationManagerBuilder auth)
      - Here we are using "in memory data" so we used auth.inMemoryAuthentication()
      
      NB: NoOpPasswordEncoder has been depreciated, so inorder to use it, we assign {noop} along with password (eg. .password("{noop}abc");)
      
Step6 - Create a controller, inorder to test whether your authentication is working on you API.

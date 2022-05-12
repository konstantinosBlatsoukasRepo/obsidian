.antMatchers("/", "index")
.permitAll()


```java

public class ApplicationSecurityConfig extends WebSecurityConfigurerAdapter

protected void configure(HttpSecurity http) throws Exception {
http.authorizeRequests()
    .antMatchers("/", "index")
    .permitAll()
    .anyRequest()
    .authenticated()
    .and()
    .httpBasic();
}

@Overide
@Bean
protected UserDetailsService userDetailsService() {
	return super.userDetailsService();
	User.builder()
	.username("anna")
	.password("smith")
	.roles("STUDENT", "GENIUS")
}
```
